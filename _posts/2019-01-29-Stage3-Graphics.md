---
layout: post
title: "Stage 3 Graphics: Shaders"
date: 2019-01-29
---

## Intro
For this coursework I had to do some shader programming to add different effects to a cube mesh that was spinning on screen. This meant I had to use a variety of different shaders, for example vertex, fragement, geometry and tessalation shaders. 

## Shaders
* Shader 1: this shader was just a shader which allowed for the cube to get smaller over time.
* Shader 2: this shader allowed for a cube to become more transparent over time, to do this I reduced the alpha value over time.
* Shader 3: this shader was for blending two textures together so over time the cube would change from being rocky to more mossy.
* Shader 4: this shader was a geometry shader that split the cube into 4 smaller cubes and then moved them further away.
* Shader 5: this shader was a lighting shader which would change the colour of the light. This was done using a sine wave and a time value.
* Shader 6: this shader was a geometry shader which would change the cube into points and then add some value on each axis depending on a time value that would make the cube look like it was vibrating.


## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/cHI1GJuOFwY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>