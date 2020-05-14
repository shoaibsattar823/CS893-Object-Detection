# Table of Content
[Introduction](url)

[1. RetinaNet](url)

[2. Faster RCNN](url)

[3. YOLOv3](url)

# Object Detection
Object Detection is the problem of detecting objects in visual data. Detecing an object in image means to predict a bounding box around that object showing the coordinates in the image where the object lies and class of the object is also predicted.
In this project, I am doing object detection on [SIMS](url) using different object detection techniques/architectures which are RetinaNet, YOLOv3 and Faster RCNN.

## 1. U-Net
(Modified the original implementation at https://github.com/hlamba28/UNET-TGS/blob/master/TGS%20UNET.ipynb for this dataset)

###### Model Diagram
![model plot](unet_model_plot.png)

###### Training Settings
* Input Size: 1024x1024
* Optimizer: SGD
* Learning Rate: 0.001
* Batch Size: 5
* Epochs: 50

###### Evaluation
* Accuracy = 0.82
* Dice Score = 0.41

###### Learning Curve
![Learning Curve](unet_learning_curve.png)

###### Visualization
![demo1](unet_demo1.png)
![demo2](unet_demo2.png)

## 2. SegNet

###### Model Diagram
![model plot](segnet-model-diagram.png)

###### Training Settings
* Input: 256x256 size images for training which are actually patches of original 1000x1000 size image.
* Optimizer: Adam
* Batch Size: 16
* Epochs: 50

###### Evaluation
* Accuracy = 0.58
* Dice Score = 0.35
* F1-Score = 0.43
* Loss (Binary Crossentropy) = 0.82

###### Learning Curve
![Learning Curve Loss](segnet-loss-curve.png)
![Learning Curve Acc](seget-acc-curve.png)

###### Visualization
![demo1](segnet-demo1-test.png)
![demo2](segnet-demo2-test.png)

## 3. DeepLab-v3

###### Model Diagram
![model plot](deeplabv3plus-model-diagram.png)

###### Training Settings
* Input Size: 256x256 patches from original 1000x1000 image
* Optimizer: Adam
* Batch Size: 8
* Epochs: 32

###### Evaluation
* Accuracy = 0.8968995
* Dice Score = 0.74143386
* F1-Score = 0.75504327
* Loss (Binary Crossentropy) = 0.3610503834391397

###### Learning Curve
![Learning Curve Loss](deeplabv3plus-learningcurve.png)

###### Visualization
![demo1](deeplabv3plus-demo1.png)
![demo2](deeplabv3plus-demo2.png)
![demo3](deeplabv3plus-demo3.png)
