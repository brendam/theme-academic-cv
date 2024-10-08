---
title: Hearing the Unseen
date: 2010-07-19T13:23:43+11:00
layout: post
profile: true
aliases: /2010/07/19/hearing-the-unseen/
tags:
  - Art
  - Data Visualisation
  - User Interface
  - Sonification
image:
  # Caption (optional)
  caption: "Ear diagram"
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point: "Smart"
  # Show image only in page previews?
  preview_only: true
---
This is based on a Poster/Demo presented at the <a href="http://hyperstudio.mit.edu/h-digital/">"Humanities + Digital Visual Interpretations Conference"</a> hosted by [HyperStudio - Digital Humanities at MIT](http://hyperstudio.mit.edu/) 20-22 May 2010.

{{< figure src="featured.png" title="Ear diagram" >}}

* [Barry Moon](http://barrymoon.net)</br>
Arizona State University
* **Brenda Moon**</br>
The Australian National University

This project started as a exploration of data sonification techniques. The [abstract published in the conference program](http://hyperstudio.mit.edu/stored/moon-barry/) is a testament to this. As it progressed, the idea of using real-time data to create a game for mobile devices became more alluring. More specifically, a game where sound plays a major role in decision making, or even a game that produces interesting music with minimal interaction. For this application, the meanings of the data become far less important than its trends and time basis. We are using stock market data which wakes up and goes to sleep at fixed times of the day. Music, being predominantly time based, suits this kind of predictable framework upon which to drape its material. Although the creation of a game is the direction our sonification research has taken us, similar techniques could be applied to data to not only reveal details, but make the exploration of those details interesting and fun.

As you will see in the [conference program](http://hyperstudio.mit.edu/stored/moon-barry/), our early model was programmed in Processing and Max/MSP. While this gave us a great deal of flexibility over visualization and sonification, it would not be usable on mobile devices in the near future. For our game, the iPhone/iPad was chosen as the device, and Unity as the programming solution. Choosing to use the iPhone/iPad over Macintosh should generate a greater amount of feedback from users to aid in development and create a stronger sense of intimacy with the interface via touchscreen.

Most approaches to producing sound in interactive media follow precedents set in film. So far, in our work, we have combined two sonic elements traditionally used to enhance visual media: music and "off-screen" sound. Music reveals details in the data in two ways:

1, Amount of rhythmic activity relates to a share's trading volume - the greater trading volume per sample (6 seconds), the greater the number of beats per measure

2, Pitch change across the duration of the "measure" relates to price changes of the share -downward pitch sequence for falling share price and upward pitch sequence for increasing share price.

{{< figure src="Figure1.png" title="Figure 1: Typical bar of music with moderate trading volume (9 beats) and share increase in share price." >}}

When data is off-screen, it continues to be heard, spatialized according to its position in the corresponding visual space (Figure 2a & 2b):

{{< figure src="Figure2-GameView.png" title="Figure 2a: Game View" >}}

{{< figure src="Figure2-TopView.png" title="Figure 2b: Top View" >}}

Our main concern in creating a musical sonification (as it is in most music creation) is the balancing of repetition with variation. We generate music statistically by choosing beats via weighted probabilities. This extends a drum machine programming analogy, which if simplified (to create really horrible techno for example), the kick drum is heard on the downbeats and snare drum on upbeats.

{{< figure src="Figure3.png" title="Figure 3: Beat Tables" >}}

Audio samples are triggered at the statistically chosen beats. Audio synthesis would allow greater sonic variety, but there are no methods presently available in Unity. Sixteen percussive samples of different loudness were created for each sound. There needed to be some balance between percussiveness (which aids in direction perception), and "pitchedness" (since we are using pitch as a perceptual referent for price change). Samples needed to be quite short (less than one second), again because of limitations in the Unity environment.

We ultimately wanted to call our game "Our Tax Dollars at Work", but found some of the bailout recipients have extremely low trading volume. Instead we chose shares with large trading volume (which does include CitiGroup and Fannie Mae), and our working title is now "b-trade".

Enhancements we would like make to our game before letting it loose on the public (as much as iPhone/iPad users represent "the public") are enhanced visual interface, greater variety of sounds, the potential for users to design their own "beat tables", and for the game to morph between multiple "beat tables" to create greater musical variety. We would also like the user to be able to choose which company's shares they follow.

* Max/MSP: http://www.cycling74.com/
* Processing: http://processing.org/
* Unity: http://unity3d.com/
