# CVL-Thresholding-DIBCO

Computer Vision project for evaluating document image thresholding methods under non-uniform illumination using the H-DIBCO dataset.

This project compares a global thresholding method, **Otsu**, with two local thresholding methods, **Bradley–Roth** and **Sauvola**, on handwritten document images from H-DIBCO 2016 and H-DIBCO 2018.

## Project Overview

Document image binarization converts a grayscale document image into foreground and background regions.

Global thresholding methods such as Otsu use a single threshold value for the entire image. This approach is simple and efficient, but its performance may decrease when illumination varies across the document.

Local thresholding methods such as Bradley–Roth and Sauvola calculate thresholds based on local image statistics, allowing them to adapt better to uneven illumination.

This project investigates:

1. How does non-uniform illumination affect the performance of Otsu, Bradley–Roth, and Sauvola?
2. To what extent do local thresholding methods outperform global thresholding?
3. Under what conditions can local thresholding methods still fail?

## Dataset

The experiment uses two public handwritten document image binarization datasets:

- H-DIBCO 2016
- H-DIBCO 2018

The experiment uses:

- 10 images from H-DIBCO 2016
- 10 images from H-DIBCO 2018
- 20 images in total

Each document image is accompanied by a binary ground-truth image.

The dataset contains natural document degradation such as:

- Paper texture
- Stains
- Bleed-through
- Low-contrast handwriting
- Uneven background intensity

The dataset is automatically downloaded inside the notebook.

## Methods

### 1. Otsu Thresholding

Otsu is used as the global thresholding baseline.

The method selects a single threshold by maximizing the between-class variance of foreground and background pixels.

A single threshold is applied to the entire document image.

### 2. Bradley–Roth Thresholding

Bradley–Roth is an adaptive thresholding method based on the local mean intensity.

For every pixel, the intensity is compared with the mean intensity of its surrounding window.

The implementation uses a local window size of:

```text
41 × 41 pixels
