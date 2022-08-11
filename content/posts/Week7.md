+++ 
draft = false
date = 2022-07-11T14:56:36+05:30
title = "Week-7 (Coding Period) 1st July - 8th July"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
This week I worked on curating data points from two sources i.e the Art Institute of Chicago and the Metropolitan Museum of Art.

## 1. Art Institute of Chicago.
The [Art Institute of Chicago](https://www.artic.edu) provides open access to around 50,000 artworks with rich metadata involved. By using the search tool provided by the Institute we have got around 1500 results that pertain to containing Christian content in them.

Let's look at one of the art pieces.

![christopher](/christopher.jpg)

### Metadata involved.
|     |      |
|-----|------|
|Artist| Martin de Soria |
|Title|Saint Christopher Meets Satan; Saint Christopher before the King of Lycia |
|Place|Spain (Artist's nationality) |
|Date|1450–1487 |
|Medium|Tempera with oil glazes on panel |
|Dimensions|156.2 × 92.1 cm (61 1/2 × 36 1/4 in.)| 
|Credit Line|Gift of Mrs. Chauncey McCormick |
|Reference Number|1962.964 |
|IIIF Manifest |https://api.artic.edu/api/v1/artworks/15716/manifest.json |


During the curation process I am also logging some of the attributes from the metadata. The advantage of this is that it keeps the dataset open to more usecases.

### Interpreting the metadata.
Based on the metadata we can also understand what the painting is supposed to be and who are the actors in it. For instance the painting on screen depicts two scenes but only do we get a better idea of the actors when we read some of the attributes from the metadata.

### Filtering the artpieces.
The artpieces are a numerous but we are only focussing on two-dimensional versions like paintings, prints, stained-glass. Apart from that while Christian Icons might be a lot we only want to focus on saints, actors like Mary, Jesus etc.

To accomplish the former we use the metadata itself and for the latter we use the labels from the [Iconclass](https://test.iconclass.org) dataset.

What we do is that we take the labels and we find keywords matching to the labels. Once we do it is considered a valid source.

### Results.
After the scraping process we got access to 900 images. It is a low number honestly speaking because scraping these images takes time.

![chicago-source](/chicago_source.jpg)

We also observe various styles like fresco, oil paint, print suggesting a good mix of artwork.

## 2. Metropolitan Museum of Art.
The [Metropolitan Museum of Art](https://www.metmuseum.org/art/collection) provides open access to 375-400k images with metadata.

Out of these images using search words as "saints' left us with approximately 9k images.



### Further filtering.
After retrieving these images we limit the amount of artworks we want.

Hence the artworks are restricted to.

1. Tempera
2. Stained Glass
3. Painting
4. Oil Paintings
5. Canvas

This step leaves us with 1k images and the reason is that the themes becomes common and hence the overlapping paintings are removed.


### Results.
The finale of the retrieval is added to the dataset along with the metadata.

![met](/met_source.jpg)


# Next week
Working on stained-glass painting sources like [Corpus Vitrearum](https://corpusvitrearum.de/)
