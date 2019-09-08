---
layout: post
title: Noise Monitor
image: /soften-portfolio-jiqi963.github.io/img/noise3.jpg
bigimg: /img/iot2.jpg
---

### Touch the user
I and Bee went to Polykids and interview their manager.
Myone(The manager) said she does not need too much function such as a website or talking with LoRa server, the only thing it has an indicator light tells them how noise here.
It should be had three indicator light, keep green when DB(Decibel) < 70, turn on the yellow light when the DB between 70-85, if the DB higher than 85DB turn on the red light.
So, this's real user story and it easier than our think.
![Decibrl](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/Decibel.jpg?raw=true)

### Working noise monitor
The microphone only can get valid ADC values, because the value of dB is not linear with the value of ADC’s, so I will convert this ADC to DB.
Here has [some way](https://forum.arduino.cc/index.php?topic=318908.0) can do this, and here has a table tell me how those readings work.

| ADC | DB |
| --- |---:|
|460|44|
|480|47|
|500|59|
|508|60|
|550|61|
|600|63|
|613|65|
|700|70|
|859|78|

Once you get these numbers you will be able to form the below equation like `ADC = (11.003* dB) – 83.2073`.
From which you can derive the dB to be `dB = (ADC+83.2073) / 11.003`.

### Build a test model
After got all stull and the formula, I going to build a test model, it will reach the goal of kindergarten. Here is a Schematic

![Schematic](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/noise.jpg?raw=true)


#### order new sound detect
After talking to Vaughn, I know that the MAX9814 does not meet the kindergarten goal, and the default 'maximum gain' is 60dB.
By the way, I am looking for a new one that needs to achieve the purpose of the kindergarten.

I found a microphone on TradeMe and double check with Vaughn which can gain the max 125DB.

This [Datesheet](https://github.com/SoftEnOP/soften-portfolio-jiqi963.github.io/blob/master/img/MAX4466.pdf) include all the information you needed.