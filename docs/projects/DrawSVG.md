---
layout: page
title: DrawSVG
permalink: /DrawSVG/
in_header: false
---
> A simple software rasterizer that draws basic primitives and bitmap images in a viewer that supports features of the Scalable Vector Graphics (SVG) format.

DrawSVG is a project I did in the course Computer Graphics at CMU that utilizes important concepts in modern 2D rendering pipelines such as rasterization, sampling, perspective projection, depth and transparency, and so on.

## Rasterization ##
To draw basic primitives in the viewport, I implemented the following functions:
* `rasterize_line()`, which converts non-integer vertex coordinates into screen sample positions and uses the Bresenham's Algorithm to draw lines of any slope on the screen. In terms of efficiency, it only considers the sample positions covered by the line rather than the entire canvas which takes much more work.
* `rasterize_triangle()`, which tests all the sample points in the bounding box of a triangle and uses cross products to check for triangle coverage.

(image for rasterization)

## Supersampling ##

## Transformations ##

## Image Elements ##

## Alpha Compositing ##