# BehavioralVideoAnalysis

This repository is a **tutorial / read-more companion** for the paper
*An Imaging Primer for Ecologists* (Francisco et al., 2026).

It collects curated links and step-by-step Jupyter notebooks for ecologists
working with images and video. The link collection is organized to follow the
**section structure of the manuscript**, so each topic maps to a section of the paper.

## Repository layout

```text
links/          curated links — organized by manuscript section
notebooks/      step-by-step guides and Jupyter notebooks
assets/         reusable notebook assets such as printable calibration targets
examples/       small example settings and metadata files for notebooks
figure/         notebook for recreating Figure 4
```

## Start here

1. **Browse `links/`** for a curated collection, organized by the manuscript's sections:

   **Creating an Image** (§3)
   - [`links/creating-an-image.md`](links/creating-an-image.md) — exposure settings and light sources

   **Standardizing an Image** (§4)
   - [`links/synchronization.md`](links/synchronization.md) — camera synchronization (hardware/software triggers) and acquisition software
   - [`links/camera-calibration.md`](links/camera-calibration.md) — intrinsic/extrinsic calibration tools (multical, Anipose, Kalibr, mrcal …)
   - [`links/color-correction.md`](links/color-correction.md) — color correction pipelines and tools

   **Data Handling and Analysis** (§5)
   - [`links/workflow-automation.md`](links/workflow-automation.md) — data structure, file naming, and workflow automation/containerization (Docker, conda, uv …)
   - [`links/tracking.md`](links/tracking.md) — animal tracking software (TRex, idtracker.ai, SLEAP, DeepLabCut …)
   - [`links/photogrammetry.md`](links/photogrammetry.md) — photogrammetry and 3D reconstruction
   - [`links/data-analysis.md`](links/data-analysis.md) — trajectory and movement analysis tools

   **Case Studies** (§6)
   - [`links/case-studies.md`](links/case-studies.md) — worked examples from published studies
   - [`links/detection.md`](links/detection.md) — 2D object detection and animal tracking models
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

## Manuscript sections and where to look

| Manuscript section | Where to look |
| ------------------ | ------------- |
| §3 Creating an Image (exposure, light) | [`links/creating-an-image.md`](links/creating-an-image.md), [`notebooks/04_acquisition_metadata_checklist.ipynb`](notebooks/04_acquisition_metadata_checklist.ipynb) |
| §4.1 Synchronization | [`links/synchronization.md`](links/synchronization.md) |
| §4.2 Camera Calibration | [`links/camera-calibration.md`](links/camera-calibration.md), [`notebooks/02_lens_correction.ipynb`](notebooks/02_lens_correction.ipynb), [`notebooks/03_perspective_rectification_and_scale.ipynb`](notebooks/03_perspective_rectification_and_scale.ipynb) |
| §4.3 Color Correction | [`links/color-correction.md`](links/color-correction.md), [`notebooks/01_color_calibration.ipynb`](notebooks/01_color_calibration.ipynb) |
| §5.1–5.2 Data Structure & Workflow Automation | [`links/workflow-automation.md`](links/workflow-automation.md) |
| §5.3 Tracking | [`links/tracking.md`](links/tracking.md), [`links/detection.md`](links/detection.md) |
| §5.4 Photogrammetry | [`links/photogrammetry.md`](links/photogrammetry.md) |
| Trajectory / movement analysis | [`links/data-analysis.md`](links/data-analysis.md) |
| §6.1 Standardised Measurements | [`links/case-studies.md`](links/case-studies.md) |
| §6.2 Animal Tracking & Behavioural Quantification | [`links/tracking.md`](links/tracking.md), [`links/detection.md`](links/detection.md) |
| §6.3 Remote Sensing (drones, fixed cameras, satellite) | [`links/georeferencing-drones.md`](links/georeferencing-drones.md), [`links/satellite-imagery.md`](links/satellite-imagery.md) |

## Data

The tracking data and background image needed to recreate Figure 4 are in
[`figure/20251210_124144_000/`](figure/20251210_124144_000/), so
[`figure/Figure_Calibration_MovementSpeed.ipynb`](figure/Figure_Calibration_MovementSpeed.ipynb)
runs as-is.

The full dataset associated with the publication (`MEE_data.zip`, 477 MB) is
attached to the [v1.0.0 release](https://github.com/albiangela/BehavioralVideoAnalysis/releases/tag/v1.0.0)
because its raw files exceed GitHub's per-file size limit. It contains:

| File | Description |
| ---- | ----------- |
| `basler_record_20251210_124144_000.mp4` | raw Basler recording |
| `20251210_124144_000/basler_record_20251210_124144_000.pv` | TRex pre-processed video |
| `20251210_124144_000/basler_record_20251210_124144_000.results` | TRex tracking results |
| `20251210_124144_000/basler_record_20251210_124144_000.settings` | TRex settings for this recording |
| `20251210_124144_000/data/*_id*.npz` | per-individual trajectories (also in this repo) |
| `20251210_124144_000/data/*_vi_probs.npz` | visual identification probabilities |
| `20251210_124144_000/average_*.png` | background image (also in this repo) |
| `config.settings` | TRex configuration (also in this repo) |
| `ImageAnalysis_Calibration.ipynb` | figure notebook (same code as `figure/Figure_Calibration_MovementSpeed.ipynb`) |

SHA-256: `2f4e034dd684466bcd91ced76b6d4cffd2a339db823a6a3d9439003f5316e5f8`

## Contributing

Contributions are welcome through pull requests:
- adding useful links
- adding or improving tutorial notebooks or guides
- improving explanations for new users

Please keep additions concise, clearly labeled, and beginner-friendly.
