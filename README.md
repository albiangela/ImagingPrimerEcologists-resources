# BehavioralVideoAnalysis

This repository is a **tutorial / read-more companion** for the paper
*An Imaging Primer for Ecologists* (Francisco, Bennett-Smith, Albi, Walter, Koger, Sridhar; in prep.).

It collects curated links and step-by-step Jupyter notebooks for ecologists
working with images and video.

## Repository layout

```text
links/          curated links — paper, tools, datasets, background reading
notebooks/      step-by-step guides and Jupyter notebooks
assets/         reusable notebook assets such as printable calibration targets
examples/       small example settings and metadata files for notebooks
```

## Start here

1. **Browse `links/`** for a curated collection of calibration tools, tracking
   software, and background references:

   **Multi-camera systems and calibration**
   - [`links/synchronization.md`](links/synchronization.md) — camera synchronization methods
   - [`links/camera-calibration.md`](links/camera-calibration.md) — intrinsic/extrinsic calibration tools (multical, Anipose, mrcal …)
   - [`links/color-correction.md`](links/color-correction.md) — color correction pipelines and tools

   **Data processing**
   - [`links/tracking.md`](links/tracking.md) — animal tracking software (TRex, SLEAP, DeepLabCut …)
   - [`links/photogrammetry.md`](links/photogrammetry.md) — photogrammetry and 3D reconstruction
   - [`links/data-analysis.md`](links/data-analysis.md) — downstream data analysis tools

   **Case studies**
   - [`links/case-studies.md`](links/case-studies.md) — worked examples from published studies
   - [`links/detection.md`](links/detection.md) — 2D object detection and animal tracking
   - [`links/georeferencing-drones.md`](links/georeferencing-drones.md) — aerial imaging with drones
   - [`links/satellite-imagery.md`](links/satellite-imagery.md) — large-scale satellite imagery

2. **Open `notebooks/`** for practical, worked examples:
   - [`01_color_calibration.ipynb`](notebooks/01_color_calibration.ipynb) —
     color calibration walkthroughs for still images (Lightroom, GIMP) and video
     (DaVinci Resolve, Final Cut Pro, ffmpeg), plus a runnable Python/OpenCV pipeline
   - [`02_lens_correction.ipynb`](notebooks/02_lens_correction.ipynb) —
     lens distortion correction with OpenCV, including trajectory undistortion
   - [`03_perspective_rectification_and_scale.ipynb`](notebooks/03_perspective_rectification_and_scale.ipynb) —
     perspective rectification and pixel-to-real-world scaling from reference points
   - [`04_acquisition_metadata_checklist.ipynb`](notebooks/04_acquisition_metadata_checklist.ipynb) —
     acquisition planning, metadata capture, and field/lab checklist templates

## Key topics covered

| Topic | Where to look |
| ----- | ------------- |
| Color calibration (Lightroom, GIMP, DaVinci Resolve, ffmpeg, Python) | [`notebooks/01_color_calibration.ipynb`](notebooks/01_color_calibration.ipynb) |
| Lens distortion correction | [`notebooks/02_lens_correction.ipynb`](notebooks/02_lens_correction.ipynb) |
| Perspective rectification and scale | [`notebooks/03_perspective_rectification_and_scale.ipynb`](notebooks/03_perspective_rectification_and_scale.ipynb) |
| Acquisition metadata and checklist | [`notebooks/04_acquisition_metadata_checklist.ipynb`](notebooks/04_acquisition_metadata_checklist.ipynb) |
| Camera calibration software (multical, Anipose, mrcal …) | [`links/camera-calibration.md`](links/camera-calibration.md) |
| Camera synchronization | [`links/synchronization.md`](links/synchronization.md) |
| Color correction tools | [`links/color-correction.md`](links/color-correction.md) |
| Animal tracking software (TRex, SLEAP, DeepLabCut …) | [`links/tracking.md`](links/tracking.md) |
| Photogrammetry / 3D reconstruction | [`links/photogrammetry.md`](links/photogrammetry.md) |
| Data analysis | [`links/data-analysis.md`](links/data-analysis.md) |
| Case studies | [`links/case-studies.md`](links/case-studies.md) |
| 2D detection and tracking | [`links/detection.md`](links/detection.md) |
| Aerial imaging with drones | [`links/georeferencing-drones.md`](links/georeferencing-drones.md) |
| Satellite imagery | [`links/satellite-imagery.md`](links/satellite-imagery.md) |

## Contributing

Contributions are welcome through pull requests:
- adding useful links
- adding or improving tutorial notebooks or guides
- improving explanations for new users

Please keep additions concise, clearly labeled, and beginner-friendly.
