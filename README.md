# multiline-laser-reproducibility-data

This repository provides partial validation data for the manuscript:

**Multi-line laser matching and reconstruction for handheld scanning via infrared speckle depth guidance and trinocular geometric constraints**

The released data are provided to support external inspection of the input images, calibration results, representative qualitative results, and part of the quantitative evaluation procedure. The full source code is not publicly released at this stage due to shared institutional intellectual property restrictions.

## Folder description

* `scene_1_plaster`: plaster scene used for representative qualitative experiments and matching-performance evaluation.
* `scene_2_plaster`: another plaster scene used for matching-performance evaluation and ablation-related verification.
* `scene_3_standard_sphere`: standard-sphere scene used for reconstruction accuracy evaluation.
* `scene_4_multi_pose`: multi-pose scene used for evaluating reconstruction stability under handheld acquisition.
* `scene_5_failure_case`: transparent-surface failure case used for analysing applicability boundaries.
* `scene_6_calibration_verification`: calibration-board images and corresponding stereo calibration results.

## General note

For scenes 1–5:

* `line_laser_images` contains LaS images.
* `speckle_images` contains speckle images.
* `calibration_results` contains the calibration parameters used in the corresponding experiments.
* The image indices in `line_laser_images` and `speckle_images` correspond to the same acquisition instance.

For scene 6:

* `calibration_images` contains calibration-board images.
* `our_calibration_results` contains the stereo calibration results estimated from these images.

## Correspondence between manuscript experiments and released data

| Manuscript section       | Experiment                                        | Released data                        | Verification purpose                                                                                                    |
| ------------------------ | ------------------------------------------------- | ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| Section 5.2              | Qualitative experiments                           | `scene_1_plaster`                    | Inspect representative speckle images, line-laser images, calibration files, and qualitative reconstruction input data. |
| Section 5.3.1            | Matching performance                              | `scene_1_plaster`, `scene_2_plaster` | Inspect the input data used for MR/MPR evaluation and check the evaluation protocol described in the manuscript.        |
| Section 5.3.2            | Reconstruction accuracy                           | `scene_3_standard_sphere`            | Inspect the input data and calibration results used for standard-sphere reconstruction accuracy evaluation.             |
| Section 5.4.3            | Reconstruction results under handheld acquisition | `scene_4_multi_pose`                 | Inspect multi-pose data used for evaluating reconstruction stability under handheld acquisition.                        |
| Section 5.4.4            | Failure-case and applicability-boundary analysis  | `scene_5_failure_case`               | Inspect the transparent-surface failure case used to analyse applicability boundaries.                                  |
| Section 5.5              | Ablation experiments                              | `scene_2_plaster`                    | Inspect the representative input data used for ablation-related verification.                                           |
| Calibration verification | Camera calibration accuracy                       | `scene_6_calibration_verification`   | Inspect calibration-board images and corresponding calibration results.                                                 |

## Evaluation reference for MR and MPR

Independent point-wise LSCP matching ground truth is difficult to obtain in practical handheld multi-line laser scanning scenes. Therefore, the MR and MPR values reported in the manuscript are computed using manually verified matching reference labels.

For each reconstructed frame, the correctness of LSCP matching is judged according to:

* the spatial distribution of reconstructed 3D points;
* the continuity of reconstructed stripe profiles;
* the geometric consistency between reconstructed points and the measured surface.

Mismatched LSCPs usually appear as isolated noisy 3D points, abnormal local profiles, or unreasonable spatial jumps away from the measured surface. These mismatched points can be traced back to the original 2D LSCP correspondences through the matching relationship and are counted as false positives (FP). Left-view LSCPs for which no valid cross-view correspondence is established, or from which no valid 3D point can be reconstructed, are counted as false negatives (FN). The remaining manually verified valid matches are counted as true positives (TP).

All compared methods in the manuscript are evaluated using the same protocol.

## Note

Because the complete source code is not released, the dataset is not intended to fully reproduce all numerical results from scratch. Instead, it is provided to support:

* inspection of raw speckle and line-laser images;
* verification of camera calibration data;
* examination of representative qualitative matching and reconstruction cases;
* understanding of the MR/MPR evaluation protocol;
* partial verification of the data basis used in the quantitative experiments;
* inspection of handheld multi-pose and failure-case data.
