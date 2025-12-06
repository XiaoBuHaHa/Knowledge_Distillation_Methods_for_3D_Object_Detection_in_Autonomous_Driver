# A Comprehensive Review of Knowledge Distillation Methods for 3D Object detection in Autonomous Driving (2025)
 We are constantly updating this project page. If you have any questions, please contact us [here](mailto:bch88888@s.ytu.edu.cn).

![overview](Figures/Auto_drirver.png)

This repository is with our [survey paper](https://arxiv.org/abs/2206.09474):

> **Title:** A Comprehensive Review of Knowledge Distillation Methods for 3D Object detection in Autonomous Driving <br>
> **Authors:** Changhong Bu,Weiqing Yan:<br>
> **Publication:** None <br>

We collect the most commonly used autonomous driving datasets at [Datasets for Autonomous Driving](Papers.md).  
the current 3D object detection methods at [3D Object Detection Methods -- LIDAR, Camera, LiDAR-Camera fusion](Papers.md).  
the knowledge distillation–based approaches for 3D object detection at [3D Object Detection Algorithm Based on Knowledge Distillation](Papers.md).

## Content

![taxonomy](Figures/Paper_Structure.png)

<a name="0"></a>

- [1. The Paradigm of 3D Object Detection](#1)
    - [1.1 LiDAR-based 3D Object Detection](#1.1)
        - [1.1.1 Point-based 3D object detection](#1.1.1)
        - [1.1.2 Voxel-based 3D object detection](#1.1.2)
        - [1.1.3 Point-voxel fusion based 3D object detection](#1.1.3)
    - [1.2 Camera-based 3D Object Detection](#1.2)
        - [1.2.1 Monocular 3D object detection](#1.2.1)
        - [1.2.2 Stereo-based 3D object detection](#1.2.2)
        - [1.2.3 Multi-view 3D object detection](#1.2.3)
    - [1.3 Multi-Modal 3D Object Detection](#1.3)
        - [1.3.1 Early-fusion based 3D object detection](#1.3.1)
        - [1.3.2 Middile-fusion based 3D object detection](#1.3.2)
        - [1.3.3 Late-fusion based 3D object detection](#1.3.3)
- [2. What is Knowledge Distillation (Feature distillation,Relation distillation,Respond distillation) ](#2)
    - [2.1 Feature distillation](#2.1)
    - [2.2 Relation distillation](#2.2)
    - [2.3 Respond distillation](#2.3)
- [3. LIDAR to LIDAR Knowledge Distillation for 3D Detection](#3)
    - [3.1 Homogeneous distillation](#3.1)
        - [3.1.1 Pruning with Distillation](#3.1)
        - [3.1.2 Quantification with Distillation](#3.2)
    - [3.2 Heterogeneous distillation](#3.2)
- [4. LIDAR to Camera Knowledge Distillation for 3D Detection](#4)
    - [4.1 LIDAR to monocular image for 3D object detection](#4.1)
    - [4.2 LIDAR to stereo image for 3D object detection](#4.2)
    - [4.3 LIDAR to multi-view image for 3D object detection](#4.3)
- [5. LIDAR-Based-Multi-Modal to other Modal Knowledge Distillation for 3D Detection ](#5)
    - [5.1 LIDAR-Camera Fusion to LIDAR](#5.1)
    - [5.2 LIDAR-Camera Fusion to Camera](#5.2)
  

# The Paradigm of 3D Object Detection
![](Figures/Auto_driver_in_3D_detection.png)

## LiDAR-based 3D Object Detection
<a name="1"></a>
![](Figures/L-C_Fusion_Time.png)

A chronological overview of the most influential LiDAR-based 3D object detection methods.

### Point-based 3D object detection [[Papers]](Docs/Sensor/LiDAR/point_view.md)

![](Figs/lidarmap.JPG)

A chronological overview of the most prestigious LiDAR-based 3D object detection methods. 

![](Figures/Point_based.png)

A general point-based detection framework contains a point-based backbone network and a prediction head. The point-based backbone consists of several blocks for point cloud
sampling and feature learning, and the prediction head directly estimates 3D bounding boxes from the candidate points. 

<a name="1.1.1"></a>

### Voxel-based 3D object detection [[Papers]](Docs/Sensor/LiDAR/volumetric_view.md)

![](Figures/Voxel_based.png)

The grid-based approaches rasterize point cloud into
3 grid representations: voxels, pillars, and bird’s-eye view (BEV) feature maps. 2D convolutional neural networks or 3D
sparse neural networks are applied on grids for feature extraction. 3D objects are finally predicted from BEV grid cells. 

<a name="1.1.2"></a>

### Point-voxel based 3D object detection [[Papers]](Docs/Sensor/LiDAR/mixed_views.md)

![](Figures/Point_Voxel_fusion_based.png)

Single-stage point-voxel detection framework fuses
point and voxel features in the backbone network. Two-stage point-voxel detection framework first generates 3D object
proposals with a voxel-based 3D detector, and then refines these proposals using keypoints sampled from point cloud. 

<a name="1.1.3"></a>

## Camera-based 3D Object Detection

![](Figures/Camera_Time.png)

A chronological overview of the most influential camera-based 3D object detection methods.

<a name="1.2"></a>

### Image-only monocular 3D object detection [[Papers]](Docs/Sensor/Camera/monocular.md)

<a name="1.2.1"></a>

### Stereo-based 3D object detection [[Papers]](Docs/Sensor/Camera/stereo.md)

<a name="1.2.2"></a>

### Multi-view-based 3D object detection [[Papers]](Docs/Sensor/Camera/multi-view.md)

<a name="1.2.3"></a>

## Multi-Modal 3D Object Detection

![](Figures/L-C_Fusion_Time.png)

A chronological overview of the most influential LIDAR-Camera fusion methods for 3D object detection.

<a name="1.3"></a>

### Early fusion for 3D object detection [[Papers]](Docs/Sensor/Camera/multi-view.md)

None
<a name="1.3.1"></a>

### Middle fusion for 3D object detection [[Papers]](Docs/Sensor/Camera/multi-view.md)

None
<a name="1.3.2"></a>

### Late fusion for 3D object detection [[Papers]](Docs/Sensor/Camera/multi-view.md)

None
<a name="1.3.3"></a>

# What is Knowledge Distillation?

Including characteristic distillation, relational distillation and response distillation

<a name="2"></a>

## Feature distillation [[Papers]](Docs/Sensor/Camera/monocular.md)

![](Figures/Feature_distillstion.png)
Feature distillation 

<a name="2.1"></a>

## Relation distillation [[Papers]](Docs/Sensor/Camera/stereo.md)

![](Figures/Relation_distillation.png)
Relation distillation 
<a name="2.2"></a>

## Respond distillation

![](Figures/Respond_distillation.png)
Respond distillation 

<a name="2.3"></a>

# LIDAR to LIDAR Knowledge Distillation for 3D Object Detection

![](Figs/lidarmap.JPG)
Including Homogeneous distillation and Heterogeneous distillation.

<a name="3"></a>

## Homogeneous distillation 
<a name="3.1"></a>

### Less channels with distillation [[Papers]](Docs/Sensor/Camera/monocular.md)

![](Figures/KD_with_less_channles.png)
Feature distillation 

<a name="3.1.1"></a>

### Pruning with Distillation [[Papers]](Docs/Sensor/Camera/stereo.md)

![](Figures/prune_with_distill.png)
Relation distillation 
<a name="3.1.2"></a>

### Quantification with Distillation

![](Figures/prune_with_distill.png)
Respond distillation 

<a name="3.1.3"></a>

## Heterogeneous distillation

<a name="3.2"></a>

### Quantification with Distillation

![](Figures/KD_for_Heterogeneous.png)
Respond distillation 

<a name="3.2"></a>

# LIDAR to Camera Knowledge Distillation for 3D Object Detection

![](Figs/lidarmap.JPG)
<a name="4"></a>

## LIDAR to monocular image for 3D object detection 

None
<a name="4.1"></a>

## LIDAR to stereo image for 3D object detection 

None
<a name="4.2"></a>

## LIDAR to multi-view image for 3D object detection 

None
<a name="4.3"></a>


# LIDAR-Based-Multi-Modal to other Modal Knowledge Distillation for 3D Detection
None
<a name="5"></a>

## LIDAR-Camera Fusion to LIDAR

None
<a name="5.1"></a>

## LIDAR-Camera Fusion to Camera

None
<a name="5.2"></a>
