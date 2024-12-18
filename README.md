# PMLDL
## Papers

1. [Person-MinkUNet: 3D Person Detection with LiDAR Point Cloud](https://arxiv.org/pdf/2107.06780)
   1. [Person-MinkUNet](https://github.com/VisualComputingInstitute/Person_MinkUNet?tab=readme-ov-file)
2. [VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection](https://arxiv.org/pdf/1711.06396)
   1. [Voxel Net tensorflow](https://github.com/tsinghua-rll/VoxelNet-tensorflow?tab=readme-ov-file)
   2. [Voxel net Pytorch](https://github.com/skyhehe123/VoxelNet-pytorch?tab=readme-ov-file)
3. [3D Fully Convolutional Network for Vehicle Detection in Point Cloud](https://arxiv.org/pdf/1611.08069)
   1. [KiTTI Data Processing and 3D CNN for Vehicle Detection TF](https://github.com/yukitsuji/3D_CNN_tensorflow?tab=readme-ov-file)
4. [Online Learning for Human Classification in 3D LiDAR-based Tracking](https://sci-hub.sidesgame.com/10.1109/IROS.2017.8202247)
   1. [hdl_people_tracking is a ROS package for real-time people tracking using a 3D LIDAR](https://github.com/koide3/hdl_people_tracking?tab=readme-ov-file)
   2. [Online learning for human classification in 3D LiDAR-based tracking](https://github.com/LCAS/online_learning/tree/master): This is a ROS-based online learning framework for human classification in 3D LiDAR scans, taking advantage of robust multi-target tracking to avoid the need for data annotation by a human expert. Please watch the videos below for more details.
   3. [L-CAS 3D Point Cloud People Dataset](https://lcas.lincoln.ac.uk/wp/research/data-sets-software/l-cas-3d-point-cloud-people-dataset/)
5. [PointPillars: Fast Encoders for Object Detection from Point Clouds](https://paperswithcode.com/paper/pointpillars-fast-encoders-for-object)
   1. [Implementation of PointPillars in PyTorch for KITTI 3D Object Detetcion](https://github.com/shangjie-li/pointpillars)
   2. [Point Pillars (3D Object Detection) Through Explanation with Code](https://medium.com/@abdulhaq.ah/point-pillars-3d-object-detection-through-explanation-with-code-57763a3d5737)
   3. [PointPillars](https://github.com/nutonomy/second.pytorch): This repo demonstrates how to reproduce the results from PointPillars: Fast Encoders for Object Detection from Point Clouds (to be published at CVPR 2019) on the KITTI dataset by making the minimum required changes from the preexisting open source codebase SECOND.
   4. [MMDetection3D](https://github.com/open-mmlab/mmdetection3d) is an open source object detection toolbox based on PyTorch, towards the next-generation platform for general 3D detection.
6. [Online learning for 3D LiDAR-based human detection: experimental
analysis of point cloud clustering and classification methods](https://link.springer.com/epdf/10.1007/s10514-019-09883-y?author_access_token=bVLnE4rWjkyUnk8WopA0Lfe4RwlQNchNByi7wbcMAY6zHIY15ykgJsK70R8O7eQrMr2yHIZQSiyxe3OktHw_9R1puJtMefwAs4tGo2L7ytrEzPSDTxHtSdjXNYkRozK46fQM7ZPLOgSknycKxSoIsA%3D%3D)

7. [LiDAR-based Online 3D Video Object Detection with Graph-based Message Passing and Spatiotemporal Transformer Attention](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yin_LiDAR-Based_Online_3D_Video_Object_Detection_With_Graph-Based_Message_Passing_CVPR_2020_paper.pdf)
   1. Core Idea: This paper introduces an end-to-end 3D video object detector for LiDAR point clouds. The framework has two main components:
      1. Pillar Message Passing Network (PMPNet): Encodes spatial features within each frame by constructing a graph, where each LiDAR point is treated as a node, allowing information sharing across neighboring points.
      2. Attentive Spatiotemporal Transformer GRU (AST-GRU): Aggregates temporal information across frames using Transformer attention mechanisms to align and emphasize foreground objects, improving detection across sequences.
   2. Dataset: Uses the nuScenes dataset, a large-scale dataset with continuous LiDAR point clouds for autonomous driving.
   3. Input/Output: The input is sequential LiDAR point cloud frames, and the output is 3D bounding boxes with object classifications.
   4. Relevance: Highly relevant, especially for tasks involving tracking. The AST-GRU’s spatiotemporal feature aggregation can help maintain consistent human tracking across frames.
8. [Temporal-Channel Transformer for 3D Lidar-Based Video Object Detection in Autonomous Driving](https://arxiv.org/pdf/2011.13628)
   1. Core Idea: This paper proposes the Temporal-Channel Transformer (TCTR), designed to process sequential LiDAR frames by encoding temporal information (frame-to-frame) and channel-wise information. The TCTR model has two main parts:
      1. Temporal-Channel Encoder: Encodes temporal-channel information across frames, capturing dependencies between frame sequences and voxel channels.
      2. Spatial Decoder: Decodes spatial relationships within each frame to produce a dense representation for the current frame, refined to highlight objects.
   2. Dataset: Also uses nuScenes, ideal for evaluating video-based LiDAR detection performance.
   3. Input/Output: Input is consecutive frames converted into 2D pseudo-images (voxels), and output is 3D object bounding boxes.
   4. Relevance: Relevant for human detection and tracking in sparse data; however, TCTR is more focused on enhancing single-frame representations with past frames, which is less dynamic than PMPNet's graph-based message passing.
9.  [SA-Det3D: Self-Attention Based Context-Aware 3D Object Detection](https://openaccess.thecvf.com/content/ICCV2021W/AVVision/papers/Bhattacharyya_SA-Det3D_Self-Attention_Based_Context-Aware_3D_Object_Detection_ICCVW_2021_paper.pdf):
    1.  Core Idea: This paper introduces SA-Det3D, a self-attention module for 3D object detection, which integrates Full Self-Attention (FSA) and Deformable Self-Attention (DSA) to enhance the context-awareness of object detection models in point clouds. It aims to improve detection by allowing the network to capture long-range dependencies in the 3D space without increasing computational costs significantly.
        1.  FSA computes interactions between all points for robust global context.
        2.  DSA reduces computational demand by selectively attending to key points.
    2.  Dataset: It utilizes several large-scale 3D datasets, including KITTI, nuScenes, and Waymo Open Dataset.
    3.  Input/Output:
        1.  Input: LiDAR point clouds, processed into pillars or voxels, with each frame as input.
        2.  Output: 3D bounding boxes and classification labels for detected objects within each frame.
    4.  Relevance to Your Project:
        1.  This paper is relevant if your primary focus is detection, as the self-attention mechanism enhances the model’s ability to distinguish between humans and other objects by learning context across larger distances within a single frame.
        2.  However, SA-Det3D lacks temporal tracking, which is essential for tracking and recognition across multiple frames. The self-attention improves frame-by-frame detection but does not utilize temporal information, limiting its effectiveness for continuous human tracking. 
10. [Point Density-Aware Voxels for LiDAR 3D Object Detection](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_Point_Density-Aware_Voxels_for_LiDAR_3D_Object_Detection_CVPR_2022_paper.pdf):
    1.  Core Idea: This paper presents Point Density-Aware Voxel Network (PDV), designed to address LiDAR's uneven point density at varying distances. PDV leverages density-aware Region of Interest (RoI) pooling and uses kernel density estimation (KDE) and self-attention to incorporate point density information directly into the detection process. PDV enhances voxel feature localization by calculating voxel centroids for greater spatial accuracy and aggregates point features to better capture object shapes.
        1.   Voxel Point Centroid Localization: Calculates centroids of points in each voxel for more accurate localization.
        2.   Density-Aware RoI Pooling: Uses KDE to capture local density around each grid point, adding density-based positional encoding in the self-attention module.
    2.  Dataset: Evaluated on large-scale autonomous driving datasets, including the Waymo Open Dataset and KITTI.
    3.  Input/Output:
        1.  Input: LiDAR point cloud data with point coordinates and features (e.g., intensity).
        2.  Output: 3D bounding boxes and object classifications, refined based on density awareness.
    4.  Relevance to Your Project:
        1.  Detection Accuracy: PDV's density-aware design improves detection accuracy in varying densities, which can be useful for human detection, especially in crowded scenes or at greater distances where point density may be lower.
        2.  Tracking Limitations: This model focuses on refining object detection using density-based features in single frames. Unlike multi-frame methods, it doesn’t integrate temporal information, which limits its capability for continuous human tracking.
## Datasets

### To-Do dataset
 - [ ] Explore the dataset to understand its structure (e.g., point cloud format, annotations, metadata).
 - [ ] Visualize sample point cloud scans
   - [ ] [3D Detection & Tracking Viewer](https://github.com/hailanyi/3D-Detection-Tracking-Viewer): 3D detection and tracking viewer (visualization) for kitti & waymo dataset
 - [ ] 

### key words

__`dat.`__: dataset &emsp; | &emsp; __`cls.`__: classification &emsp; | &emsp; __`rel.`__: retrieval &emsp; | &emsp; __`seg.`__: segmentation     
__`det.`__: detection &emsp; | &emsp; __`tra.`__: tracking &emsp; | &emsp; __`pos.`__: pose &emsp; | &emsp; __`dep.`__: depth     
__`reg.`__: registration &emsp; | &emsp; __`rec.`__: reconstruction &emsp; | &emsp; __`aut.`__: autonomous driving     
__`oth.`__: other, including normal-related, correspondence, mapping, matching, alignment, compression, generative model...

### popular datsets
- [[ModelNet](http://modelnet.cs.princeton.edu/)] The Princeton ModelNet . [__`cls.`__]
- [[ShapeNet](https://www.shapenet.org/)]  A collaborative dataset between researchers at Princeton, Stanford and TTIC. [__`seg.`__]
- [[S3DIS](http://buildingparser.stanford.edu/dataset.html#Download)] The Stanford Large-Scale 3D Indoor Spaces Dataset. [__`seg.`__]
- [[ScanNet](http://www.scan-net.org/)] Richly-annotated 3D Reconstructions of Indoor Scenes. [__`cls.`__ __`seg.`__]
- [[SUNRGB-D](http://rgbd.cs.princeton.edu/challenge.html)] 19 object categories for predicting a 3D bounding box in real world dimension. [__`det.`__]
- [[Large-Scale Point Cloud Classification Benchmark(ETH)](http://www.semantic3d.net/)] This benchmark closes the gap and provides a large labelled 3D point cloud data set of natural scenes with over 4 billion points in total. [__`cls.`__]
- [[Paris-Lille-3D](http://rgbd.cs.princeton.edu/challenge.html)] A large and high-quality ground truth urban point cloud dataset for automatic segmentation and classification. [__`cls.`__ __`seg.`__]
- [[KITTI](http://www.cvlibs.net/datasets/kitti/)] The KITTI Vision Benchmark Suite. [__`det.`__]
- [Waymo Open Dataset](https://waymo.com/open/about/)
- [ONCE 3D Object Detection Baselines](https://once-for-auto-driving.github.io/)
- [NuScenes 3D Object Detection](https://www.nuscenes.org/)
- [L-CAS 3D Point Cloud People Dataset](https://lcas.lincoln.ac.uk/wp/research/data-sets-software/l-cas-3d-point-cloud-people-dataset/)
- [Sydney Urban Objects Dataset](https://www.acfr.usyd.edu.au/papers/SydneyUrbanObjectsDataset.shtml)
- [IQmulus & TerraMobilita Contest](https://data.ign.fr/benchmarks/UrbanAnalysis/#Description)

### other datasets
- [[PartNet](https://shapenet.org/download/parts)] The PartNet dataset provides fine grained part annotation of objects in ShapeNetCore. [__`seg.`__]
- [[PartNet](http://kevinkaixu.net/projects/partnet.html)] PartNet benchmark from Nanjing University and National University of Defense Technology. [__`seg.`__]

- [[Stanford 3D](https://graphics.stanford.edu/data/3Dscanrep/)] The Stanford 3D Scanning Repository. [__`reg.`__]
- [[UWA Dataset](http://staffhome.ecm.uwa.edu.au/~00053650/databases.html)] . [__`cls.`__ __`seg.`__ __`reg.`__]
- [[Princeton Shape Benchmark](http://shape.cs.princeton.edu/benchmark/)] The Princeton Shape Benchmark.
- [[SYDNEY URBAN OBJECTS DATASET](http://www.acfr.usyd.edu.au/papers/SydneyUrbanObjectsDataset.shtml)] This dataset contains a variety of common urban road objects scanned with a Velodyne HDL-64E LIDAR, collected in the CBD of Sydney, Australia. There are 631 individual scans of objects across classes of vehicles, pedestrians, signs and trees. [__`cls.`__ __`match.`__]
- [[ASL Datasets Repository(ETH)](https://projects.asl.ethz.ch/datasets/doku.php?id=home)] This site is dedicated to provide datasets for the Robotics community with the aim to facilitate result evaluations and comparisons. [__`cls.`__ __`match.`__ __`reg.`__ __`det`__]

- [[Robotic 3D Scan Repository](http://asrl.utias.utoronto.ca/datasets/3dmap/)] The Canadian Planetary Emulation Terrain 3D Mapping Dataset is a collection of three-dimensional laser scans gathered at two unique planetary analogue rover test facilities in Canada.  
- [[Radish](http://radish.sourceforge.net/)] The Robotics Data Set Repository (Radish for short) provides a collection of standard robotics data sets.
- [[IQmulus & TerraMobilita Contest](http://data.ign.fr/benchmarks/UrbanAnalysis/#)] The database contains 3D MLS data from a dense urban environment in Paris (France), composed of 300 million points. The acquisition was made in January 2013. [__`cls.`__ __`seg.`__ __`det.`__]
- [[Oakland 3-D Point Cloud Dataset](http://www.cs.cmu.edu/~vmr/datasets/oakland_3d/cvpr09/doc/)] This repository contains labeled 3-D point cloud laser data collected from a moving platform in a urban environment.
- [[Robotic 3D Scan Repository](http://kos.informatik.uni-osnabrueck.de/3Dscans/)] This repository provides 3D point clouds from robotic experiments，log files of robot runs and standard 3D data sets for the robotics community.
- [[Ford Campus Vision and Lidar Data Set](http://robots.engin.umich.edu/SoftwareData/Ford)] The dataset is collected by an autonomous ground vehicle testbed, based upon a modified Ford F-250 pickup truck. 
- [[The Stanford Track Collection](https://cs.stanford.edu/people/teichman/stc/)] This dataset contains about 14,000 labeled tracks of objects as observed in natural street scenes by a Velodyne HDL-64E S2 LIDAR.
- [[PASCAL3D+](http://cvgl.stanford.edu/projects/pascal3d.html)] Beyond PASCAL: A Benchmark for 3D Object Detection in the Wild. [__`pos.`__ __`det.`__]
- [[3D MNIST](https://www.kaggle.com/daavoo/3d-mnist)] The aim of this dataset is to provide a simple way to get started with 3D computer vision problems such as 3D shape recognition. [__`cls.`__]
- [[WAD](http://wad.ai/)] This dataset is provided by Baidu Inc.
- [[nuScenes](https://d3u7q4379vrm7e.cloudfront.net/object-detection)] The nuScenes dataset is a large-scale autonomous driving dataset.
- [[PreSIL](https://uwaterloo.ca/waterloo-intelligent-systems-engineering-lab/projects/precise-synthetic-image-and-lidar-presil-dataset-autonomous)] Depth information, semantic segmentation (images), point-wise segmentation (point clouds), ground point labels (point clouds), and detailed annotations for all vehicles and people. [[paper](https://arxiv.org/abs/1905.00160)] [__`det.`__ __`aut.`__]
- [[3D Match](http://3dmatch.cs.princeton.edu/)] Keypoint Matching Benchmark, Geometric Registration Benchmark, RGB-D Reconstruction Datasets. [__`reg.`__ __`rec.`__ __`oth.`__]
- [[BLVD](https://github.com/VCCIV/BLVD)] (a) 3D detection, (b) 4D tracking, (c) 5D interactive event recognition and (d) 5D intention prediction. [[ICRA 2019 paper](https://arxiv.org/abs/1903.06405v1)] [__`det.`__ __`tra.`__ __`aut.`__ __`oth.`__]
- [[PedX](https://arxiv.org/abs/1809.03605)] 3D Pose Estimation of Pedestrians, more than 5,000 pairs of high-resolution (12MP) stereo images and LiDAR data along with providing 2D and 3D labels of pedestrians. [[ICRA 2019 paper](https://arxiv.org/abs/1809.03605)] [__`pos.`__ __`aut.`__]
- [[H3D](https://usa.honda-ri.com/H3D)] Full-surround 3D multi-object detection and tracking dataset. [[ICRA 2019 paper](https://arxiv.org/abs/1903.01568)] [__`det.`__ __`tra.`__ __`aut.`__]
- [[Argoverse BY ARGO AI]](https://www.argoverse.org/) Two public datasets (3D Tracking and Motion Forecasting) supported by highly detailed maps to test, experiment, and teach self-driving vehicles how to understand the world around them.[[CVPR 2019 paper](http://openaccess.thecvf.com/content_CVPR_2019/html/Chang_Argoverse_3D_Tracking_and_Forecasting_With_Rich_Maps_CVPR_2019_paper.html)][__`tra.`__ __`aut.`__]
- [[Matterport3D](https://niessner.github.io/Matterport/)] RGB-D: 10,800 panoramic views from 194,400 RGB-D images. Annotations: surface reconstructions, camera poses, and 2D and 3D semantic segmentations. Keypoint matching, view overlap prediction, normal prediction from color, semantic segmentation, and scene classification. [[3DV 2017 paper](https://arxiv.org/abs/1709.06158)] [[code](https://github.com/niessner/Matterport)] [[blog](https://matterport.com/blog/2017/09/20/announcing-matterport3d-research-dataset/)]
- [[SynthCity](https://arxiv.org/abs/1907.04758)] SynthCity is a 367.9M point synthetic full colour Mobile Laser Scanning point cloud. Nine categories. [__`seg.`__ __`aut.`__]
- [[Lyft Level 5](https://level5.lyft.com/dataset/?source=post_page)] Include high quality, human-labelled 3D bounding boxes of traffic agents, an underlying HD spatial semantic map. [__`det.`__ __`seg.`__ __`aut.`__]
- [[SemanticKITTI](http://semantic-kitti.org)] Sequential Semantic Segmentation, 28 classes, for autonomous driving. All sequences of KITTI odometry labeled. [[ICCV 2019 paper](https://arxiv.org/abs/1904.01416)][__`seg.`__ __`oth.`__ __`aut.`__]
- [[The Waymo Open Dataset](https://waymo.com/open/)] The Waymo Open Dataset is comprised of high resolution sensor data collected by Waymo self-driving cars in a wide variety of conditions.[__`det.`__]
- [[A*3D: An Autonomous Driving Dataset in Challeging Environments](https://github.com/I2RDL2/ASTAR-3D)] A*3D: An Autonomous Driving Dataset in Challeging Environments.[__`det.`__]


### references

- [Yochengliu/awesome-point-cloud-analysis: A list of papers and datasets about point cloud analysis (processing)](https://github.com/Yochengliu/awesome-point-cloud-analysis)
- [timzhang642/3D-Machine-Learning: A resource repository for 3D machine learning](https://github.com/timzhang642/3D-Machine-Learning)
- [Dataset from Yulan Guo's Homepage](http://yulanguo.me/dataset.html)

## Models

## Model To-Do List

### To-Dos
 - [ ] Research state-of-the-art models for 3D point cloud detection, recognition, and tracking (e.g., PointPillars, PV-RCNN, CenterPoint).
   - [ ] [Person-MinkUNet](https://github.com/VisualComputingInstitute/Person_MinkUNet?tab=readme-ov-file): 3D Person Detection with LiDAR Point Cloud
   - [ ] [PV-CNN](https://github.com/mohamed-said-ibrahem/PV-RCNN_Point-Voxel-Feature-Set-Abstraction-For-3D-Object-Detection/tree/master)
   - [ ] [OpenPCDet](https://github.com/open-mmlab/OpenPCDet)
   - [ ] [PointRCNN](https://arxiv.org/abs/1812.04244)
   - [ ] [Part-A2-Net](https://arxiv.org/abs/1907.03670)
   - [ ] [PV-RCNN](https://arxiv.org/abs/1912.13192)
   - [ ] [Voxel R-CNN](https://arxiv.org/abs/2012.15712)
   - [ ] [PV-RCNN++](https://arxiv.org/abs/2102.00463)
   - [ ] [MPPNet](https://arxiv.org/abs/2205.05979)
   - [ ] [Contains implementations of models which used 3D Object Detection on nuScenes](https://paperswithcode.com/sota/3d-object-detection-on-nuscenes)
   - [ ] [EA-LSS: Edge-aware Lift-splat-shot Framework for 3D BEV Object Detection](https://paperswithcode.com/paper/ea-bev-edge-aware-bird-s-eye-view-projector)
   - [ ] [kaggle competition: Lyft 3D Object Detection for Autonomous Vehicles](https://www.kaggle.com/competitions/3d-object-detection-for-autonomous-vehicles/data): contains codes of participants
   - [ ] [kaggle competition KITTI-3D-Object-Detection-Dataset](https://www.kaggle.com/datasets/garymk/kitti-3d-object-detection-dataset/code): contains codes of participants
   - [ ] and others
 - [ ] Compare models based on their strengths, weaknesses, and suitability for the project.
 - [ ] Select the primary models to implement (e.g., PointPillars for real-time performance, PV-RCNN for accuracy ...).
 - [ ] Document the rationale behind model selection for future reference.
 - [ ] Document what kind of data format required for model training
 - [ ] implement models of find code from `gh`, `papers with code`, `kaggle`
 - [ ] Evaluate model performance on the validation set using relevant metrics (e.g., precision, recall, F1 score, IoU).
 - [ ] Compare results from different models to determine the best-performing architecture.
 - [ ] Identify and analyze failure cases (e.g., missed detections, misclassifications).
 - [ ] Log and track model performance metrics for each model tested.
 - [ ] Implement multi-object tracking using models like AB3DMOT or integrate tracking into the detection pipeline.


Person-MinkUNet