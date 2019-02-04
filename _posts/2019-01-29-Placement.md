---
layout: post
title: "Summer Placement at Teledyne"
date: 2019-01-29
---

## Intro
During this placement at Teledyne Defence and Space, I mostly worked on two projects. The first was a program to extract data (from Radio Frequency Filters) from CSV files to place in a table. The second was to write a tool which would convert a graphical file format from a pre AutoCAD format to an AutoCAD format.

## Filter Extraction Program
This program was built using C++, the purpose of the program was to take data from a CSV file, where the data had been recorded from tests of RF Filters. This program read the data in for a selected Filter type (Bandpass, Highpass or Lowpass), and place that data into a table. The data was put into a table like this because in its current format it wasn't very readable for customers. Since the data was in a table it could then be copied and pasted into excel to produce graphs based on a certain attribute of the filter.

## DrawboxToDXF Conversion Tool
The second tool I had to build was a tool that would convert a file format from a program called Drawbox which was a tool that was used at the company for designing RF Filters before AutoCAD was used. This meant I had to learn what each part of the file format was for, what each number meant. This mean plotting coordinates on a graph in excel. After each part of the file was figured out, I made the program to read this in. The first part was to make a file reader that would read in all of this data and then create shapes in an OpenGL window. The purpose of the OpenGL window was to allow the user to then decide what layer they wanted to put that shape on. After this I had to learn how AutoCAD file formats worked and then pick the one that was most useful for the Engineers to use in AutoCAD, this ended up being DXF.