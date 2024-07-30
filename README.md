# Custom Object Detection with YOLOv7

This repository demonstrates the process of training and deploying the YOLOv7 model for custom object detection tasks. Below is a comprehensive guide covering data preparation, model training, and object detection on new videos.

## Data Preparation

### Image Annotation

1. **Dataset Split**: The dataset was divided into two groups.
2. **Annotation**: Using `labelImg`, images were annotated with six categories: Portugal, Spain, Ball, Referee, Goalkeeper.s, and Goalkeeper.p.

### Data Splitting

- After verifying and correcting annotations, the dataset was split into training and validation sets in an 80:20 ratio.

## Setting Up the Environment

### Google Drive Integration

- The initial setup includes granting access to Google Drive for file management.

### Directory Management

1. Change the working directory to `MyDrive`.
2. Create a new directory if it doesn't exist and navigate into it.

### Cloning the YOLOv7 Repository

- Clone the YOLOv7 GitHub repository into the new directory:
  ```sh
  git clone https://github.com/WongKinYiu/yolov7.git
  cd yolov7
