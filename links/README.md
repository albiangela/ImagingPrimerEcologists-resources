# Important links

Curated references for the *An Imaging Primer for Ecologists* paper and this repository.

---

## Paper

- [An Imaging Primer for Ecologists](https://github.com/mooch443/BehavioralVideoAnalysis) — this repository (preprint link to be added on publication)

---

## Camera calibration

### Software (single- and multi-camera)

- [multical](https://github.com/oliver-batchelor/multical) — chessboard-based multi-camera calibration in Python
- [mrcal](https://mrcal.secretsauce.net/) — camera calibration with custom lens models; good for wide-angle lenses
- [Anipose](https://anipose.readthedocs.io/en/latest/tutorial.html) — chessboard or wand calibration for multi-view pose estimation (Karashchuk et al. 2021)
- [Kalibr](https://github.com/ethz-asl/kalibr) — AprilTag-based spatiotemporal calibration for camera-IMU systems (Rehder et al. 2016)
- [Deep ChArUco](https://github.com/JunkyByte/deepcharuco) — deep-learning-based ChArUco detection, robust to motion blur and underwater distortion
- [eWand](https://github.com/backyardbiomech/eWand) — calibration wand approach for flexible setups (Gossard et al. 2023)

### Calibration targets

- [ChArUco board (8×11)](../assets/calibration_targets/charuco_8x11.pdf) — printable PDF included in this repo
- [Annotated ChArUco board](../assets/calibration_targets/charuco_8x11_annotated.pdf) — printable PDF showing key measurements
- [OpenCV chessboard (14×9)](../assets/calibration_targets/opencv_checkerboardSB.pdf) — printable PDF included in this repo
- [OpenCV calibration tutorial](https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html) — step-by-step guide using the Python bindings

### Lens distortion correction

- [notebooks/02_lens_correction.ipynb](../notebooks/02_lens_correction.ipynb) — apply calibration to images, videos, or trajectories using OpenCV
- [OpenCV undistort docs](https://docs.opencv.org/4.x/d9/d0c/group__calib3d.html) — `cv2.undistort`, `cv2.initUndistortRectifyMap`, `cv2.undistortPoints`

---

## Color calibration

### Reference targets

- [X-Rite ColorChecker Classic / Passport](https://www.xrite.com/categories/calibration-profiling/colorchecker-classic) — 24-patch reference standard; widely used in ecological imaging
- [Calibrite ColorChecker](https://calibrite.com/us/product/colorchecker-classic/) — equivalent product (X-Rite rebranded)
- [ColorChecker reference values (sRGB)](https://www.xrite.com/service-support/new_color_specs) — official target values for all 24 patches

### Software guides (in this repo)

- [notebooks/01_color_calibration.ipynb](../notebooks/01_color_calibration.ipynb) — step-by-step walkthroughs (Lightroom, GIMP, DaVinci Resolve, Final Cut Pro, ffmpeg) plus a runnable Python/OpenCV pipeline

### Tools — general

- [Adobe Camera Raw / Lightroom](https://helpx.adobe.com/camera-raw/using/adobe-camera-raw.html) — eyedropper + curves correction; X-Rite plug-in available
- [GIMP](https://www.gimp.org/) — free; Colors → Curves; Script-Fu for batch processing
- [Darktable](https://www.darktable.org/) — free, open-source; has a dedicated Color Calibration module with built-in ColorChecker support
- [X-Rite ColorChecker Camera Calibration plug-in](https://www.xrite.com/service-support/passport_photo2) — free plug-in for Lightroom/Photoshop; creates a custom DNG camera profile
- [colour-science (Python)](https://www.colour-science.org/) — Python library with full ColorChecker support for programmatic calibration

### Tools — specialized

- [micaToolbox](https://www.empiricalimaging.com/about/) — ImageJ-based toolbox for ecological colour pattern analysis (Troscianko & Stevens 2015)
- [Sea-Thru](https://github.com/hainh/sea-thru) — physically-based underwater colour restoration (Akkaynak & Treibitz 2019)
- [Lumariver Profile Designer](https://lumariver.com/profile-designer/) — advanced DNG profile creation from ColorChecker measurements

---

## Animal tracking

- [TRex](https://trex.run/) — background subtraction + YOLO-compatible; identity-preserving tracking (Walter & Couzin 2021)
- [idtracker.ai](https://idtracker.ai/latest/) — background subtraction; identity-preserving multi-animal tracking (Torrents et al. 2025)
- [SLEAP](https://sleap.ai/) — deep-learning keypoint detection (Pereira et al. 2022)
- [DeepLabCut](https://github.com/DeepLabCut/DeepLabCut) — keypoint detection with 3D support (Nath et al. 2019; Lauer et al. 2022)
- [FastTrack](https://www.fasttrack.sh/) — centroid tracking (Gallois & Candelier 2021)
- [AnimalTA](http://vchiara.eu/index.php/animalta) — centroid tracking with manual correction (Chiara & Kim 2023)

---

## Photogrammetry / 3D reconstruction

- [Meshroom](https://github.com/alicevision/Meshroom) — open-source, node-based structure-from-motion pipeline
- [COLMAP](https://colmap.github.io/) — open-source photogrammetry for unordered image collections
- [Metashape](https://www.agisoft.com/) — commercial photogrammetry (Agisoft; academic licence available)

---

## Post-processing / trajectory analysis

- [movement](https://movement.neuroinformatics.dev/) — Python library for trajectory cleaning, visualization, and analysis (Sirmpilatze et al. 2025)
- [animovement](https://github.com/roaldarbol/animovement) — R library for trajectory cleaning and motion quantification (Roald-Arbøl 2025)
- [swaRmverse](https://marinapapa.github.io/swaRmverse/) — R library for collective motion analysis (Papadopoulou 2025)

---

## Data acquisition software

- [mokap](https://github.com/FlorentLM/mokap) — multi-camera acquisition software
- [campy](https://github.com/ksseverson57/campy) — multi-camera acquisition with real-time compression
- [pypylon](https://github.com/basler/pypylon) — official Python wrapper for Basler cameras
- [ffmpeg](https://ffmpeg.org/) — versatile command-line tool for video conversion, trimming, and processing

---

## Background reading

- Anderson & Perona 2014 — [Toward a Science of Computational Ethology](https://doi.org/10.1016/j.neuron.2014.09.005)
- Tuia et al. 2022 — [Perspectives in machine learning for wildlife conservation](https://doi.org/10.1038/s41467-022-27980-y)
- Panadeiro et al. 2021 — [A review of 48 open-source tools for behavioral analysis](https://doi.org/10.1093/gigascience/giab08)
- Troscianko & Stevens 2015 — [Image calibration and analysis toolbox](https://doi.org/10.1111/2041-210X.12439) (micaToolbox)
- Akkaynak & Treibitz 2019 — [Sea-Thru: A Method for Removing Water from Underwater Images](https://doi.org/10.1109/CVPR.2019.00178)
