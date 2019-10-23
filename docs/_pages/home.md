---
layout: page
title: gradSLAM - Dense SLAM meets Automatic Differentiation
date: 2019-10-23
permalink: /
---

### Abstract

> <span style="font-size:0.7em;"> The question of "representation" is central in the context of dense simultaneous localization and mapping (SLAM). Newer learning-based approaches have the potential to leverage data or task performance to directly inform the choice of representation. However, learning representations for SLAM has been an open question, because traditional SLAM systems are not end-to-end differentiable. </span> 
> <span style="font-size:0.7em;">In this work, we present gradSLAM, a differentiable computational graph take on SLAM. Leveraging the automatic differentiation capabilities of computational graphs, gradSLAM enables the design of SLAM systems that allow for gradient-based learning across each of their components, or the system as a whole.
This is achieved by creating differentiable alternatives for each non-differentiable component in a typical dense SLAM system. Specifically, we demonstrate how to design differentiable trust-region optimizers, surface measurement and fusion schemes, as well as differentiate over rays, without sacrificing performance. This amalgamation of dense SLAM with computational graphs enables us to backprop all the way from 3D maps to 2D pixels, opening up new possibilities in gradient-based learning for SLAM. </span>


### Explanatory video

<div style="text-align:center">

Click on the image below, to watch a video that explains what gradSLAM is, and showcases our primary results.

<br/> <br/>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=2ygtSJTmo08
" target="_blank"><img src="http://img.youtube.com/vi/2ygtSJTmo08/0.jpg" 
alt="Click to watch the explanatory video."/></a>

<!-- [![Watch an explanatory video on gradSLAM](http://img.youtube.com/vi/2ygtSJTmo08/0.jpg)](http://www.youtube.com/watch?v=2ygtSJTmo08) -->

</div>

<!-- <div style="text-align:center">

    <img src="{{ site.baseurl }}/images/icpslam.gif" />

</div> -->


### About gradSLAM

gradSLAM is a fully differentiable dense SLAM framework. It provides a repository of differentiable building blocks for a dense SLAM system, such as differentiable nonlinear least squares solvers, differentiable ICP (iterative closest point) techniques, differentiable raycasting modules, and differentiable mapping/fusion blocks. One can use these blocks to construct SLAM systems that allow gradients to flow all the way from the outputs of the system (map, trajectory) to the inputs (raw color/depth images, parameters, calibration, etc.).

Specifically, we implement differentiable versions three classical dense SLAM systems using the gradSLAM framework: KinectFusion, PointFusion, ICP-SLAM. We choose these because
* Each of these approaches sparked a new line-of-research in dense SLAM
* The approaches themselves are fairly simple from an algorithmic standpoint
* We wanted to provide differentiable SLAM solutions for a wide variety of 3D representations (voxels, surfels, points).

<div style="text-align:center">

    <img src="{{ site.baseurl }}/images/header.png" />

</div>

### Qualitative results

The differentiable SLAM systems perform quite similarly to the non-differentiable counterparts, while allowing for gradients to flow right through. This makes gradSLAM attractively poised to be used in gradient-based learning systems.

Here's a comparitive analysis of the three differentiable SLAM systems we provide.

<div style="text-align:center">

    <img src="{{ site.baseurl }}/images/icl.png" />

</div>

More qualitative results, this time, on the ScanNet dataset.

<div style="text-align:center">

    <img src="{{ site.baseurl }}/images/scannet.png" />

</div>

Further, we have evaluated gradSLAM on the TUM RGB-D benchmark, as well as on an in-house sequence captured from an Intel RealSense D435 camera.

<div style="text-align:center">
    <img src="{{ site.baseurl }}/images/tum.gif" />
</div>
<div style="text-align:center">
    <img src="{{ site.baseurl }}/images/mrsd.gif" />
</div>


### Paper

<div style="text-align:center">

A preprint is currently available on arXiv, at the following link. Click on the thumbnail below, to access.

<br/> <br/>
<a href="{{ site.baseurl }}/paper.pdf" target="_blank"><img src="{{ site.baseurl }}/images/paper.png" 
alt="Click to access the preprint."/></a>
</div>


### Citing us

If you would like to cite us, you could use the following BibTeX entry.

```
@article{gradslam,
    author  = { Krishna Murthy, J. and Iyer, Ganesh and Paull, Liam },
    title   = { gradSLAM: Dense SLAM meets Automatic Differentiation },
    journal = { arXiv },
    year    = { 2019 },
}
```


### Code

gradSLAM will be released as an open-source SLAM framework for PyTorch. As the manuscript is currently under review, we are eyeing a release date in the latter half of January 2020.

### Correspondence

If you need to discuss any further, or seek clarifications on implementation detail, correspondence is encouraged to [Krishna Murthy](https://krrish94.github.io), [Ganesh Iyer](https://epiception.github.io/), or [Liam Paull](http://liampaull.ca). Also, we would like to hear more from anyone working on similar ideas.

### More qualitative results

Stay tuned for more gifs!!!

### Acknowledgements

The authors are grateful to the wonderful help from several people, including, but not limited to, [Gunshi Gupta](https://gunshi.github.io), [Ankur Handa](https://ankurhanda.github.io/), [Bhairav Mehta](https://bhairavmehta95.github.io), [Mark Van der Merwe](https://mvandermerwe.github.io/), [Aaditya Saraiya](https://www.ri.cmu.edu/ri-people/aaditya-saraiya/), [Parv Parkhiya](https://www.ri.cmu.edu/ri-people/parv-parkhiya/), [Akshit Gandhi](https://www.ri.cmu.edu/ri-people/akshit-kishor-gandhi/), [Shubham Garg](https://www.ri.cmu.edu/ri-people/shubham-garg/), [Tejas Khot](https://tejaskhot.github.io), [Gautham Swaminathan](https://www.ri.cmu.edu/ri-people/swaminathan-gurumurthy/), [Zeeshan Zia](http://zeeshanzia.com), [Ronald Clark](http://ronnieclark.co.uk), and [Sajad Saeedi](https://www.sajad-saeedi.ca/).
