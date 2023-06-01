---
layout: default
title: "PolyDiffuse: Polygonal Shape Reconstruction via Guided Set Diffusion Models"
---

# Abstract

<div>
	<img width="900" src="assets/img/teaser.png" class="center"> 
</div>>

This paper presents *PolyDiffuse*, a novel structured reconstruction algorithm that transforms visual sensor data into polygonal shapes with Diffusion Models (DM), an emerging machinery amid exploding generative AI, while formulating reconstruction as a generation process conditioned on sensor data. 
The task of structured reconstruction poses two fundamental challenges to DM: 1) A structured geometry is a "set" (e.g., a set of polygons for a floorplan geometry), where a sample of \( {N} \) elements has \( {N!} \) different but equivalent representations, making the denoising highly ambiguous; and 2) A "reconstruction" task has a single solution, where an initial noise needs to be chosen carefully, while any initial noise works for a generation task.
Our technical contribution is the introduction of a Guided Set Diffusion Model where 1) the forward diffusion process learns *guidance networks* to control noise injection so that one representation of a sample remains distinct from its other permutation variants, thus resolving denoising ambiguity; and 2) the reverse denoising process reconstructs polygonal shapes, initialized and directed by the guidance networks, as a conditional generation process subject to the sensor data. We have evaluated our approach for reconstructing two types of polygonal shapes: floorplan as a set of polygons and HD map for autonomous cars as a set of polylines. Through extensive experiments on standard benchmarks, we demonstrate that PolyDiffuse significantly advances the current state of the art and enables broader practical applications.



# Method Overview


<div>
	<img width="900" src="assets/img/method_figure.png" class="center"> 
</div>>

<p>
<strong>(a)</strong>. The overall architecture of HEAT, which consists of three steps: 1) edge node initialization; 2) edge image feature fusion and edge filtering; and 3) holistic structural reasoning with two weight-sharing Transformer decoders.  <strong>(b)</strong>. The image feature fusion module for edge nodes. <strong>(c)</strong>. The edge Transformer decoder. For the geometry-only (geom-only) decoder, \( {f} \) is replaced by \( {f}_{coord} \) and the image feature fusion module (gray part) is discarded.
</p>


# Paper

<div>
	<a href=".">
	<img class="thumbnail" src="assets/img/thumbnail.png"> 
	</a>
</div>>

<div class="text-center">
	<a href="assets/paper.pdf"> Download PDF </a> &nbsp; &nbsp; <a href="https://arxiv.org/abs/2111.15143"> Arxiv </a> &nbsp; &nbsp; <a href="assets/supp.pdf"> Supplementary </a> &nbsp; &nbsp; 
	<!-- <a href="assets/poster.pdf"> Poster </a> -->
</div>

<br>
<div class="bibtex-box">
	<strong>@InProceedings{</strong>chen2022heat,
	<br>
	&nbsp;&nbsp;&nbsp;&nbsp; title={HEAT: Holistic Edge Attention Transformer for Structured Reconstruction}, 
	<br> 
	&nbsp;&nbsp;&nbsp;&nbsp; author={Jiacheng Chen, Yiming Qian, Yasutaka Furukawa},
	<br> 
	&nbsp;&nbsp;&nbsp;&nbsp; booktitle={IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	<br> 
	&nbsp;&nbsp;&nbsp;&nbsp; year={2022}<br><strong>}</strong>
</div>


<!-- # Video

<div>
<iframe width="820" height="492" src="https://www.youtube.com/embed/0R5Le2lJw-4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div> -->


# Code / Pre-trained Models

Our code and pre-trained models are available on our [Github repo](https://github.com/woodfrog/poly-diffuse).


# Acknowledgement

This research is partially supported by NSERC Discovery Grants with Accelerator Supplements and DND/NSERC Discovery Grant Supplement, NSERC Alliance Grants, and John R. Evans Leaders Fund (JELF). We thank the Digital Research Alliance of Canada and BC DRI Group for providing computational resources.
