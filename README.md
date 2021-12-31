# 2DHPE (2D Hand Pose Estimation)

### By Mithesh Ramachandran

----

### Introduction:

Hand Pose Estimation (HPE) is an important part of 3-D Hand Reconstruction and Gesture Recognition. It involves obtaining hand key points such as fingertips and joints from an input image of a hand. Standard HPE methods involve using depth images for HPE. This might not be the most feasible option as they require specialized hardware. 2-D HPE is a method where the model input is an RGB image, without a depth dimension. This method is more effective for setups that use a standard RGB image camera. Various models have been used to accurately predict the key points, including segmentation models such as U-Nets and key point regression models. This article explores HPE using 2-D RGB images and the use of modified U-Nets to minimize the average key point percentage error.

### Methodology:

The 2-D Hand Pose Estimation process can be divided into 2 parts: Preprocessing and Model Building & Training. Pre-processing involves projecting the 3-D points onto a 2-D plane. Model Building and Training is based on U-Net architecture and its modifications.

### Software:

Both pre-processing and model building, and training have been done on python version 3.7. [PyTorch](https://github.com/pytorch/pytorch) library has been used to build the U-Nets. Custom dataset class and data loaders were created. The models have been trained using the NVIDIA Tesla -T4 GPUs (15 GB).

### Dataset:

The [FreiHAND dataset](https://github.com/lmb-freiburg/freihand) consists of 32560 RGB images of the right hand showing various hand poses. These images are augmented with different background and scale, which results in the total dataset having 130240 images. There are 21 hand points in the dataset.
The dataset consists of masks of hands, a JSON file with the 3-D coordinates of the hand points. It also consists of an intrinsic camera K matrix that helps in deriving the 2-D coordinates of the points.
