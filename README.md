# multiline-laser-reproducibility-data

This repository provides partial data for reproducing and verifying the experiments reported in the manuscript.

## Folder description
- `scene_1_plaster`: plaster scene used for qualitative and quantitative reconstruction evaluation
- `scene_2_plaster`: another plaster scene used for qualitative and quantitative reconstruction evaluation
- `scene_3_standard_sphere`: standard-sphere scene used for reconstruction accuracy evaluation
- `scene_4_multi_pose`: multi-pose scene used for evaluating reconstruction stability under hand-held motion
- `scene_5_failure_case`: transparent-surface failure case used for analysing applicability boundaries
- `scene_6_calibration_verification`: calibration-board images and corresponding stereo calibration results

## General note

For scenes 1–5:
- `line_laser_images` contains LaS images
- `speckle_images` contains speckle images
- the image indices in `line_laser_images` and `speckle_images` correspond to the same acquisition instance

For scene 6:
- `calibration_images` contains calibration-board images
- `our_calibration_results` contains the stereo calibration results estimated from these images

## Note
Due to shared institutional intellectual property restrictions, the full source code cannot be publicly released at this stage.
