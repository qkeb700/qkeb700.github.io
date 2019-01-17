---
layout: project
type: project
image: images/fig13_sm.jpg
title: GIF_Color_Table
permalink: projects/color_table
date: 2019-1-17
labels:
  - Java
  - C++
  - C
  - GitHub
summary: A useful application for changing the original color table of gif file to the new result file.
---

<img class="ui medium right floated rounded image" src="../images/fig13_sm.gif">

GIF employs a variety of ways to store image data. One of them is use of "color table," or a color palette. First, you define an index for each color you will use, e.g., 0 for white, 1 for black, 2 for blue, and so on. Based on this table, you can encode each pixel with the corresponding color index.

Modifying the color table

When you open the GIF file, your computer actually draws the image based on the color palettes in the file. What if we replace them with other palettes? Let's say we hack and modify the color table, and change white (FF FF FF) to black (00 00 00), red (FF 00 00) to cyan (00 FF FF), blue (00 00 FF) to yellow (FF FF 00), green (00 FF 00) to magenta (FF 00 FF). The resulted image from the one above is like this.

In this project, I gained experience with dealing with Image file and got more interested in C++. 
