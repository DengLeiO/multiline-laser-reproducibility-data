# multiline-laser-reproducibility-data
This repository provides partial data for reproducing and verifying the experiments reported in the manuscript:

## Contents
The repository includes:
1. **Stereo calibration results**
   - left–middle stereo calibration results
   - middle–right stereo calibration results
   - left–right stereo calibration results
2. **Representative scene data**
   - for three representative scenes
   - left, middle, and right speckle images
   - the corresponding left, middle, and right line-laser images

## Directory structure
reproducibility_data/
├─ scene_1/
│  ├─ calibration_results/
│  └─ images/
│     ├─ speckle_images/
│     └─ line_laser_images/
├─ scene_2/
│  ├─ calibration_results/
│  └─ images/
│     ├─ speckle_images/
│     └─ line_laser_images/
└─ scene_3/
   ├─ calibration_results/
   └─ images/
      ├─ speckle_images/
      └─ line_laser_images/

## Usage
These data are provided to support:
- construction of speckle depth priors
- verification of the subsequent matching and reconstruction process

## Note
Due to shared institutional intellectual property restrictions, the full source code cannot be publicly released at this stage.
