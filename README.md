This Project is based on https://github.com/drprojects/DeepViewAgg

It is a part of my work with my teammate Jakob Waibel in our Masters' course Advanced Deep Learning for Computer Vision at the Technical University of Munich. Most of our work is done on `/torch_points3d/modules/multimodal/fusion.py` as we investigated a self-attention based novel mechanism for fusing features from 2D and 3D data.  

## Requirements :memo:
The following must be installed before installing this project.
- Anaconda3
- cuda >= 11.6
- gcc >= 7

All remaining dependencies (PyTorch, PyTorch Geometric, etc) should be installed using the provided [installation script](init.sh).
For using the point transformer layer follow instruction in https://github.com/POSTECH-CVLab/point-transformer

The code has been tested in the following environment:
- Ubuntu 20.04.5 LTS
- Python 3.7.9
- PyTorch 1.12.0
- CUDA 11.6
- NVIDIA GeForce RTX 3080 10G
- 64G RAM


## Disclaimer
This is **not the official [Torch-Points3D](https://github.com/nicolas-chaulet/torch-points3d) framework**. This work builds on and modifies a fixed version of the framework and has not been merged with the official repository yet. In particular, this repository **introduces numerous features for multimodal learning on large-scale 3D point clouds**. In this repository, some TP3D-specific files were removed for simplicity. 

## Project structure
The project follows the original [Torch-Points3D framework](https://github.com/nicolas-chaulet/torch-points3d) structure.
```bash
├─ conf                    # All configurations live there
├─ notebooks               # Notebooks to get started with multimodal datasets and models
├─ eval.py                 # Eval script
├─ insall.sh               # Installation script for DeepViewAgg
├─ scripts                 # Some scripts to help manage the project
├─ torch_points3d
    ├─ core                # Core components
    ├─ datasets            # All code related to datasets
    ├─ metrics             # All metrics and trackers
    ├─ models              # All models
    ├─ modules             # Basic modules that can be used in a modular way
    ├─ utils               # Various utils
    └─ visualization       # Visualization
└─ train.py                # Main script to launch a training
```

The models we added can be found under conf/models/segmentation/multimodal/adl4cv-scannet.yaml

Scripts to train
- `scripts/train_kitti360.sh`
- `scripts/train_s3dis.sh`
- `scripts/train_scannet.sh`

For more information on the project check https://github.com/drprojects/DeepViewAgg for detailed 
