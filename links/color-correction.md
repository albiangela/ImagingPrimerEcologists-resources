---
layout: default
---

# Color Correction

Color representation changes with light availability due to wavelength-specific
absorption and reflectance, making color calibration essential for studies
involving color quantification, spectral analysis, or differing visual systems.
Calibration typically relies on standardised reference targets (white, gray, or
multi-color palettes such as the X-Rite or Calibrite ColorChecker) to balance
and standardize color levels across images.

For a runnable walkthrough, see the companion notebook
[`01_color_calibration.ipynb`](../notebooks/01_color_calibration.ipynb). A
printable color reference target is available in
[`../assets/calibration_targets`](../assets/calibration_targets).

## Encoding profiles

Images and videos can be recorded with standard or logarithmic (log) encoding
profiles. Standard profiles are optimized for immediate viewing but can lose
detail in highlights or shadows; log profiles compress tonal contrast to
preserve a wider dynamic range (useful under sun glare, shadows, or underwater
light gradients) but require conversion or grading before quantitative analysis.

## General-purpose tools

Tools for color correction and image processing.

| Software | Context | Reference |
|----------|---------|-----------|
| [Adobe Photoshop](https://www.adobe.com/products/photoshop.html) | General image editing | Adobe 2025 |
| [GIMP](https://www.gimp.org) | General image editing (open-source) | The GIMP Development Team 2026 |
| [Darktable](https://www.darktable.org) | General photo workflow (open-source) | darktable developers 2024 |
| [OpenCV (Python)](https://opencv.org/) | Programmatic color correction | Bradski 2000 |
| [imager (R)](https://cran.r-project.org/package=imager) | Programmatic image processing in R | Barthelmé & Tschumperlé 2019 |

## Specialized ecological tools

Tools developed for specific contexts.

| Software | Context | Reference |
|----------|---------|-----------|
| [Sea-Thru](https://github.com/hainh/sea-thru) | Underwater photography (water removal) | Akkaynak & Treibitz 2019 |
| [micaToolbox](https://www.empiricalimaging.com/) | Multispectral and calibrated color analysis | Troscianko & Stevens 2015 |
| charisma | Color calibration for ecological applications | Schwartz et al. 2026 |

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
