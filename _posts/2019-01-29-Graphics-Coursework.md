---
layout: post
title: "Graphics Coursework"
date: 2019-01-29
---

## Intro
This coursework involved creating a renderer using NCLGL (Necastle Uni's OpenGL Framework), and then using that renderer to create 3 scenes that would show off multiple different graphical features. 

## Graphics Features
For this coursework I implemented multiple graphical features into my three scenes:
* Scene 1
    * Heightmap Mesh: I created a function that would read in heightmap data from a JPG image so that I could then have a heightmap in one of my scenes.
    * Water: I used a flat heightmap with a semi-transparent texture for this and then applied a few sine wave and cosine waves to it to make it look like basic water. This made the scene look like it had a river.
    * Particles: I created a particle system for this scene as well. The particles I decided to create was snow particles as this was fairly easy to model.
    * Terrain Textures: For the heightmap texture I used a shader which would create a mix of a rock texture and grass texture depending on the direction of the normal for that polygon. I then also added a time factor which would then mix the grass texture and the colour white so that over time it would look like the snow is setting on the ground or melting.
* Scene 2
    * OBJ Mesh: I used a mesh from Spyro 2 to add in an OBJ Mesh into the scene.
    * Tessalated Water: The water i used in this scene was a set of 4 quads which had each been tessalated to have more polygons and then I applied a sine wave so that it looked more water like.
    * Directional Lighting: For this scene I used to directional lighting by just using the normalised direction vector as the direction for the light rather than a position as this then allowed me to have a sun in the scene.
* Scene 3
    * Skeletal Animation: I used some hellknight meshes from Doom and using them to have some form of animation in one of my scenes. I used the walking animation we were provided with for this scene and then made it so that at the end of the animation the world transform was updated, so that it looked as if they were marching along. I also used a hardware skinning vertex shader to do the skinning for this mesh, this meant that I could have more hellknights in the scene as all the skinning was being done on the GPU rather than the CPU.
    * Shadows: For this scene I had a shadow map that I rendered before the actual scene and then used that shadow map to work out what would be in shadows every frame.
* All Scenes
    * Post Processing: I made lots of different post processing effects for this project. The effects I made was a blur effect, a bloom effect, a sobel filter (edge detection), inverted colour effect and a greyscale effect. I used a enum variable to change what effect was turned on, which the value would change based on what num pad number the user pressed.
    * Split Screen: I also added a split screen effect into my renderer which would render all 3 scenes at the same time, and place each one in 3 corners of the scene. I used 3 different camera to get this effect.
    * Skybox: I used a different skybox in each of the 3 scenes. I picked a different skybox based on what would go with the content in each scene.

## Ways to improve:
* The graphics demo could do with using a multidirectional shadow map so that I can have multiple shadows based on multiple lights in one scene.
* Deferred Rendering was a technique I didn't have enough time to implement in to this demo, but would make for a new scene in this demo.


## Youtube Vid
<iframe width="560" height="315" src="https://www.youtube.com/embed/1-rdsH3Wiv0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>