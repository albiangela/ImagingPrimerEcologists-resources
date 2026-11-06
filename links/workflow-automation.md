---
layout: default
---

# Data Management and Workflow Automation

Resources on data management, file naming, and reproducible, automated
processing pipelines. These correspond to Sections 5.1 (Data Management) and 5.2
(Workflow Automation) of *An Imaging Primer for Ecologists*.

## Data Management

Establishing consistent data structures, file naming conventions, and metadata
standards as early as possible is critical. Common naming conventions include
`snake_case`, `camelCase`, and `kebab-case`; all avoid spaces, which impede
searching and cross-platform compatibility. For automatically generated files,
zero-padded numbering (e.g., `000000.mp4`, `000001.mp4`) ensures correct sorting
and simplifies parsing.

### Background reading

- Wilkinson et al. (2016) — The FAIR guiding principles for scientific data management and stewardship. *Scientific Data*. [doi:10.1038/sdata.2016.18](https://doi.org/10.1038/sdata.2016.18)
- Cooper & Hsing (2025) — *Guide to Reproducible Code*. British Ecological Society. [doi:10.5281/zenodo.16421733](https://doi.org/10.5281/zenodo.16421733)
- [Jones et al. (2026)](https://doi.org/10.1111/2041-210x.70259) — A short guide for effective field data collection.

## Workflow Automation

Once a suitable data structure is in place, analysis can be automated with
scripts following consistent naming (e.g., `0_cut_videos.py`,
`1_whitebalance.py`, `2_remove_background.py`) integrated into a pipeline.
Workflows can be scheduled with `cron` (Linux/macOS) or Task Scheduler (Windows),
and containerized for reproducibility and sharing.

### Code standardization and containerization

Overview of common code standardization and containerization solutions.

| Software | Description | Reference |
|----------|-------------|-----------|
| [Singularity / Apptainer](https://apptainer.org/) | Containerization software (HPC-focused) | Kurtzer et al. 2017 |
| [Docker](https://www.docker.com/) | Containerization software | Merkel 2014 |
| [conda](https://docs.conda.io/) | Package and project manager | Anaconda Inc. |
| [uv](https://github.com/astral-sh/uv) | Package and project manager | Astral |

### General-purpose automation tools

| Software | Description | Reference |
|----------|-------------|-----------|
| [ffmpeg](https://ffmpeg.org/) | Cross-platform tool to record, convert, and stream audio and video | FFmpeg Developers 2024 |
| [GitHub](https://github.com/) | Version control and code hosting | — |
| [Zenodo](https://zenodo.org/) | Archiving and DOI minting for code and data | — |
| [Figshare](https://figshare.com/) | Archiving and sharing of research outputs | — |

### Fiducial markers

Fiducial markers enable automated detection and scaling of reference objects or
animals placed within the field of view, supporting rectification and dynamic
spatial tracking.

| Software | Description | Reference |
|----------|-------------|-----------|
| [BEEtag](https://github.com/jamescrall/BEEtag) | Low-cost, image-based fiducial tracking | Crall et al. 2015 |
| [ArUco / ChArUco (OpenCV)](https://docs.opencv.org/4.x/d5/dae/tutorial_aruco_detection.html) | Marker detection for pose and rectification | Bradski 2000 |

## Additional resources from the final proof

- [Cooper & Barber (2026), BES Data Management guide](https://assets.britishecologicalsociety.org/2026/09/21103535/BES-Data-management-guide-2026.pdf).
- [TracktorLive](https://doi.org/10.64898/2026.03.12.711471) — real-time tracking and response systems.

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
