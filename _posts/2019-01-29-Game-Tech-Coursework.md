---
layout: post
title: "Game Tech Coursework"
date: 2019-01-29
---

## Intro
For this coursework I had to create a golf game, similar to Golf With Your Friends on Steam. The main learning outcomes for this coursework was to learn how to write a physics engine, how game physics work, AI (State Machines and Pathfinding) and networking. The coursework was split into two parts, first part was Physics and the second part involved AI and Netowrking.

## Framework
The framework that we used for this peice of coursework involved filling in the functions for the physics engine and creating a networking subsystem from scratch. The networking part of this framework involved using enet to setup a server class and a client class and then creating packets to send between them. 

## Game
From this framework, once everything had been filled in, I had to build a golf game. This involved making a singleplayer version in which the player would play through a couple of courses and then if they beat a course it would progress them to the next one and display their score for that course. 

The second part of this involved making a networked multiplayer version of the game. For this I created a seperate server executable which meant that the clients would just be clients that would connect to one dedicated server. The server ran the physics engine and would then send position and orientation updates every frame, while the clients would send ray casting data for applying a force on the server for that clients ball. 

## Ways to improve:
* For this coursework the main way to improve it would be to get multiple player balls on the server when multiple players join. At the moment the game just allows all connected players to control the same ball, which does create a fun cooperative multiplayer golf mode. But it would be better to also have seperate balls for each player.

## Video 
<iframe width="560" height="315" src="https://www.youtube.com/embed/LsIYmMvf21A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
