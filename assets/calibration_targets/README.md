# Calibration targets

These files correspond to the illustrative calibration material in SI Figures S1–S3:

- `color_checker.png`: color-checker illustration (S1). A printout is not a calibrated physical color reference; use a characterized target and its reference values for quantitative work.
- `charuco_8x11.pdf`: ChArUco board (S2); `charuco_8x11_annotated.pdf` includes annotations. Verify orientation and board parameters against the printed target before calibration.
- `opencv_checkerboardSB.pdf`: checkerboard target (S3).

Print geometric targets without automatic page scaling and measure the actual square/marker dimensions. Enter those measured dimensions and the correct inner-corner or marker layout in the calibration software. The tutorial lens notebook demonstrates applying existing calibration; it does not estimate camera parameters from these PDFs.
