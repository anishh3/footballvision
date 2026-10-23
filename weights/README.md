# Local model and intermediate artifacts

This directory is intentionally excluded from version control except for this file. It contains locally generated or downloaded artifacts that should not be committed to the public repository.

| Local artifact | Role | How to obtain or regenerate |
| --- | --- | --- |
| `best (1).pt` | Main four-class football object detector (ball, goalkeeper, player, referee). | Run `notebooks/01-main-model-training.ipynb`, or place the resulting detector checkpoint here and update the notebook path. |
| `best (3).pt` | Pitch keypoint checkpoint used for the 32-landmark calibration workflow. | Train/download it through `notebooks/03-pitch-calibration-homography.ipynb` using Football Field Detection v18, then update the configured path. |
| `tracking_results1.pkl` | Frame-level detections, track IDs, and team assignments from the tracking workflow. | Run the tracking/export steps in `notebooks/02-detection-tracking-experiments.ipynb`. |
| `per_frame_homographies.npz` | Per-frame image-to-pitch homographies and calibration validity information. | Run the calibration export in `notebooks/03-pitch-calibration-homography.ipynb`. |
| `calibrated_only_tracking.pkl` | Tracking results filtered to frames with valid calibration. | Run the alignment/filtering step in `notebooks/04-football-analytics.ipynb`. |
| `calibrated_only_homographies.npz` | Homographies aligned with the calibrated-only tracking data. | Run the alignment/filtering step in `notebooks/04-football-analytics.ipynb`. |

The notebooks were originally run in Kaggle and refer to `/kaggle/input` and `/kaggle/working` paths. Adapt those paths before running locally. Never commit checkpoints, datasets, raw videos, tracking pickles, or calibration archives unless you have explicitly chosen an appropriate storage/distribution method such as Git LFS.
