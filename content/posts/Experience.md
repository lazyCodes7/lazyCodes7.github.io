+++ 
draft = false
date = 2023-01-27T14:56:36+05:30
title = "Google Summer of Code at RedHenLab"
description = "Getting accepted and some info on my project!"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

## Why am I writing this blog? 
Well I did my Google Summer of Code in 2022 that was like two years back. But every year I get a lot of people on LinkedIn or Twitter DMing about guidance, tips or just wanting to know about my experience. So this is a blog for them and to answer their questions!

So let's get started..

### Why RedHenLab?
Here in my college people are passionate to do GSoC like I am not kidding. A lot of juniors did it before me and I hadn't even tried once and I was in my third year at that time. I was into Computer Vision and thought of trying out for this program at least once somewhere around in May 2021 when the results were announced for GSoC 2021 I guess..

So yeah at that time I compiled a list of orgs I could try out for and I made sure that none of my friends or college seniors I knew were in that org. To normal people, this will definitely be a stupid decision but I kind of really wanted to join an organization that no one from my college had joined

So I joined the OpenMined slack. Yep. Not RedHenLab lol. Somewhere around August I think.

I thought Federated Learning was really cool so I started taking their courses tried setting up the codebase for PySyft and raised a solitary MR to their codebase but I don't know why I wasn't really enjoying this as much. The thing is I used to do a lot of hackathons during my college and so I liked taking up a problem and building things from scratch. That is where RedHenLab sort of came in.

I browsed RedHenLab and at first their goal of promoting research into multimodal communication kind of went top of my head. Obviously now I understand it better.

But yeah I was just browsing through the org page and I came across [this](https://www.redhenlab.org/home/the-cognitive-core-research-topics-in-red-hen/the-barnyard)

It is a barnyard of projects related to multimodal communication that haven't been solved yet. It was in this list that I found a project that I could work on.

## [Christian Iconography](https://www.redhenlab.org/home/the-cognitive-core-research-topics-in-red-hen/the-barnyard/christian-iconography-the-emile-male-pipeline)
One of the open ideas at RedHenLab. The idea related to Christian Iconography proposes building a pipeline that can identify the icons(in our case saints) and their attributes(such as sword, crucifix etc) by using Computer Vision. Previous work? Very minimal at the time I started just a dataset of 700 images built by [Insiyah](https://medium.com/@insiyahhajoori/red-hen-lab-christian-iconography-884a00aa66f8)

### Starting my work.
Although I had found something I liked. RedHenLab doesn't exactly have a mode of communication like Slack apart from their email. Before sending an email, I wanted to make sure that I had done something that could kickstart a conversation, apparently RedHenLab also states this they are not really looking for people interested in solving problems X,Y,Z but rather looking for people that know the problem and can propose ways to solve it. 

With that I got into my literary review to see if there was some prior work done on Christian Iconography. Luckily I found a paper that was close enough to what I wanted. It basically tackled classification of icons in Christian paintings. [Paper link](https://dl.acm.org/doi/abs/10.1145/3458885)

After implementing a paper I thought of ways to build upon this implementation and so I finally mailed the org on Jan 10, 2022

Following which I recieved a reply from Professor Mark Turner from CWRU who is one of the org heads.

(To be honest, the mail turned up in my spam and I saw it a week later. Moral: always check spam)

So yeah from then onwards we mailed each other a few times back and forth discussing about the possibilities. And at that time I really wanted to work on this project even it was not for GSoC but I was doing an internship at that time due to which I wasn't getting time to devote for this project.

### Announcement of ideas for GSoC 2022
It was somewhere around March I think when the ideas for GSoC 2022 had been announced by RedHenLab. At that time I was delighted to see that the idea that I had worked on was included for GSoC 2022. Moreover my implementation was referenced in the idea itself. A bolt of energy pretty much flew into me and I was like I need to do this:p

### Building up my proposal.
So yeah now that I decided that I will do GSoC for sure. I surveyed a lot of papers related to Iconography to figure out what was a viable project to do during the timeline of GSoC. After surverying I fixated on building a captioning module that captions the Christian art pieces and also tell us about their attributes. 

Now RedHenLab doesn't really encourage mails saying they are interested in solving a problem. Rather they want potential contributors to write up a pre-proposal describing their vision for the project and mail that instead.

So I pretty much did the same. For building my preproposal I looked into literary articles suited best to solving captioning in art and sent my proposal to RedHenLab. Contrary to people building their proposals for about a month. I used 5 days and mailed them the preproposal. To be honest I never received a mail until the deadline for submitting the preproposal on the GSoC website came and that is when I was asked to submit the proposal which was also when I received feedback to improve my proposal. Following which I submitted my proposal 1hr before the deadline(following some fixes on the feedback).

### Getting the acceptance.
So it was 20th of May when one of my friends sent me a screenshot showing that my name was in the list of accepted contributors. I was in Pondicherry for a trip and I was really overjoyed that day because I literally had zero hopes of getting selected. But yeah it was great.

This concludes my journey for getting Google Summer of Code

## Tips?
Although I don't think I am qualified enough to be giving tips to people. I would refer to this as a checklist.
- Find what you like. This is very important don't do GSoC just because it is a program to put on your resume.
- If you do find something you like. Put in the work, it doesn't matter whether you get selected for GSoC or not at least you can be glad you still did something. 
- Following on the last point you can still just contribute to the organization without GSoC. In case of RedHenLab you can even get LoRs from the professors you work with if they say so.
- This is something I realized when I was reviewing proposals for last year's GSoC with RedHenLab. Make sure to write a proposal that is clear and concise and tells the reader elaborately what it is you are trying to accomplish. It doesn't matter if you are grades are low, or your college is not a Tier-1 what matter is how you present what you want to do. We are not seeing your college when ranking proposals.
- And don't get disheartened if you don't get GSoC. I know I got it so easy for me to say but there are other things I got rejected for so it really isn't the end of the world

## Program
Now I have my weekly [blogs](/categories/google-summer-of-code/) that go in a very detailed way about my experience throughout the program and the work I did so do check it out. Apart from that I am glad that I got the opportunity to do my Google Summer Of Code with RedHenLab. While I am still a very inexperienced researcher, it definitely taught me how to carry out research and build small but working pipelines.

Post GSoC I still collaborate with Mark at RedHenLab for the Emile Male Pipeline. Last year I mentored a fellow contributor from my college to help build a pipeline for recognizing speech gestures in art!

For the folks interested in contributing to this project I would be delighted to help you out!

(I will keep this blog live and keep updating based on questions I recieve. But that's all for now:p)





