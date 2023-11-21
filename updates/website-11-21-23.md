---
title: AI Chat?
description: How we Built an AI chat on our website
author: Boardsource
product_link: https://boardsource.xyz/store/61d0b772319a1f3cc53ba2fb
subcategory: shop update
draft: false
tags: 
- programing
- update
banner: https://images.boardsource.xyz/banner.jpg
thumbnail: https://images.boardsource.xyz/thumb.jpg
---

# Building an AI Chat for Your Website: A Comprehensive Guide

## Overview

In the era of advanced technology, integrating Artificial Intelligence (AI) into your website can significantly enhance user interaction and satisfaction. One effective way to achieve this is through an AI chat that not only responds to user queries but also directs them to relevant documentation. In this blog post, we'll delve into the intricacies of how we built an AI chat for our website.

Our AI chat system takes a unique approach by analyzing our documentation to find the most suitable information for user queries. If the AI can't provide a direct answer, it gracefully redirects users to our Discord community for further assistance.

### 🚫Warning🚫 this is a very technical document going deep into code if you care great this is the blog post I wanted when we first started down this path. If not your take away can be we are testing an ai chat for the website.

## How Does It Get Info from Our Docs

### Document Embeddings

The key to our system lies in document embeddings. We convert our documentation into embeddings, which are representations of text in a numerical format. This involves breaking down the document into smaller chunks and transforming each chunk into an embedding. An embedding is a mathematical representation that captures the semantic meaning of the text.

To keep our embeddings up-to-date, we regularly check the last update time of each document. After a certain period, we refresh the embeddings in our database to reflect the latest changes in our documentation.

We've opted for the all-MiniLM-L6-v2 AI model for generating these embeddings. The decision was driven by the ability to run the model locally, providing flexibility and eliminating vendor lock-in concerns.

**Code Example:**

```typescript

export const embedDoc = async (path: string) => {
    const model = new HuggingFaceTransformersEmbeddings({
        modelName: "Xenova/all-MiniLM-L6-v2",
    }); // our embeding model.
    try {
        const client = createClient(url, privateKey); // our connection to our vector database
        const store = new SupabaseVectorStore(model, {
            client,
            tableName: "documents",
        });

        const splitDocuments = await getAndSpltDocs(path) // this takes a url path and fetches that 
                                                          // document then splits the doc into parts
                                                          // and returns them for us to use.

        const ids = await store.addDocuments(splitDocuments); // this takes that array of split 
                                                              // documents and puts them into 
                                                              // the AI to get embeddings
                                                              // then stores them into the database 
  
    } catch (error) {
        // handle the error here
    }

}

```

**So what does this look like really**

This is a single split part of a document: 
```javascript
Document {
  pageContent: '# What are Combos in a Keyboard Firmware?\n' +
    '\n' +
    'Combos are a feature that allows you to assign special functionality to combinations of key presses. Different keyboard firmwares may have different implementations and options for combos, but the basic idea is the same. Some of the common types of combos are:\n' +
    '\n' +
    '- **Chords**: Chords are combos that match keys in random order, all pressed within a short time window (usually 50ms or less). For example, you can define a chord that activates KC.ESC when you press KC.A and KC.S together.\n' +
    '\n' +
    '- **Sequences**: Sequences are combos that match keys in order, pressed within a longer time window (usually 1s or more). For example, you can define a sequence that activates KC.LWIN when you press KC.A, KC.B and KC.C in order.\n' +
    '\n' +
    '- **Leader keys**: Leader keys are special keys that start a sequence of key presses that trigger an action. For example, you can define a leader key that activates KC.LWIN when you press KC.LEAD followed by KC.A.',
  metadata: {
    handle: 'articles-what_are_combos_in_a_keyboard_firmware',
    loc: { lines: { from: 1, to: 9 } }
  }
}
```
you can see the `pageContent` is one section of the document.
and we also store the `metadata.handle` so we can use that to link to the correct document.

Now we pass this into the Embeddings Ai and that returns this:
```javascript
embedding:{
    content:`# What are Combos in a Keyboard Firmware?

Combos are a feature that allows you to assign special functionality to combinations of key presses. Different keyboard firmwares may have different implementations and options for combos, but the basic idea is the same. Some of the common types of combos are:

- **Chords**: Chords are combos that match keys in random order, all pressed within a short time window (usually 50ms or less). For example, you can define a chord that activates KC.ESC when you press KC.A and KC.S together.

- **Sequences**: Sequences are combos that match keys in order, pressed within a longer time window (usually 1s or more). For example, you can define a sequence that activates KC.LWIN when you press KC.A, KC.B and KC.C in order.

- **Leader keys**: Leader keys are special keys that start a sequence of key presses that trigger an action. For example, you can define a leader key that activates KC.LWIN when you press KC.LEAD followed by KC.A.`,
embedding:[-0.0715645,-0.08542983,0.07252541,/*....300 more of these*/, 01806953,-0.0450035,0.07591504,-0.011525745,-0.021956643,-0.017396873,0.009075671,-0.013171698]
metadata: {
    handle: 'articles-what_are_combos_in_a_keyboard_firmware',
    loc: { lines: { from: 1, to: 9 } }
  }
}
```

Now you can see mostly the same stuff but a new member called `embedding` these are all of the words as numbers.
These we can use to do similarity searches using math instead of string, making the whole search very fast and more accurate.


## How We Generate the Answer

### Prompt Engineering

Once a user submits a query, we convert their question into an embedding and search our database for similar embeddings. This ensures that the AI identifies the document most likely to answer the user's question.

To generate the final answer, we utilize prompt engineering. This involves taking the search results' embeddings, combining them with the user's question, chat log, and predefined instructions, and feeding this composite prompt into our AI model of choice.

**Code Block:**

```typescript

export const retriever = async (prompt: string, chatHistory: string[] = []) => { // this is our 
//entry point where we take in the prompt and chat history then build the prompt we will send into 
//the ai and seach our docs database for relevent info for the ai to use as context.
    const formattedPrompt = await buildProptemplate(prompt, chatHistory)
    const result = await prompAi(formattedPrompt)
    return result
}

const buildProptemplate = async (prompt: string, chatHistory: string[] = []) => { // this function 
                                                    //takes the user's question and the chat history 
                                                    //and formats it into a prompt for the AI to use
    const embeddingsModel = new HuggingFaceTransformersEmbeddings({
        modelName: "Xenova/all-MiniLM-L6-v2",
    });

    const client = createClient(url, privateKey);
    const vectorStore = new SupabaseVectorStore(embeddingsModel, {
        client,
        tableName: "documents",
    }); // connect to vector database

    const res = await vectorStore.similaritySearch(prompt, 2); // take the user promt and search the database.

    const formattedPrompt = await questionPrompt.format({
        chatHistory: chatHistory.join(" "),
        context: cleanContext(res),
        question: prompt
    });// this helper function fills in blank spots in a template with the correct information

    return formattedPrompt
}

const cleanContext = (context: Document[]) => { // clean the context to only include the page       
                                                //content and the url in markdown format
    let searchResponce: { pages: string[], urls: string[][] } = { pages: [], urls: [] }
    context.reduce((acc, item) => {
        acc.pages.push(item.pageContent)
        acc.urls.push(
            [item.metadata.handle,`https://www.boardsource.xyz/docs/${item.metadata.handle}`]
        )
        return acc
    }, searchResponce)

    return `Documents: ${searchResponce.pages.map((item, i) => `${item} SOURCE:[${searchResponce.urls[i][0]}](${searchResponce.urls[i][1]})`).join("\n")}`
}

const prompAi = async (prompt: string) => { // this function takes the prompt and sends it to the OpenAI API and returns the result.
    const model = new OpenAI({
        temperature: 0
    });
    const res = await model.call(prompt)
    return res
}

```

**What is the end result of all of this "Prompt Engineering"**

so lets follow this step by step:

**user question:** `what are combos?`

**formatted Prompt:**
```markdown
Use the following pieces of context to answer the question at the end. If you don't know the answer, just say that you don't know, don't try to make up an answer. Always return markdown, and return any urls from context
----------------
CHAT HISTORY: ** array of past messages ** 
----------------
CONTEXT: ** used embeddings serarch to pull out the context and place it here thats a huge wall of text tho **
----------------
QUESTION: what are combos?
```  
**Output from AI with that Prompt:** `Combos are a feature in keyboard firmware that allows you to assign multiple keycodes to a single key. For example, you can define a combo key that activates KC.LCTL and KC.LALT when you press it.`

You can see that the answer is correct and is appropriate for our users it knows to only talk about combos in how they refer to keyboard.

**VS raw Chat GPT:**

**prompt:**` what are combos?`

**answer:**
```markdown
"Combos" can refer to different things depending on the context. Here are a few possible meanings:

1. **Combination Meals:**
   In the context of food or beverages, "combos" often refers to combination meals or packages. For example, at a fast-food restaurant, a combo meal might include a sandwich, fries, and a drink.

** Goes on and on nothing about keyboards.**

5. **Musical Combos:**
   In music, particularly jazz or improvisational genres, "combos" may refer to small groups of musicians playing together, often in contrast to larger ensembles.

If you have a specific context in mind, please provide more details for a more accurate explanation!
```

The results are even more impressive when we compare asking about building a keyboard :D 

## Then That Gets to the Front End

In terms of user experience, we designed a React component for the front end. This component renders the chat log, converts messages from markdown to HTML on-the-fly, and utilizes the Vercel AI package to manage message communication between the client and the server.

## The Stack

Our tech stack is a robust combination of tools and libraries:

- **LangChain:** Facilitates easy interaction with various components and aids in template generation.
- **Hugging Face TransformersJS:** Used for generating document embeddings.
- **Vercel AI:** Manages communication between the client and server for seamless chat interactions.
- **Supabase:** Stores document embeddings in a reliable and scalable manner.
- **OpenAI (as of writing):** Powers the final question-answering stage.

By integrating these technologies, we've created a dynamic AI chat system that not only responds effectively to user queries but also evolves with the updates in our documentation. Feel free to explore and adapt this approach for your website's AI chat functionality.



Quinn and Cole

Boardsource.xyz