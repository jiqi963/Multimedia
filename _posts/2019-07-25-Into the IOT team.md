---
layout: post
title: Into the IOT team
bigimg: /img/iot1.jpg
---

# First week

I joined internet of thing team, the reason is I like arduino thing and enjoy create stuff.

Our team have some project like Orokonui senser, classroom senser and also need to maintenance some website.

Before I work on the classroom senser, I need to know how the sensor work and connect the gateway,so I did some practice...

The classroom senser looks like this:
![Senser](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/adafruitNode.jpg?raw=true)

It use a `AdafruitFeather32u4`, so the key point is how to get data from this broad.

Firstly I need get a key for our devices. Access [The Things network](https://console.thethingsnetwork.org/). We need three code from here, that device address, network sessoin key and app session key the first one should has 4 groups code other two should has 16 groups code, it's should looks like that.

![code](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/week11.jpg?raw=true)

After I got three code, copy/paste to arduino IDE

![IDE](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/week12.jpg?raw=true)

Also, there have some library need to be install, follow the introdacution on [Gitlab](https://gitlab.op-bit.nz/BIT/Project/Internet-Of-Things/nodes/tree/master/AdafruitFeather32u4-ABP-ClassroomSensor-AU915) is easy.

When all thing set up, you can get the data from data page. 

By the way, I didn't do much in the first week, but I understand how classroom sensors work, which is very helpful for the challenges that follow.