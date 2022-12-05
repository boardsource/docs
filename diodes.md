 # Welcome to the ultiment diode guide

 By the end of this you should know everything you could ever want to know about diodes when it comes to keyboards.

 Table of contents:
 * [why we use them](#why)


## What is a diode
A diode is a very simple fondaital electronic component.
So what a diode does is only alow electricty to flow in one direction.(sometimes it almost never lets it flow ).
To that point a little out of scope of this article but they will alow electricty flow in the other direction when pushed hard enough see more in [other uses in keyboards](#other-uses-in-keyboards). But lets continue to the next section in seeing why we would only want electricty to flow in one direction. 

## Why we use them

![The keyboard matrix](matriximg)
So in our standard keyboard matrix we have one diode per keyswitch and that is connected the the row and the key switch.
Then the other pin of a switch is connected to the the colum.
Each row is connected to one pin on our microcontroller, and each colum is connected to a pin.
So now we know the parts involved and how to wire it but lets talk about why.
So lets make a very simple fantisy firmware call it Foo-MK, in our firmware we need to tell the computer when a key is pressed. 
So we need to figure that out for our selfs, how do we do this we know that we have a n number of row pins and n number of colum pins.
What we will do is loop over every row and for each row pin pull it high ( meaning that we make that pin output 3.3v or 5v ).
Next we will scan every colum pin and see if any of them are being pulled high ( note we did not set them high so they would default to low o   r 0v). 
If we then find one that is high we can assume its because the switch at that intersection is being pushed.

 Thats all well and good but what does the diode do you my rightly be thinking. Well lets get into an edge case.... well something that may seem like an edge case but happens all the time.
We push 2 keys at the same time ⁀⊙෴☉⁀. 
Lets go over what would happen if we had no diode, electricty will flow through the switch and out into the rest of the switches pulling unexpected pins high, leading to false presses aka gohsting.
With our diodes installed we limmit the the electricty from flowing backwards and pulling unexpected colums high.

### Other options

Now diode matrixes are not the only game in town to solve this problem. 
another way of dealing with this is simply deacate a single pin to each switch.
![diode less matrix](diodelessmatriximg)

Now you say great but my microcontroller only hass n number of pins and I want n+1 keys, no worries use a port expander.
![port expander matrix](portexpandermatriximg)
Lets get back to the star of our show the humble diode in our next section we will look over the diffrent packages diodes come in and no I dont mean bags or boxes ;).

## Diode packages and what they look like

So we know why we want a diode but what in the heck do they look like?

### Through hole 
![raw through hole diode]()
this is what a uninstalled through hole diode looks like.
You will likely notice that they dont look the same, But they have things in common. All diodes will have a marking on them to indacate the direction that electricty will flow. Above and on most diodes the marking is a black bar( on a glass diode ) or a white / grey bar on black diodes.
![installed through hole diode]()
You can see here that to install them the legs of the diodes have to be bent.
The reason you would use a through hole diode is because of there ease of soldering, this comes at a cost of taking up space in our PCB.

### SMD 
![raw smd diode]()
Again you can see that they may look diffrent much like the through hole diodes they are equivelent and work the same it is a mater of taist weather to go with mel package (glass) or the more terdisnial black smd diode.
![installed smd diode]()
Here you can see just how much smaller a smd diode is on the keyboard.
Once you get used to it soldering them is not much harder and a lot faster (even if your hand soldering).

#### One other package 
The last package I want to bring up is the diode bank, these are sevral smd diode put together. while not very common to build with you can find them in a lot of keyboards due to the lower component count. Witch saves space on your pcb and saves you money when haveing your PCB factory assembeled. 
![smd diode bank]()

### How to solder diodes?


## Other uses in keyboards