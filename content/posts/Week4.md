+++ 
draft = false
date = 2022-06-19T14:56:36+05:30
title = "Week-4 (Coding Period) 12th June - 19th June"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
The project kickoff

Before the coding period began I had previously been working on classification of the Christian icons in the painting. But in order to caption art, we needed a good source. So I had been collecting sources here. 

In order to get some idea on how to proceed with the sources collected I contacted my mentor Fred.

## Minutes of the meeting. 
Attendees - Fred, Marcelo, Rishab, Tiago
- I gave a brief idea about how I plan to proceed with this project in two phases. First would be the curation and subsequently the creation of a multimodal pipeline.

- For curation, I proposed to build a simplistic module which will enable us to automatically add images(and descriptions) of paintings to a database(could be GDrive as well). Once the images are added it should automatically be assigned to a directory denoting a saint. The advantages of this would be that we could use it for both classification and tagging.
 
- Since classification is one of the goals of Parth’s project I also proposed that we could possibly work together

- Tiago asked me what are some of the challenges I could foresee. My answer was oriented mostly towards curation since I don’t possess any information on this topic.

- The next topic in discussion was related to the types of images we would be using. Whether it would be just painting or also sculptures or what period it would be from. Marcelo suggested that it would be better to stick to paintings as vision algorithms apply relatively easier. Apart from that we decided to stick to Renaissance paintings and then expand to other strokes/styles.

- Since I already had begun researching sources. I shared that in the meeting. While the sources are enough, we need to check the license details if we were to make the dataset public.

- The last minutes were related to the captions of the paintings. Given a source, what I need to check is whether these images are just mere descriptions or contain richer representations.

- An [example](https://3minutosdearte.com/wp-content/uploads/2016/10/El-Bosco-el-jard%C3%ADn-de-las-delicias-1490-1500-e1578065369211.jpg) of the prior was discussed by Tiago. The image has so many elements in it in every corner!

## License.
One of the problems foreseen by Marcelo was that if our dataset was to be made public then we would have to make sure that the sources we took images from allowed us to actually use their images for research or commercial purposes. Hence I spent some time figuring out whether the sources I had collected were usable or not. Apart from that I also compiled a list of musuems that provide open access to their images. I will be updating as I find more.



| Source | Link | Captions | Filtering | Size | License |
|---------|-----|----------| --------  | ---- | ------- |
|Art Institute of Chicago|	https://www.artic.edu/collection?q=saint|	Yes|	Required|	50k|	Creative Commons Zero (CC0)|
|Belvedere, Austria|	https://sammlung.belvedere.at/opencontent/images|	Yes(German)|	Required|	Unknown|	Creative Commons|
|J. Paul Getty Museum, Los Angeles|	https://www.getty.edu/art/collection/search?open_content=true&q=Saint|	Yes|	Required|	Unknown|	Unrestricted and commercial use|
|Metropolitan Museum of Art, New York|	https://www.metmuseum.org/art/collection|	Yes|	Required|	375k|	Open Access|
|Minneapolis Institute of Art|	https://collections.artsmia.org/info/open-access|	Yes|	Required|	50k|	CC PDM|
|National Gallery of Art, Washington, D.C.|	https://www.nga.gov/open-access-images.html|	Yes|	Required|	50k|	Open Access|
|Smithsonian Institution, Washington, D.C.|	https://www.si.edu/openaccess/|	Yes|	Required|	4.4M|	Open Access|
|Yale University|	https://artgallery.yale.edu/collection/search/saints|	Yes|	Required|	250k|	Open Access|

## Inspecting sources.
One of the points discussed in the meeting was that paintings normally have a lot of elements in them so while collecting sources we should also check whether the description correctly describes the elements of the painting. 

Let's understand this with an example.

![p7](/p7.png)

{{< rawhtml >}}
    <details>
    <summary>See the description.</summary>
    <br>
    This small devotional object differs stylistically from Buglioni's Madonna and Child Enthroned with Saints Francis and Anthony Abbot (1921.1180), also in the museum's collection. In contrast to the other work, the faces of the Madonna and Child are significantly less expressive, and the passages of exposed skin have been left unglazed. The Madonna holds a nude Christ on her left arm and wears a mantle of blue with green lining and a maroon tunic with a yellow collar and cuffs. Her bright yellow shoes and the purple of her tunic are characteristic of Buglioni's color scheme and can also be seen in the other work. The tabernacle frame is probably contemporary to the figures, although it may not have been created specifically for this altarpiece. Buglioni likely worked in the studio of Andrea della Robbia, where he would have studied the family's techniques for glazing terracotta. The frame is classically inspired, with Corinthian capitals and Buglioni's characteristic egg and dart 
    </details>

{{< /rawhtml >}}

This is a random image taken from the Cleveland Musuem of Art that provides open access to 60k images. 

If i would look at this image, normally I would say that a mother is holding a baby.

That is normal so why make a painting? Are the agents in the painting someone special? These are the types of questions that our description should answer.

Now if we see the description we observe that the description gives us more insights about the painting. It tells us about the expressions of the agents and who the agents are. It also describes the technique used and it's similarity to another painting. Hence the description feeds us with a richer understanding of the painting that our naive mind wouldn't comprehend by just looking at it.

More on this can be found [here](https://colab.research.google.com/drive/1rHVdRMJq7CJNXE2Z_o1QC5rW4gs2ueFy?usp=sharing)

## The Raw pipeline.

### 1. Data Curation
![curation](/curation.png)

### 2. Tagging
![architecture](/arch.png)


# Next week
Finalizing probably on what sources to take images from and what period.

