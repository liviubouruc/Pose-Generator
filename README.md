## Dataset
Available at https://huggingface.co/datasets/unibuc-cs/3DHumanEmotions

## SMPLify-X Pipeline:
This repository provides a set of Jupyter notebooks for processing videos, extracting frames, generating 3D meshes using SMPLify-X, and visualizing the results. It integrates tools such as FFmpeg, OpenPose, and VPoser to facilitate human pose estimation and 3D reconstruction.

### Usage
1. Extract Frames from Video
2. Convert Image to SMPL-X Mesh
3. ScoreHMR Implementation
4. Generate Pose Variations
5. Visualize Mesh

### Overview
This repository contains the following Jupyter notebooks:
- Video Frame Extraction (Python script) - Uses FFmpeg to extract frames from a given video at a specified rate.
- Image to SMPL-X Mesh (Jupyter Notebook) - Converts 2D images into SMPL-X meshes using OpenPose and SMPLify-X.
- ScoreHMR Implementation (Jupyter Notebook) - Uses ScoreHMR for pose estimation and requires authentication with SMPLify.
- VPoser Model (Jupyter Notebook) - Generates pose variations based on a given SMPL object.
- Mesh Visualization (Python script) - Uses the vedo library to visualize 3D meshes.

### Requirements
Before running the notebooks, ensure you have the following files available in Google Drive:
pose_iter_102000.caffemodel.zip
pose_iter_584000.caffemodel.zip
pose_iter_116000.caffemodel.zip

### Steps
1. Extract frames using extract_frames.py, setting the video path and output directory for extracted frames.
2. Convert the image to SMPL-X object using image_to_smpl-x_mesh.ipynb ; Set the correct paths for the OpenPose models, SMPL-X model, and VPoser model before executing the notebook.
3. For a comarative perspective, the ScoreHMR implementation is in the ScoreHMR.ipynb notebook.
4. Run vposer.ipynb, providing a valid SMPL object as input to generate pose variations.
5. Visualize meshes using the python script provided to, setting the correct mesh path.

## Big thanks to:

- https://github.com/vchoutas/smplify-x | https://github.com/KyujinHan/Smplify-X-Perfect-Implementation
- https://github.com/nghorbani/human_body_prior
- https://statho.github.io/ScoreHMR/
- https://github.com/nghorbani/homogenus
