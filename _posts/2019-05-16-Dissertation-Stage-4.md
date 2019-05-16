---
layout: post
title: "Dissertation Stage 4 - Atmospheric Scattering and Procedural Generation"
date: 2019-05-16
---

## Info
In this project I created an implementation of Atmospheric Scattering and Procedural Generation.

The atmospheric scattering uses a fragment shader which calculates the colour of that fragment based on where the directional light is position in the sky.
Since this is in the shader it is recalculated each frame to display so when the light direction is changed so does the sky.
With it being a shader it also means all of these calculation are done on the GPU and can be done in real time.
It has to be done on the GPU since it needs to work on each individual pixel of fragment.


The procedural generation is a simple perlin noise implementation.
This generated the terrain at the beginning of the application.
The terrain is rougher or smoother depending on the size, as there is a difference in the amount of vertices.

## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/AjCW0mLtiwM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/0jw-vFWxsps" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/_eocpRhb31M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



