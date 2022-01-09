+++ 
draft = false
date = 2020-03-28T14:56:36+05:30
title = "Networking Protocols"
description = "A try towards explaining what protocols are"
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++


## Protocols.

So what exactly are protocols? Protocols according to me are certain set of rules that we use to communicate with each other

## Why do we use Protocols ?

So in brief I explained about protocols but the next question is why do we need them.Let's consider an example,say I am Thor and I wanna talk to some new avenger(Night Monkey) then first I need Night Monkey's permission to talk(although I can just smash him with thunder and make him talk) and then Night Monkey will talk to Thor and so on a talk session starts.Now if you observe for talking  to some new person I need to first ask him,know about him and then I can start talking.Before talking I started with some set of rules that I had to follow so that I could talk to him.I couldn't just blabbering something as that person is unknown to me.This is the reason we need protocols or these set of rules.

## Protocols For Humans.
Like I said before.If you can see this boy and girl.The protocol for them to talk is pretty simple.The boy says Hi! and the girl replies back in the same manner.And then some weird romantic background music plays and they start talking to each other.This in short can be called as protocol for Humans.

## Protocols for Computers.

Now that I have discussed a lot about protocols for humans. Let's see how computers converse with each other.I think it's exactly the same except there is no romantic song played when boy and girl or no 'ooh' sound is made.So how computers exactly work is by a protocol call TCP(will explain about it later).So what happens exactly is that first the client says to server 'Let's Synchronize' and then server accepts this and then says ok 'I acknowledge your synchronize message' and then same message is acknowledged by the client and the connection is established.This can also be called as a three way handshake.

## The OSI Model.

Now what is thing I have written up there.I said we need protocols for talking,in the same way we need protocols for computers to talk and for this purpose the OSI Model was introduced. Now if you want to know the full form go search online and read the whole page so that maybe you will understand better.

### Seven Layers Of The OSI Model.

![](/osi.png)

As you can see there are seven layers in this diagram that is represented.Each Layer has different protocols for different purposes.Like application layer contains network protocols such as http and https for handling of info passed over internet.Let me explain now each layer one by one and it's purpose.

### Application Layer.

So the application layer is at the top of the OSI model.Now application layer consists of network applications like chrome,firefox,outlook etc.

### Protocols of application layer.

#### 1.HTTP

I know everybody knows about this but what exactly is this and why do we use it.So the reason we use http protocol is for viewing hypertext.Like there is a html webpage so other people can view your site only if it has http protocol.

#### 2.HTTPS

Let's say I am passing some password and my username through internet to login so first I will type my password and all and then I will click on submit after which it will pass through server and authenticate us.Now let's say between us and the server there is a hacker say noobmaster69(again avengers reference) who is trying to steal your password and will make you life real bad.Now you don't have space stone and the mind stone to go to that hacker and beat the hell out of him but you got https.What exactly it does is that it will convert your normal text into some really cryptic code and the hacker won't be able to do anything and your life is saved..

#### 3.DHCP 

Before I explain what is DHCP let's understand what would happen if I didn't have DHCP and that way you can understand better.

In Windows,we can choose our  IP address manually as well for using internet and all our thing like DNS etc.But say in a scenario there are 3 persons and they are setting up the IP address but by coincidence two of three IP address is same and hence those two won't be able to access the internet since IP addresses must be unique.In another scenario if the user is not using the internet anymore then that IP address is wasted.

From all these cases we can see that we need something that will automatically assign the IP addresses and also assign them only when you are using Internet.It should also give the DNS,subnet mask etc.

So the answer to this is DHCP and whatever I said was needed is exactly what DHCP does and it was created to handle these problems.

#### 4.SMTP

Ever wondered how do we send a mail to someone.Now that's a stupid question,we can use gmail or outlook right.But then how does it work how is it send to another person.Well the answer to this is SMTP protocol.The SMTP protocol is specifically used for delivering mails.It works with TCP/IP to deliver mails to specific recipient.

#### 5.FTP

So FTP  also called as file transfer protocol is basically used for transferring files.Using this we can transfer files in a secure manner between two machines.

There are many more protocols left that I haven't explained like DNS and some more but you can look for it in the geeksforgeeks site for more.

### Presentation Layer.

So I hope you understood the first layer.So now let's move on to the next layer which is the presentation layer.Now when I say the presentation layer of course it does not mean it's related to powerpoint presentation(bad joke).So the exact purpose of presentation layer is to convert the normal texts into some weird encryption and also it compresses the data to be sent so that more data can be sent,it also decrypts the encrypted data when it is recieved.

#### Protocols in presentation layer

I know only of one right now so will update later

#### 1.SSL

So SSL also called as secure sockets layer.Now SSL works with HTTP to get what is called HTTPS.Now I have already mentioned how https works so I won't repeat myself.But in addition to that I will mention one point that when using https the browser also checks if there is any certificate verified by known authority by that site.So if the certificate is not there or it's expired then https will alert to you to not enter any sensitive information like passwords or bank details.

### Session Layer.

Hope you understood the presentation layer. Moving on,we have the session layer.Now what exactly does layer this is that manages various sessions when you are on Internet.Like say you are on some site so first it will authenticate you as a user.Then it will acknowledge us.Then it will load the web page by sending files in form of data packets.Sometimes the file may not be accessible so it directs some message towards us.

### Transport Layer.

Hope everything is good till now and you haven't ran out of this blog post.Next up we have the transport layer.The main stuff happens in this layer so you might want to read a bit carefully.So in the transport layer we divide the files to be sent into data packets which consists of source and destination address and port no etc.This can be called Segmentation.Another thing that comes with Segmentation is flow and error control.Now let's say the server can send data at 50 Mbps speed and your computer can receive it at only 20 Mbps speed.So what flow control will do is that it will reduce it to 20 so that you can receive it.Error control comes when maybe some packet is not received so a message is sent to server to send it back.

#### Protocols in Transport Layer

#### 1.UDP

Now UDP(User Datagram Protocol) is a really simple protocol for sending data packets.It's connection less protocol.What it really means there is no sense of order behind sending these and there is no relation between the previous packets and the packets sent in the present.Also you can't check whether all the packets are sent or not.So then why have such a protocol that does not have much functionality.Well, we do use it anyways in my beloved games(Clash Royale) where you can manage to lose data packets though it pisses me off when I lose.Also UDP is faster than TCP.

#### 2.TCP

So TCP also called as (transmission control protocol) is almost same as UDP but has some improvements.Firstly,it is a connection oriented protocol so if some data packets are sent in certain order it ensures that same order is maintained when it is received.It has efficient flow and error control meaning if some data packets are not received it will ask the server to send it once more.Now a classic example of this thing would be the mail delivery system like say you are sending to some invalid email what exactly happens is that you get back a message saying that the mail was not delivered.So the purpose of TCP is in places where we need to ensure that all data packets are sent.Like mail delivery system.

### Network Layer.

In the Transport Layer I had said that files are divided in form of data packets called segments.This data packets are then sent to the network layer for further steps.For sending these data packets we need a logical addressing so that we can get something from source and send something to the destination.Now,logical addressing consists of IP addressing and subnet mask.So when we take these segments the IP address of two networks are attached to it and actually this is a data packet.It also uses path determination protocols to find shortest path to deliver data.

### Data Link Layer.

In the data link layer we use Physical Addressing.Physical addressing means the  MAC address and this MAC address of the source and destination is added to the data packets to constitute what is called a frame.MAC address is a permanent address which can't be changed.

## Physical Layer.

So till now we saw that the file is divided into various segments.After dividing into various segments the ip addresses are attached to it which makes it a data packet and then after this mac address is also used which converts it into frame.And then this frame is converted into bits and this bits is converted to signal and then this is passed through a media say air etc.And this is what constitutes the Physical Layer.

#### End.

So in this blog post I have talked about a lot of things about protocols.I started off with an example how humans use protocols to communicate and then I just extended it for computers.I told about the OSI model.How it Works and all.And I mentioned various protocols on the way.So in short how OSI model really works is like this:

So I am a user and I am sending a file so what happens is that the file contents are encrypted and divided into segments then I add the IP address of source and destination so it becomes a data packet.Then I add my physical source and destination address and then it becomes a frame.Now I have reached the end point and my frame is converted into bits,further into signals and then it's transmitted through media.Now my receiver is receiving this so what will happen.Of course,we go through in the reverse order now do the same steps until we reach the file so we convert signals into bits,bits into frames and we remove everything till we reach our file of course decrypting it though.This is it.

Hope Whoever read this understood

If you didn't.

JUST LIKE CAP SAID..

JUST CALL ME AND I WILL BE THERE.