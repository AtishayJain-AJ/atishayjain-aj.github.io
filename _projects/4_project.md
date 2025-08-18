---
layout: page
title: Evaluating Methods of Classifying and Segmenting Point Clouds
description: Point Cloud Segementation using Graph Neural Networks and Auto-Encoders
img: assets/img/cv_poster.jpg
importance: 4
#category: work
---
In this project, we tested graph neural network (GNN) and auto-encoder models to the state-of-the-art PointNet method. We compared them on a point cloud segmentation task using the accuracy metric. We also compared their computational requirements such as GPU memory and time taken to train. We noted that the simple GNN method had slightly worse performance compared to PointNet in exchange for lower training time, but had higher memory requirements. However, the auto-encoder performed worse than the GNN.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cv_poster.jpg" title="Computer Vision Poster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This project was part of the 1430 Computer Vision course.