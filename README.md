# Confidence-Guided Hybrid Document Scanning with Shadow-Aware Enhancement

This repository contains the implementation for the project **Confidence-Guided Hybrid Document Scanning with Shadow-Aware Enhancement for Smartphone-Captured Documents**.

The project compares several classical document scanning pipelines for smartphone-captured document images. The goal is to detect the document region, correct perspective distortion, reduce uneven illumination, and improve readability.

## Compared Methods

The following methods are implemented and compared:

1. Contour-based scanner with Otsu thresholding
2. Hough-line-based scanner with adaptive thresholding
3. Adaptive-mask contour scanner
4. Proposed confidence-guided hybrid scanner with Lab luminance normalization

## Dataset

The experiment was performed on six real smartphone-captured document images. The images include perspective distortion, shadows, non-uniform illumination, and textured background clutter.

## Metrics

The following metrics are reported:

* document detection success
* text-to-background contrast
* OCR confidence
* runtime per image
* internal confidence score

## How to Run

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```text
Smart_Document_Scanner_Experiments_Colab_FIXED.ipynb
```

Then run all cells in Google Colab or Jupyter Notebook.

## Main Result

The proposed hybrid method achieved full detection success on the six-image custom dataset and improved OCR confidence and text-to-background contrast compared with the Hough-only baseline. However, the adaptive-mask baseline achieved the highest OCR confidence in this small experiment. Therefore, the proposed method is best interpreted as a balanced and explainable pipeline rather than an absolute winner across all metrics.

## Reproducibility

The notebook contains the full experimental pipeline, including preprocessing, document detection, perspective correction, image enhancement, metric calculation, and result visualization.
# confidence-guided-document-scanner
