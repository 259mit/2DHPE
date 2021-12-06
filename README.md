# 2DHPE

### By Mithesh Ramachandran

----

### Introduction

Hand Pose Estimation (HPE) is an important part of 3-D Hand Reconstruction and Gesture Recognition. It involves obtaining hand key points such as fingertips and joints from an input image of a hand. Standard HPE methods involve using depth images for HPE. This might not be the most feasible option as they require specialized hardware. 2-D HPE is a method where the model input is an RGB image, without a depth dimension. This method is more effective for setups that use a standard RGB image camera. Various models have been used to accurately predict the key points, including segmentation models such as U-Nets and key point regression models. This article explores HPE using 2-D RGB images and the use of modified U-Nets to minimize the average key point percentage error.

### Methodology


