---
layout: page
title: Seam Carving
description: Implement a content-aware image resizing algorithm
img: /assets/img/sc_h_2.png
importance: 3
category: course proj
---

Discovered in 2007, seam-carving is an elegant content-aware image resizing technique where the image is reduced in size by one pixel of height/width at a time. A vertical seam in an image is a path of pixels connected from the top to the bottom with one pixel in each row, while a horizontal seam is a path of pixels connected from the left to the right with one pixel in each column.

Unlike standard content-agnostic resizing techniques (such as cropping and scaling), seam carving **preserves the most interest features** (aspect ratio, set of objects present, etc.) of the image by calculating and removing seams with less energy.


<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seamcarving-HJoceanSmall.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seamcarving-HJoceanSmall357x285.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The left is the original 505-by-287 pixel image; the right is the result after removing 150 vertical seams, resulting in a 30% narrower image.
</div>

To implement the algorithm, we did energy calculation (Dual-Gradient Energy Function), seam identification, and seam removal. The problem is reduced to a shortest path problem that we could solve using Dijkstra's algorithm, or A* (star) search algorithm, with appropriately preprocessing and postprocessing the input/output data.

Run the algorithm implemented on the photos I took.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_h_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_h_2.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_h_3.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    seamcarving horizontally
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_v_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_v_2.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sc_v_3.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    seamcarving vertically
</div>
