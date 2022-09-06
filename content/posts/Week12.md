+++ 
draft = false
date = 2022-08-09T23:56:36+05:30
title = "Week-12 (Coding Period) 4th August - 11th August"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
- Read a chapter exclusively on saints from The Gothic Image by Emile Male.
- Annotated 200 images + previous images with more attributes I learned from reading the book by Emile Male

## Paintings in context
This whole time I had been curating images and trying to annotate them but after reading 70 pages of this book. It made things really clear for me so I think it will be great to explain how Christian Paintings really work.


The first thing to keep in mind is that position matters. For instance, if we consider an image of Jesus being crucified. Then you can't just change positions of people beside him. On Jesus's right it has to be Mary and on his left it has to be John. This matters at least at that time it did.

Next, a lot of the paintings show saints holding a book. This was a common thing in the 13th century as it was attributed with possessing wisdom and being knowledgable.

Some paintings also show saints holding things like swords, cups, crucifix. One wonders what these signify right. There were two things behind this. 

- First reason was to distinguish saints that might look same. While earlier saints used to write the names on paintings, Chartres came up with a brilliant solution by including an attribute that resulted in the death of that saint. So some saints were seen holding a crucifix and some saints were seen holding a cup possibly because they died of posioning.

- Placing a sword, or cup of poison in a saint's hand would feel odd and hence would attract attention(this is what the thought process was here)

Some other attributes are not shown in the hand and it is supposed to be in background. For instance, saints like St Mark always have lions in the paintings so what this means is that Saint Mark was killed by a lion. On the other hand in case of St George paintings have dragons in them which signifies how he saved a princess from a dragon.

Last thing is other background elements like trees, forts etc. In these paintings it is kept minimal and more focus is on the saints in paintings. The saints themself might not have any expression to potray their superhuman abilities. The last part is not for all cases of course.



## Adding more labels.
After reading a section of the book. I reviewed the paintings again and reannotated 200 images with more attributes and annotated additional 400 images. After applying augmentation the size of dataset is approximately 1200.

Following are the labels.
- Angel
- Arrow 
- Baby 
- Book 
- Christ 
- Cross 
- Crown
- Cup
- Flower
- Fruit 
- Horse
- Instrument 
- Key 
- Lamb 
- Lion 
- Mary 
- Pen 
- Saint 
- Skull 
- Staff
- Sword 

While the labels are more the no of instances of each object are uneven so my model failed on some of the classes that are not annotated extensively. So that is something I have to work on as I perfect this. Another challenge to take is to annotate more images where the whole life of a saint is depicted in a single painting. I have tried to exclude those as it is more difficult to interpret them but it is important to include them as well as the module might fail on those instances. Finally the last thing is to annotate across different forms of artworks. The initial dataset I had collected had only fresco/oil paintings but now I have tried to include more instances like prints and stained glass paintings.

Nonetheless, here are the results on some new labels.

![](/frcnn_outputs.jpg)

# Next Week
![](/n_2.png)
The outputs from the object-detection module are supposed to be inputs to our encoder but if we see the architecture the decoder also has some inputs so my next step is to work on this module while perfecting the object-detection module of course