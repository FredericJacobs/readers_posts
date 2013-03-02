---
layout : post
title : Working on a Geiger Counter for iPhone
author : fred
published : true
date : 2011-06-12
slug : geiger-iphone
category : [technology]
tags : [geiger, iphone, counter, fukushima]
---
It has been a while now since I made this Geiger counter for iPhone. I would like to sum up all the things I've learned about it in this post before archiving the project.

![](http://f.cl.ly/items/3u0g1k1q2U3R0O082q3a/DSD_2747.jpeg)

##Why a Geiger Counter ?

Fukushima. That was the main idea. Geiger Counters are expensive and often not portable at all. There's no way people could own one. With this project, the components together are under 50$.
You could ask why people would want a Geiger but I can tell you that people are worried about nuclear radiations.
For instance the japanese tea seller at the end of my street was wondering if the tea he was selling was radioactive or not. Using our Geiger he found out it wasn't more than average.

## How does it work ?

The electronics of the Geiger counter is made out of 3 main parts. The transformer, the Geiger tube and the signal stretcher.
 
After having passed in the chopper, the current coming from the battery is transformed into alternating current. Then, the transformer amplifies the voltage up to 400 Volts that is needed by the Geiger tube to work. This high voltage on the electrodes allows the current passing through the tube when a particle enters the tube. This event lasts only a few microseconds. If the signal was directly converted to a flashlight or sound, it would be to short to be seen or heard. For that specific reason, we added a signal stretcher that allows the signal to be long enough to be seen. Given that this is an digital circuit, this means the output is either on or off and its state doesn't depend on the intensity and speed of the particles.

The Geiger tube is made of a metallic tube filled with ionizable gas in which are placed two electrodes.

Above are represented the two different cases viewed from inside the Geiger tube. When no particle enters the tube, no current can pass through the tube because the gas is not naturally conductive. When a particle enters the tube, it is likely to grab electrons from the gas. This is called ionization and now the gas is conductive during a short moment. Therefore the current can pass through it.


##What are the features of the Geiger ?

The Geiger has three outputs :

- LED : A LED light to show each time the detector gets a particle.
- Buzzer : A buzzer sound to hear show each time the detector gets a particle.
- mini-jack : Goes straight into the phone's mini-jack.

![](http://f.cl.ly/items/1O3i1i0O0e3E2B2z3V2A/DSD_2785.jpeg)


The iPhone app we designed offers the following features :

- Alert : Runs in the background and alerts you in case of high radioactivity. Sensibility can be set by a slider in the settings app.

- Measures  : The signal stretcher hides lots of disintegrations. Although the counter is not  precise enough to take lab measures, the number of disintegrations is linear. You can say that a radioactive material is twice as radioactive as another.

- Crowd-sourced maps : The iPhone app features a crowd sourced map with all users of the app. It uses the GPS chip of the iPhone to provide information of average radioactivity in a wide area. The gathered data is provided by different labeled sources.

![](http://f.cl.ly/items/0z0y1E130o3A0N2w3e3Q/DSD_2789.jpeg)

[More information](http://cl.ly/Fw1f)

If you need any information about the source code, feel free to ping me on Twitter. (@FredericJacobs)

This project was presented at the #ESI2011 in Bratislava.

With collaboration of Loïc van Oldeneel and Colin Hannesse.