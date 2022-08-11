+++ 
draft = false
date = 2022-07-18T14:56:36+05:30
title = "Week-8 (Coding Period) 8th July - 15th July"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
This week I spent curating data from two sources.

## 1. Corpus Vitrearum.
Corpus Vitrearum is a museum that has around 7000 stained glass artworks that are stored according to their iconclasses. By using various scraping techniques I scraped 2000 images that pertain to Christian iconographic content.

During the curation process I am also logging some of the attributes from the metadata. The advantage of this is that it keeps the dataset open to more usecases.


### Filtering the artpieces.
The artpieces are a numerous but we are only focussing on two-dimensional versions like paintings, prints, stained-glass. Apart from that while Christian Icons might be a lot we only want to focus on saints, actors like Mary, Jesus etc.

To accomplish the former we use the metadata itself and for the latter we use the labels from the [Iconclass](https://test.iconclass.org) dataset.

What we do is that we take the labels and we find keywords matching to the labels. Once we do it is considered a valid source.

### Results.

![chicago-source](/corpus.jpg)


## 2. National Gallery of Art.
The [National Gallery of Art](https://www.metmuseum.org/art/collection) provides open access to 130k images with metadata.

### Filtering the artpieces.
After retrieving these images we limit the amount of artworks we want.

Hence the artworks are restricted to.

1. Tempera
2. Stained Glass
3. Painting
4. Oil Paintings
5. Canvas

After following the criteria the dataset provided by NGA reduces to 900 records

### Results.
The final results along with the metadata have been added.

![nga](/nga.jpg)


## Completion of curation.
Over the past few weeks I spent a good amount of time understanding the types of paintings we are looking for and the types of descriptions. For instance if we consider an image of Mary we are looking for something that describes the emotions in the painting.

Let's consider two paintings.

![mh](/mary.png)

Now if we scraped an amateur title they both would probably say that Mary is with Jesus or something like there is Mary in this painting.

But that doesn't capture what is really happening.

After going through dozens of images what I have observed these are both different. In the first painting Mary is holding a baby version of Jesus and the second painting shows that Mary is sad as Jesus has died which is natural for a mother. When I started this project I would not have been able to identify these people but I think the captions that I was collecting built this intuition into me as a result of which I got better understanding of Christian Iconography and that's what the model should do as well and hence collecting good captions is important.

So following this methodology 

I have curated images from 5 sources. 

1. [Web Gallery of Art](https://www.wga.hu/) - 5k images
2. [Art Institute of Chicago](https://www.artic.edu/collection) - 500-700
3. [Met Art](https://www.metmuseum.org/) - 500-700
4. [Corpus Viteraeum](https://corpusvitrearum.de/) - 2k
5. [National Gallery of Art, Washington DC](https://www.nga.gov/) - 4-5k(WIP)

Which approximately sums up to 12-13k unfiltered images with metadata comprising.
1. Title
2. Medium
3. Artist
4. Creation Time
5. Description(Contextual meaning basically)

And forms of art mainly divided into
1. Painting
2. Print
3. Stained glass 

And period belonging to renaissance except for some prints.

# Next week
Now that I have gotten a satisfactory amount of images the next step is to work on the image-captioning model