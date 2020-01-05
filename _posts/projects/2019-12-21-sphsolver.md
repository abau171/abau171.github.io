---
layout: project
category: project
title: SPH Fluid Simulator
thumbnail: /sphthumbnail.jpg
description: Smoothed-particle hydrodynamics (SPH) fluid solver written for GPU. Includes OpenGL viewer with support for GPU-based meshing via Marching Cubes and simple rendering. Capable of real-time (60 FPS) simulation of up to 1 million particles.
---
{% include snippets.html %}

This is a fluid simulation project I built for UCSD's CSE 291 course in Physics Simulation. I wrote an entirely GPU-based smoothed-particle hydrodynamics (SPH) solver, then rendered some results using an early version of my personal rendering project [Dino](/project/dino.html). My solver is written in C++, and uses CUDA for simulation and meshing and OpenGL for the interactive viewer.

{{ gfycatStart }}obeseshortabyssiniangroundhornbill{{ gfycatEnd }}

## Features

- uniform grid spatial acceleration structure
- optional incompressibility constraint using [PCISPH](https://people.inf.ethz.ch/~sobarbar/papers/Sol09/Sol09.pdf)
- meshing using [Marching Cubes](https://en.wikipedia.org/wiki/Marching_cubes)
- real-time viewer with interactive fluid properties
- Wavefront .obj mesh exporter

## Interactive Viewer

The interactive viewer lets watch the simulation unfold in real-time with a controllable camera. Properties such as physics framerate, gravity, and viscosity can be modified and take immediate effect in the simulation. The video below shows a demo of the viewer running on a GeForce 1060 GPU. On a more powerful GeForce RTX 2080 GPU, I achieved consistent 60 FPS simulation and display for up to 1 million particles.

{{ gfycatStart }}recentthriftybrahmanbull{{ gfycatEnd }}
