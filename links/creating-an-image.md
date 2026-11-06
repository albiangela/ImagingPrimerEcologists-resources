---
layout: default
---

# Creating an Image

Resources on the fundamentals of image formation — the exposure settings and
light sources that determine image quality before any post-processing. These
correspond to Section 3 of *An Imaging Primer for Ecologists*.

For a hands-on walkthrough of acquisition planning and metadata capture, see the
companion notebook
[`04_acquisition_metadata_checklist.ipynb`](../notebooks/04_acquisition_metadata_checklist.ipynb).

## Exposure settings

The *exposure triangle* describes how exposure time (shutter speed), aperture,
and ISO/gain interact to produce a well-exposed image. Aperture additionally
controls depth of field, exposure time affects motion blur and attainable frame
rate, and ISO/gain trades sensitivity for noise.

| Resource | Type | Notes |
|----------|------|-------|
| [PhotoPills exposure guide](https://www.photopills.com/articles/understanding-the-exposure-triangle) | Tutorial | Beginner-friendly explanation of the exposure triangle |
| [OpenCV camera basics](https://docs.opencv.org/4.x/) | Documentation | Programmatic control of exposure, gain, and capture settings |

### Background reading

- Battiato, Castorina & Mancuso (2003) — High dynamic range imaging for digital still cameras: an overview. *Journal of Electronic Imaging*. [doi:10.1117/1.1580829](https://doi.org/10.1117/1.1580829)
- Burggraaff et al. (2019) — Standardized spectral and radiometric calibration of consumer cameras. *Optics Express*. [doi:10.1364/OE.27.019075](https://doi.org/10.1364/OE.27.019075)
- Chlubna & Zemčík (2025) — Comparative survey of image compression methods across pixel formats and bit depths. [doi:10.1007/s11760-025-04579-6](https://doi.org/10.1007/s11760-025-04579-6)

## Light source

Most imaging systems operate in three wavelength ranges: ultraviolet (UV,
10–400 nm), visible light (380–780 nm), and infrared (IR, 780–1000 nm). Beyond
wavelength, the type of light source (incandescent, fluorescent, LED) affects
spectral properties, efficiency, and flicker. Diffuse lighting reduces harsh
shadows, while reflections and glare can hinder automated analysis.

### Background reading

- Delcourt et al. (2011) — Video tracking in the extreme: fluorescent elastomer tags for nocturnal underwater animals. *Behavior Research Methods*. [doi:10.3758/s13428-011-0060-5](https://doi.org/10.3758/s13428-011-0060-5)
- Chittka et al. (1994) — Ultraviolet as a component of flower reflections and the colour perception of Hymenoptera. *Vision Research*. [doi:10.1016/0042-6989(94)90151-1](https://doi.org/10.1016/0042-6989(94)90151-1)
- Newman & Hartline (1982) — The infrared "vision" of snakes. *Scientific American*.
- [Zhang & Hu (2021)](https://doi.org/10.34133/2021/9753625) — Light scattering by pure water and seawater: recent development.
- Azevedo et al. (2025) — The effects of light on vertebrate welfare: a review. *Animals*. [doi:10.3390/ani15223329](https://doi.org/10.3390/ani15223329)

## Hardware and acquisition resources

- [GoPro Labs](https://gopro.github.io/labs/) — action-camera customization (SI Box S1).
- [v4l-utils](https://git.linuxtv.org/v4l-utils.git/) — Linux camera controls, including `v4l2-ctl` (SI Box S1).
- [Grove Strong: exposure triangle](https://www.wearegrovestrong.com/blog-post/photo-basics-understanding-the-exposure-triangle) — source cited for Figure 1A.
- [Tamron: depth of field](https://www.tamron.com/global/consumer/sp/impression/detail/article-what-is-depth-of-field.html) — source cited for Figure 1B.

SI Boxes S1 and S2 cover camera hardware and image information. Record the sensor, lens, filters, illumination, storage, container, codec, pixel format, bit depth, and color channels alongside acquisition settings; the [metadata notebook](../notebooks/04_acquisition_metadata_checklist.ipynb) provides a template.

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
