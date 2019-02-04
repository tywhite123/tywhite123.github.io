---
layout: post
title: "Stage 3 Dissertation: GPU Cloth Simulation"
date: 2019-01-29
---

## Intro
For my Stage 3 dissertation I wanted to something physics related, so I got suggested to model how softbodies worked and model that by doing a Cloth Simulation. This ended up being a very intresting project. 

## Technologies Used:
* NCLGL: The graphics framework I used for this project.
* CUDA: Since this was a GPU simulation I had to use some technology for writing GPU programs. For this I decided to use CUDA.
* C++: To program this simulation I used C++.

## Implementation
To implement this cloth simulation, I first needed a mesh that could be used as the graphical representation of the cloth. For this I had to work to get a heightmap that used Index buffers working. This meant I could have a big mesh with lots of vertices, as each vertex was to be a node/particle on the cloth. The next step after that was to start writing the physical representation of the cloth. This was the harder part as it meant I needed to learn CUDA. With CUDA I had to map the vertices of the cloth to a CUDA resource and then use those vertices. Once the vertices were loaded in I wrote a couple of functions (or kernels in CUDA) to handle the physics of the cloth, this involved a function which would handle the springs that connected each of the nodes and one to handle the wrapping of the cloth around the sphere.

## Results
From this simulation I found that if the cloth had more vertices then the more realistic it would look, but would take more time to render the frame. Since I was using CUDA to run the cloth physics on the GPU it meant that there wasn't much of a time difference between the increases in vertices as the kernel was running the updating of the vertices in parellel as it runs on the shader cores of the GPU.

## What to Improve
The main thins to improve upon in my project is to stiffen the springs a bit more, becuase the springs are not stiff enough at the moment. This means the cloth keeps stretching around the ball and eventually falls through the ball as the gap between vertices gets too big. This can be fixed by slightly changing the values that handle the stiffness of the springs.

## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/oeZKX6Ec6zo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
