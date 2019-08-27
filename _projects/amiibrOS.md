---
project-title: amiibrOS
project-thumbnail: amiibrOS-thumbnail
project-thumbnail-alt: A picture of something
start-date: 2019-05
bg-img: amiibrOS
---

amiibrOS is an electronics/embedded-software summer project started in 2019.

The original goal of the project was to create a retro art display which would
change to reflect an Nintendo Amiibo figure scanned by its built-in scanner.

<video muted width="320" height="240" controls>
  <source src="../assets/vid/amiibrOS-demo.mp4" type="video/mp4">
  Error, your browser does not support the video technology used on this page.
</video>

As time progressed, however, the project turned into a video game console and
the display functionality was implemented as a slideshow app - one of the many
kinds of apps amiibrOS now supports.

At the end of its development time (Summer 2019), the major project goals were
completed with only a few minor polish details left for me to implement someday
later.

## Hardware
The hardware consists of:
* [Raspberry Pi 3B+](https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/)
used to run amiibrOS system software.
* [PN532 Breakout Board](https://www.adafruit.com/product/364) for scanning NFC
tags embedded within Nintendo Amiibo figures.
* LTN170X2-L02 LCD screen salvaged from an old Gateway laptop.
* LTN170X2-L02 LCD compatible controller board such as
[this one from Amazon](https://www.amazon.com/NJYTouch-M-NT68676-2A-LTN170X2-L01-LTN170X2-L02-LTN170X2-L03/dp/B01F8RXIIA/ref=pd_sbs_421_1/131-1769298-7112456?_encoding=UTF8&pd_rd_i=B01F8RXIIA&pd_rd_r=d3c9421d-74dc-11e9-8016-4b75b3288f34&pd_rd_w=nXCjS&pd_rd_wg=oDnjZ&pf_rd_p=588939de-d3f8-42f1-a3d8-d556eae5797d&pf_rd_r=C5BX3PS617PSJ7X79KVV&psc=1&refRID=C5BX3PS617PSJ7X79KVV)
* Custom buck converter. Info on this custom buck converter will be available
in a future post, but buying and modifying a cheap one that can supply 3A+ is
good too.
* 12V 3A power adaptor. I used one with a 5.5mm jack output.
* Power switch fashioned from a N.O. Push Button switch, jumper cables, and
Lego.

I also played around with bluetooth and was able to get an
[8Bitdo N30 Pro 2](https://www.8bitdo.com/n30pro-2/) to work. A tutorial for
getting bluetooth controllers to work with amiibrOS will be available soon.

<img src="../../assets/img/amiibrOS-enclosure.jpg"
  alt="Enclosure made of Lego">

An enclosure was built out of Lego hastily, but it holds together nicely with a
new technique I found for locking in PCBs and perfboards. I will be posting
more on this soon.

## Software
The main part of the amiibrOS project was its system software - dubbed
"amiibrOS". The software would run on a custom, minimal Linux built via
[Buildroot](https://github.com/buildroot/buildroot). There are several software
components, including:
* amiibrOS main system software coded in C with interface using
[Raylib](https://github.com/raysan5/raylib) graphics library.
* Python program for scanning NFC and using a pipe to communicate to amiibrOS
main system software.
* Python program launched via init.d to monitor the GPIO connected to the power
switch.
* Optional slideshow application coded in C also using Raylib.
* A fork of Buildroot containing a default configuration for building amiibrOS
automatically.

All of the software can be found at the GitHub project:
<https://github.com/jpyankel/amiibrOS>

## Relevant Posts
A list of relevant posts concerning amiibrOS can be found below:
{% include related-posts.html %}
