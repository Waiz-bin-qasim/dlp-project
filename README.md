# Violence Detection and Blur - YOLOv8 & DETR

## Introduction:
This repository contains code for a project focused on detecting violent objects like guns and blood in videos using YOLOv8 and DETR models. The primary goal is to automatically blur these detected objects for sensitive content moderation. The project utilizes Roboflow datasets for training and validation.

## Flow of Model:
1. **Video Processing**: Frames of the video are extracted using OpenCV (cv2).
2. **Object Detection**: YOLOv8 and DETR models are employed to detect violent objects within the frames.
3. **Blur Application**: Detected objects are then blurred using image processing techniques.
4. **Video Reconstruction**: The modified frames are combined to reconstruct the video.

## Dependencies:
- Python 3.x
- OpenCV (cv2)
- YOLOv8
- DETR
- Roboflow dataset

## Installation:
1. Clone this repository:
   ```
   git clone <repo_url>
   cd <repo_directory>
   ```
2. Install dependencies:
   ```
   pip install opencv-python yolov5 torchvision
   ```
3. Obtain necessary model weights and configurations for YOLOv8 and DETR.
4. Prepare Roboflow dataset for training and validation.

## Results:
The project has achieved promising results, with an accuracy of approximately 85% on diverse video datasets. These results demonstrate the efficacy of the YOLOv8 and DETR models in detecting violent objects and applying appropriate blurring techniques.

## Directory Structure:
- **DETR**: Contains the training code for the DETR model and scripts for downloading the dataset from Roboflow.
- **YOLO**: Includes the training code for the YOLO model and scripts for downloading the dataset from Roboflow.
- **main.ipynb**: This notebook comprises the main code responsible for splitting the video into frames, applying the models, blurring the detected objects, and then combining the frames to reconstruct the video.

## Note on Trained Models:
- Trained models for YOLO are present in the `best.pt` file within the YOLO folder. However, the trained model for DETR could not be uploaded due to its large size. Git only allows files up to 50MB in size, whereas the DETR model exceeded this limit with a size of 189MB.

## References:
- [YOLOv8 Ultralytics](https://github.com/ultralytics/YOLOv8)
- [DETR: End-to-End Object Detection with Transformers](https://github.com/facebookresearch/detr)

