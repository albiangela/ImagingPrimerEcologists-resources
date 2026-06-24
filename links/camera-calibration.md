---
layout: default
---

# Camera Calibration

Camera calibration estimates intrinsic parameters (focal length, principal
point, pixel aspect ratio) and extrinsic parameters (position and orientation)
for single- or multi-camera systems, allowing conversion from image space to
physical coordinates. Two main approaches exist: minimizing distortion in-camera
with low-distortion lenses and corrective optics (hardware), or correcting
distortion computationally during post-processing (software).

For a runnable walkthrough, see the companion notebooks
[`02_lens_correction.ipynb`](../notebooks/02_lens_correction.ipynb) and
[`03_perspective_rectification_and_scale.ipynb`](../notebooks/03_perspective_rectification_and_scale.ipynb).

## Hardware Solutions

Many camera and lens combinations produce optically distorted images, primarily
through refraction. The simplest hardware solution is to select a low-distortion
lens; where distortion cannot be avoided, corrective optics can partially
compensate by redirecting light before it reaches the sensor.

## Software Solutions

When hardware solutions are insufficient, computational correction methods
mitigate optical distortions during post-processing. Calibration targets such as
chessboards (with smooth or ArUco/ChArUco boundaries) and calibration wands are
used to estimate parameters. Printable calibration targets are available in
[`../assets/calibration_targets`](../assets/calibration_targets).

## Implementation

Overview of camera calibration software supporting single- and multi-camera
setups. "Partial" multi-camera indicates stereo support but limited native
support for rigs with three or more cameras.

| Software | Calibration Method(s) | Multi-Camera | Best For | Reference |
|----------|-----------------------|:------------:|----------|-----------|
| [multical](https://github.com/oliver-batchelor/multical) | Chessboard calibration | Yes | General-purpose multi-camera lab and field rigs | https://github.com/oliver-batchelor/multical |
| [Anipose](https://anipose.readthedocs.io/en/latest/tutorial.html) | Chessboard or wand calibration | Yes | 3D pose estimation workflows integrated with DeepLabCut or SLEAP | Karashchuk et al. 2021 |
| [Kalibr](https://github.com/ethz-asl/kalibr) | AprilTag-based spatiotemporal calibration | Yes | Camera rigs requiring spatiotemporal calibration | Rehder et al. 2016 |
| [mrcal](https://mrcal.secretsauce.net/) | Chessboard calibration | Partial | High-accuracy applications requiring uncertainty quantification or non-standard lenses | https://mrcal.secretsauce.net |
| [Deep ChArUco](https://github.com/JunkyByte/deepcharuco) | ChArUco detection for underwater images | No | Underwater or low-contrast environments where standard chessboards fail | Hu et al. 2019 |

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
