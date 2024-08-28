# Thermal-NeRF
The official dataset for our paper: [**Thermal-NeRF: Neural Radiance Fields from an Infrared Camera**](https://arxiv.org/abs/2403.10340).
## Self-collected Infrared Dataset 
### 1.1 Description
The dataset utilizes the infrared camera for image collection, with ground truth camera poses recorded using the VICON motion capture system (MoCap) and camera intrinsics obtained through the infrared calibration. It features three distinct scenarios designed to replicate visually degraded environments, including low lighting, fluctuating lighting, and smoke. These scenarios aim to thoroughly evaluate the performance of thermal imaging under challenging conditions. 

### 1.2 Sensor Parameter
* **Infrared Camera:** optris PI 450i, 382*288
* **Rostopics of rosbag sequences:** /optris/thermal_image

### 1.3 Data Format 
- The dataset can be downloaded from [this link](https://drive.google.com/drive/folders/11Xtrd09bIzCifB1hicU9E9lgKrGXFcSB?usp=sharing).

- The data structure of the dataset is shown as below: 
```
/Thermal-NeRF dataset
│
├── /low lighting
│   ├── /sequence_1
│   │   ├── /train
│   │   │   ├── /intrinsics
│   │   │   ├── /pose
│   │   │   └── /rgb
│   │   └── /test
│   │       ├── /intrinsics
│   │       ├── /pose
│   │       └── /rgb
│   ├── /sequence_2
│   ...
│ 
├── /fluctuating lighting
│   ├── /sequence_1
│   ...
│
├── /smoke
│   ├── /sequence_1
│   ...
```
- All the pose data conformes to the **OpenCV** camera convention, adaption should be made if used with the OpenGL camera convention.
