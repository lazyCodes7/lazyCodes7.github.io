+++ 
draft = false
date = 2022-07-03T14:56:36+05:30
title = "Week-5+6 (Coding Period) 19th June - 3rd July"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
- I continued my search for licensed souces and also found a really good site that provides API access/open access to museum metadata
- After compiling enough sources for 2 weeks I finally started the process for [curation](https://drive.google.com/drive/folders/1IKJg8bJU17ZyVrYfpa8J_nK-7cS2cJ0R?usp=sharing).

## Source 1 - The Web Gallery of Art
![web](/web.jpg)

The [Web Gallery of Art](https://www.wga.hu/) provides access to 60,000 artworks in the form of a dataset. This source has also been used in other art-related datasets like SemArt and ArtDL.

### Curation process.

#### Filtering records.
Previously it was discussed that we would be moving forward with renaissance paintings and hence first I filtered the dataset to find religious paintings. This left us with approximately 12k records.

Following is the analysis of the timelines associated with these paintings.

![timeline](/timeline.png)
We observe that a lot of paintings are from the renaissance era which is a good sign.

#### Some more filtering..
After filtering the records to find religious paintings. The next step is to find paintings that adhere to the Christian Religion. To accomplish this I have taken help of the Christian icons used in the Iconclass datasets. They range from male saints like Anthony of Padua, John the Baptist to female saints like Mary Magdalene etc. The criteria to filter was based on the description and titles of the paintings. If we found the iconclass then that would mean that the painting is containing content w.r.t to the Christian religion.

After this step of filtering we were left with 5.5k paintings.

#### Results.
![web-gallery](/web_gallery.jpg)

## Source 2: Iconclass AI Test Set
The [Iconclass AI Test Set](https://labs.brill.com/ictestset/) is a dataset containing 87k records of different icons from the Iconclass dataset with corresponding descriptions. While the descriptions are not well-harvested. It is still a good enough source.

### Curation process.
Since the dataset that explicitly contains iconclasses for each record. I just filtered the records corresponding to the Christian icons and added around 12,000 records containing Christian icons.

#### Results.
![iconclass](/iconclass_ai.png)


## Meetings

### Meeting 1
The first meeting was held by Mark and included just me. We just talked about the things to do with this project and how the problems that me and Parth are solving are part of a bigger pipeline.

I also learned about the FrameNet teams' annotation tool Lutma. While it is far fetched goal for the Emile Male pipeline it is still something possible in the future. 

### Meeting 2
The second meeting was held again by Mark and included me, Parth, Saby and other mentors as well. It was just a general discussion regarding our projects and problems we might be facing. Since I had started with the collection of data. The question I had in my mind was regarding the scale of data that I might have to collect. After discussion with Mark, I understood that I should try to solve a problem that solves a simple problem.

For eg: Given an image of Virgin Mary can our model learn what she might be doing?

Based on this discussion as of now my idea is to restrict the data to saints(male and female) and try and answer the question of what this saint might be doing or who this saint is or what are their possible attributes.






