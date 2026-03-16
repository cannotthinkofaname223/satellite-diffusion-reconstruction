# Satellite Diffusion Reconstruction Demo

## Project Overview

Satellite imagery often suffers from missing or corrupted regions due to cloud cover, sensor failures, or atmospheric interference.
This project explores a **diffusion-style iterative reconstruction method** to recover missing regions in satellite images.

Using images from the EuroSAT dataset, we simulate missing pixels and cloud occlusions, then reconstruct the corrupted regions using an iterative diffusion-based smoothing process.

This project is a small prototype inspired by recent research on **diffusion models for image restoration and satellite data recovery**.

---

## Motivation

Satellite images frequently contain missing information caused by:

* Cloud cover
* Atmospheric noise
* Sensor failures

Recovering missing regions is an important problem in remote sensing and Earth observation.


---

## Dataset

The experiments use the **EuroSAT dataset**, which contains land-use images derived from Sentinel-2 satellite imagery.

Each image is a 64×64 RGB satellite patch representing categories such as:

* farmland
* forest
* residential areas
* industrial areas

---

## Method

The reconstruction pipeline consists of four steps:

1. Load satellite image
2. Simulate missing pixels or cloud occlusion
3. Apply diffusion-style iterative smoothing
4. Evaluate reconstruction quality

The diffusion reconstruction process iteratively smooths missing regions while keeping known pixels fixed.

---

## Experiments

We simulate different levels of missing pixels:

* 10% missing
* 30% missing
* 50% missing

For each scenario we reconstruct the corrupted image and evaluate the reconstruction quality using PSNR.

---

## Example Results

| Original | Masked | Reconstruction |
| -------- | ------ | -------------- |
| image    | image  | image          |

The reconstruction quality decreases as the missing ratio increases, which is reflected by lower PSNR values.

---

## Evaluation Metric

Reconstruction quality is measured using **PSNR (Peak Signal-to-Noise Ratio)**.

Higher PSNR indicates better similarity between the reconstructed image and the original image.

---
