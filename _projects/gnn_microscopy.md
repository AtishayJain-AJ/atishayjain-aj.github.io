---
layout: page
title: Large Image Segmentation with GNN
description: Memory Efficient Semantic Segmentation of Large Microscopy Images Using Graph-based Neural Networks
img: assets/img/GNNLarge.jpg
importance: 2
#category: work
#giscus_comments: true
---

This project is a graph neural network (GNN)-based framework applied to large-scale microscopy image segmentation tasks. While deep learning models, like convolutional neural networks (CNNs), have become common for automating image segmentation tasks, they are limited by the image size that can fit in the memory of computational hardware. In a GNN framework, large-scale images are converted into graphs using superpixels (regions of pixels with similar color/intensity values), allowing us to input information from the entire image into the model. By converting images with hundreds of millions of pixels to graphs with thousands of nodes, we can segment large images using memory-limited computational resources. We compare the performance of GNN- and CNN-based segmentation in terms of accuracy, training time, and required graphics processing unit (GPU) memory. Based on our experiments with microscopy images of biological cells and cell colonies, the GPU-based segmentation used one to three orders-of-magnitude fewer computational resources with only a -2% to +0.3% change in accuracy. Furthermore, errors due to superpixel generation can be reduced by either using better superpixel generation algorithms or increasing the number of superpixels, thereby allowing for improvement in the GNN framework's accuracy. This tradeoff between accuracy and computational cost over CNN models makes the GNN framework attractive for many large-scale microscopy image segmentation tasks in biology.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/GNNLarge.jpg" title="GNN Framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    a. An illustration of the process of generating nested graphs from an input ST sample that contains the spatial coordinates and gene expression values for all the spots in the sample. STING inputs these nested graphs to its GNNs. i) STING applies k-means to the spatial information of the input to obtain spot regions. ii) It then uses these spot regions and input gene expression values to generate spot-level gene-gene relation graphs. Finally, the framework uses the input spatial information and the gene-gene relation graphs to create a nested graph that represents the entire input sample. b. An overview of the STING framework. (1) STING generates spatial regions of spots in the sample. It then calculates gene co-expression matrices per region. (2) STING uses the edges from the co-expression matrices and features from gene expression inputs to create spot-specific graphs (3) that it feeds to the inner GNN. (4) The framework uses the inner GNN outputs as node features and spatial information as edges in a sample-level graph. (5) It then uses these graphs to train the outer GNN, which aims to (6) reconstruct the original gene expression values.
</div>


[GitHub](https://github.com/rsinghlab/gnn_microscopy_segment), [Publication](https://academic.oup.com/jmicro/article-abstract/73/3/275/7326526)