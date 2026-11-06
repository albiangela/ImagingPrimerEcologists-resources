# Reproduce Figure 4

Install the root `requirements.txt` following the [setup instructions](../README.md), launch JupyterLab from the repository root, and open `Figure_Calibration_MovementSpeed.ipynb`. Select the environment's kernel and use **Restart Kernel and Run All Cells**. The notebook accepts a working directory of either the repository root or `figure/`.

Bundled inputs:

- `config.settings`: camera matrix, distortion coefficients, and original `cm_per_pixel` scale.
- `20251210_124144_000/average_basler_record_20251210_124144_000.png`: background image.
- `20251210_124144_000/data/basler_record_20251210_124144_000_id10.npz`: trajectory used in the figure. The other 23 individual tracks are also included.

The original positional selection (`TRACK_INDEX = 2` after lexical filename sorting) selected ID 10. The notebook now names ID 10 explicitly. It uses the recording's 10 fps rate, excludes missing/non-finite input positions, and retains the original speed calculation and focal-length scaling convention. It fails clearly on duplicate frame indices or invalid corrected coordinates.

**Interpretation:** this is a reproduction of the published calculation, not a general metric-calibration validation. The original code multiplies corrected pixel speeds by `cm_per_pixel` and `newK[0,0] / mtx[0,0]`. For a new camera or scene, establish scale in the corrected reference plane and validate it against known distances/speeds. Do not transfer the bundled calibration to another recording setup.

Output: `figure/notebook_outputs/trajectory_comparison_600dpi.pdf`, plus notebook plots and summary statistics. Generated outputs are ignored by Git.

The [publication archive](https://doi.org/10.5281/zenodo.23674782) is the source cited in the final proof for reproducing Figure 4. Raw `.mp4` and TRex `.pv` files are not required for this bundled trajectory example. The absolute `meta_source_path` in the settings file records the original acquisition location; the notebook does not read it. Keep it as provenance, or supply your own path when using TRex separately.
