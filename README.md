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

1. **Read `links/README.md`** for a curated collection of calibration tools, tracking
   software, and background references.
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
| Camera calibration software (multical, Anipose, mrcal …) | [`links/README.md`](links/README.md#camera-calibration) |
| Animal tracking software (TRex, SLEAP, DeepLabCut …) | [`links/README.md`](links/README.md#animal-tracking) |
| Photogrammetry / 3D reconstruction | [`links/README.md`](links/README.md#photogrammetry--3d-reconstruction) |

## Contributing

Contributions are welcome through pull requests:
- adding useful links
- adding or improving tutorial notebooks or guides
- improving explanations for new users

Please keep additions concise, clearly labeled, and beginner-friendly.
