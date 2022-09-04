---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
in_header: false
title: "Home"
---

### Hi! Welcome to my project showcase website :)
### I'm a junior studying Mathematics and Computer Science at Carnegie Mellon University, passionate about combining technology and art to make great things. You can read more about me [here](about.markdown), or scroll down to view my project experience in the following areas:
- Computer Graphics
- Computer Systems
- Game Development
- 3D Animation

---
# **Computer Graphics**
## Scotty3D
[GitHub Repo](https://github.com/CMU-Graphics/Scotty3D) | [Documentation](https://cmu-graphics.github.io/Scotty3D/)

Carnegie Mellon University’s educational graphics software package. Includes components for interactive 3D mesh editing, path tracing, dynamic animation, and physics-based simulation.

[[Read More]](projects/Scotty3D.md)

![15-462 F20 Renders](media/scotty3d/scotty3d-001.png)

## DrawSVG
[GitHub Repo](https://github.com/CMU-Graphics/DrawSVG) | [Documentation](https://github.com/CMU-Graphics/DrawSVG/blob/master/README.md)

A simple software rasterizer that draws basic primitives and bitmap images in a viewer that supports features of the Scalable Vector Graphics (SVG) format.

[[Read More]](projects/DrawSVG.md)

![DrawSVG Pipeline](media/drawsvg/DrawSVG-001.png)

## 3D Video Title Generator
[GitHub Repo](https://github.com/fakeveliu/3D-Video-Title-Generator) | [Video Demo](https://www.youtube.com/watch?v=_HKwtrwD1u4)

An application that generates a 3D title intro for your video with background customization and built-in effects presets.

[[Read More]](projects/3D-Video-Title-Generator.md)

![3DVTG Menu](media/3d-video-title-generator/3DVTG-001.jpg)

---

# **Computer Systems**
These are some of the more challenging projects I did in CMU's Introduction to Computer Systems[^1] course, all of which built up my understanding of essential concepts used in computer systems.

## Malloc Lab
A dynamic memory allocator that efficiently reproduces the `malloc`, `free`, `realloc`, and `calloc` library functions. My task in this lab was to write these function from scratch to satisfy some performance benchmarks, which required a relatively good grasp of the low-level memory layout. 

The starter code used a single implicit list to manage the data blocks, which has a very low throughput (average number of operations completed per second). To combat this, I implemented a segregated explicit lists data strucutre where free blocks are kept in buckets according to their sizes. This greatly shortens the searching time because (1) the program only needs to traverse the one bucket corresponding to the size `malloc` asks for, rather than go through all the free blocks, and (2) every bucket is a doubly-linked list containing only the free blocks.

However, this is not enough to produce a high utilization (peak used memory to heap size ratio) due to fragmentation. This is addressed by decreasing the minimum block size and removing overheads in each block. The final solution increases utilization by 16% and has 10x better throughput compared to the initial implemenation.

## Shell Lab
A simple Linux shell program `tsh` that supports basic job control and I/O redirection. Each command is either a path to an executable (e.g. `tsh> /bin/ls`) or a built-in command that has special meaning to the shell (e.g. `tsh> quit`). Excecutables are run in child processes while built-in commands are run in the shell's own process. The shell manages a job list where each job is either a foreground job or a background job, the difference being that the shell only waits for a command to terminate if it's a foreground job. The shell also responds to `Ctrl-C` or `Ctrl-Z` by interrupting or stopping the entire foreground process group accordingly.

A must-have for implementing all of these is an extensive understanding of signals. Writing the 3 required signal handlers (`SIGCHLD`, `SIGINT`, and `SIGTSTP`) taught me a lot about how they interact with the processes exactly and when to block them to avoid race conditions.
## Proxy Lab
A concurrent Web proxy that sits between local browsers and the rest of the World Wide Web.

[^1]: As per the academic integrity policy at CMU, the source code is not to be disclosed here.

---

# **Game Development**
## CapeGuy
[GitHub Repo](https://github.com/fakeveliu/CapeGuy) | [Gameplay Video](https://www.youtube.com/watch?v=tRJ_BaRIuRc)

A 2D platformer adventure game. Along the journey, the player controls CapeGuy to fight enemies in the forest and collect coins to unlock new levels.

![CapeGuy](media/capeguy/capeguy-001.png)

---

# **3D Animation**
## Dreamwriter
[Showcase Video](https://www.youtube.com/watch?v=1fceOg6SGZs)

A short 3D animation film in which I was responsible for everything in the pipeline from character design, storyboarding, 3D modeling, rigging, to animation. [[Read More]](projects/Dreamwriter.md)

![Dreamwriter Render](media/dreamwriter/dreamwriter-001.jpeg)

---