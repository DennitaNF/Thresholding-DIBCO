# CVL_Assignment02 - Thresholding DIBCO

This repository contains the implementation of **Image Thresholding** techniques for the Advanced Computer Vision course.

The project evaluates several document image binarization methods on handwritten document images from the **H-DIBCO 2016** and **H-DIBCO 2018** datasets under different illumination conditions.

## Methods

The thresholding techniques implemented in this project include:

- Otsu Thresholding
- Bradley-Roth Adaptive Thresholding
- Sauvola Thresholding

Otsu is used as a global thresholding baseline, while Bradley-Roth and Sauvola use local image statistics to produce adaptive thresholds.

## Evaluation

The results are evaluated using three standard document binarization metrics:

- **F-measure**
- **PSNR (Peak Signal-to-Noise Ratio)**
- **DRD (Distance Reciprocal Distortion)**

The experiment also applies different levels of synthetic non-uniform illumination to evaluate the robustness of each thresholding method.

## Files

- `CVL_Thresholding_DIBCO.ipynb` — main implementation notebook
- `Tugas_CVL_Laporan_Thresholding_Dennita_Noor_Febianty.pdf` — assignment report containing the experiment, analysis, and results

## Summary

The experiment shows that different thresholding methods respond differently to illumination changes:

- Otsu performs well when foreground and background intensities are clearly separated.
- Bradley-Roth is more robust to non-uniform illumination because it uses local mean intensity.
- Sauvola adapts to both local intensity and local contrast.
- Local thresholding methods are generally more stable than Otsu under strong illumination variation.
- Local methods can still fail on thin and low-contrast handwriting.

The results show that there is no single thresholding method that is optimal for all document conditions.

## Author

**Dennita Noor Febianty**
