# Notebook examples

This folder contains the runnable companion notebooks for *An Imaging Primer for Ecologists*.

## Index

1. [`01_color_calibration.ipynb`](01_color_calibration.ipynb) — color calibration workflows for still images and video.
2. [`02_lens_correction.ipynb`](02_lens_correction.ipynb) — camera/lens undistortion for images and trajectories.
3. [`03_perspective_rectification_and_scale.ipynb`](03_perspective_rectification_and_scale.ipynb) — perspective correction and pixel-to-unit scaling with reference objects.
4. [`04_acquisition_metadata_checklist.ipynb`](04_acquisition_metadata_checklist.ipynb) — acquisition planning, file naming, metadata, and quality-control checklist.

The notebooks use synthetic examples where possible, so they can be opened and tested without private data. Reusable calibration targets live in [`../assets/calibration_targets`](../assets/calibration_targets).

## Setup and execution

Follow the [root setup instructions](../README.md). Use **Restart Kernel and Run All Cells** to execute a notebook from a fresh kernel. Notebooks 01–04 use synthetic data or metadata templates; no private recording is required. The [Figure 4 notebook](../figure/README.md) uses bundled real tracking data and its background image.

Notebook 01 generates a short sample video and a corrected copy under `notebook_outputs/`. For real recordings, disable synthetic mode and supply 24 measured chart-patch centers. The overlay must match the physical target. This is an illustrative encoded-RGB calibration, not a validated spectral/RAW/HDR workflow. GUI guides link to official illustrated documentation rather than relying on missing screenshots.

Notebook 02 uses example calibration parameters; replace these for your own camera. Notebook 03 assumes all measurements lie on the calibrated reference plane. Notebook 04 prints a metadata template and does not write files by default.

## Validation environment

The dependency ranges in `requirements.txt` allow installation on compatible Python versions. Validation for the final-proof update uses Python 3.9 with NumPy 2.0.2, OpenCV 5.0.0, Matplotlib 3.9.4, seaborn 0.13.2, nbformat 5.10.4, and nbclient 0.10.2. Other operating systems and codec builds may differ. Run the notebooks in your target environment before analysis.

On 2026-11-06, all five notebooks passed fresh-kernel execution. The color workflow additionally passed translated-chart sampling and invalid-input checks; the generated input and corrected videos both decoded as 12 frames at the expected dimensions. Local documentation links and embedded proof-URL coverage were checked. Live external-link checks found publisher access restrictions and timeouts, so availability of every external site is not guaranteed.
