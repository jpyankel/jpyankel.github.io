---
title: amiibrOS Arcade
startdate: 2020-07-01
enddate: 2020-09-01
tags: ['amiibrOS']
---

# Project Overview
amiibrOS is an electronics/embedded-software summer project started in 2019. This page showcases the
updates to amiibrOS developed in 2020 - titled "amiibrOS Arcade". See the [original project](https://jpyankel.github.io/projects/amiibrOS.html) for the original hardware and project background.

<img src="/assets/img/amiibrOS/amiibrOS_arcade_front.jpg"
  alt="New amiibrOS Arcade hobby project front view"

<img src="/assets/img/amiibrOS/amiibrOS_arcade_back.jpg"
  alt="amiibrOS Arcade back view"

<img src="/assets/img/amiibrOS/amiibrOS_arcade_internal.jpg"
  alt="amiibrOS Arcade showing electronics and other components"

{% include youtubePlayer.html id="FAwBiTkSlRw" %}

## New Features
* Wooden bartop arcade cabinet I designed in Autodesk Fusion 360. 3D model viewer here:
https://a360.co/2VPVUB3
* [Raspberry Pi 4B](https://www.raspberrypi.org/products/raspberry-pi-4-model-b), upgraded from the
original version's 3B+.
* My custom PCB which distributes power to different components of the system. Steps down 12V to 5V
using an [LM2678T-ADJ](https://www.ti.com/lit/ds/symlink/lm2678.pdf), and has terminals for a 5V RPI
USB-C [breakout board](https://www.sparkfun.com/products/15100), 12V LCD, audio AMP, and two
(optionally GPIO-controlled) fans. See the 3D model [here](https://a360.co/3hNxQY5). View the
schematic [here](https://jpyankel.github.io/assets/img/amiibrOS/pm_board_schematic.png) and board
layout [here](https://jpyankel.github.io/assets/img/amiibrOS/pm_board_layout.png).
* Reworked system software ported from C Raylib to Python Pygame. This will make it easier to
maintain and add more features in the future. You can find all of the sotware at the GitHub project:
<https://github.com/jpyankel/amiibrOS>
* [Class D audio amp board]() which amplifies stereo audio from the RPIs headphone jack.
* Two sets of mid-range speakers taken from an old TV.
* An swappable arcade joystick panel with an 8-button and joystick layout inspired by
https://www.slagcoin.com/joystick/layout.html. The buttons and joystick were obtained from a [kit](https://www.amazon.com/Hikig-Encoders-Joysticks-Buttons-Raspberry/dp/B07JF34XPB/ref=sr_1_7?dchild=1&keywords=joystick+and+buttons+kit&qid=1626635167&sr=8-7)
which also includes a USB encoder.
