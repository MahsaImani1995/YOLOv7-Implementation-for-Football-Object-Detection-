# YOLOv7 Training and Detection Pipeline

This project demonstrates the process of training and utilizing the YOLOv7 model for object detection on a custom dataset. The steps include data preparation, environment setup, model customization, training, and detection on new videos.

## Data Preparation

### 1. Image Annotation
- Images were categorized into two sets.
- Annotated using labelImg software for six classes: `Portugal`, `Spain`, `Ball`, `Referee`, `Goalkeeper.s`, and `Goalkeeper.p`.

### 2. Dataset Splitting
- Corrected any labeling errors.
- Split the dataset into `train` and `validation` sets with an 80:20 ratio.

## Environment Setup

### 1. Google Drive Integration
- Provided access to Google Drive to save and load necessary files.

### 2. Directory Configuration
- Navigated to `MyDrive`.
- Created and accessed a new directory if it didn't already exist.

### 3. Cloning YOLOv7 Repository
- Cloned the YOLOv7 repository from GitHub into the new directory.
- Changed directory to the `YOLOv7` folder.

### 4. Pre-trained Weights Download
- Downloaded pre-trained weights for YOLOv7x.

## Customizing YOLOv7 for the Dataset

### 1. Data Configuration
- Loaded training data and duplicated the `coco.yaml` file.
- Edited the file to include the custom number of classes and their names.

### 2. Model Configuration
- Edited the `yolov7x.yaml` file in the `cfg/training` directory to match the custom dataset.
- Set parameters: `Epoch` to 32, `BatchSize` to 16, and `ImageSize` to 416x416.

## Model Training

### 1. Initial Training
- Trained the model using the specified data and configurations.

### 2. Saving Trained Weights
- Saved the best weights from the `runs/training/weights` directory to the main `yolov7` folder.

## Object Detection on New Videos

### 1. Video Preparation
- Processed a 4-minute video clip not used in training.
- Uploaded this video to the main directory.

### 2. Running Detection
- Used the `detect.py` script with the best-trained weights and a confidence threshold of 0.25 to detect objects in the video.
- Saved detected results in the `yolov7/runs/detect` directory.

## Additional Notes

- The best training weights and detection scripts are available.
- Example images and labels are provided in the dataset structure, but more labeled images are needed for optimal results.
- You can download the mp4 file separately by clicking on it and selecting download.
- Setting the epoch to 100 and confidence level to 0.5 can improve precision and recall but will require more time and resources.
