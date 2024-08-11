
# Detection of Personal Protective Equipment (PPE)

Overview

This project focuses on detecting Personal Protective Equipment (PPE) in images and video streams using computer vision techniques. The system identifies whether individuals in a workplace environment are wearing the necessary safety gear, such as helmets, safety vests, gloves, and other PPE, ensuring compliance with safety standards.


## Features

- Real-time Detection: The model processes images or video feeds to detect the presence or absence of PPE.
- High Accuracy: The model is trained on a diverse dataset, ensuring  accurate detection across various environments and lighting conditions.
- Customizable Classes: Ability to detect multiple types of PPE, including helmets, gloves, masks, safety vests, and more.
- Integration Ready: Easily integrable with existing surveillance systems or IoT devices for real-time monitoring.


## Installation

1 Prerequisites

```bash
  Python 3.x
  TensorFlow / PyTorch
  OpenCV
  Other dependencies listed in requirements.txt
```
    
2 Clone the Repository
```bash
git clone https://github.com/yourusername/detection-of-ppe.git
cd detection-of-ppe
```

3 Install Dependencies
```bash
pip install -r requirements.txt
```


## Usage
1 Running the detection on an image:
```bash
python detect_ppe.py --image path_to_image.jpg
```
2 Running the detection on a video stream:

```bash
python detect_ppe.py --video path_to_video.mp4
Real-time detection using a webcam:
```
3 Real-time detection using a webcam:
```bash
python detect_ppe.py --webcam
```

## Code

```bash
├───.ipynb_checkpoints
├───assets
├───data
├───├──data.yaml
├───├──ppe_data.yaml
│   ├───test
│   │   ├───images
│   │   └───labels
│   ├───train
│   │   ├───images
│   │   └───labels
│   └───valid
│       ├───images
│       └───labels
├───models
├───output
│   └───output_yolov8n_100e
├───results
└───source_files
```



## Model Architecture

The model architecture used for PPE detection in this project is designed to balance accuracy and computational efficiency, making it suitable for real-time applications. Below are the key components of the architecture:

- Backbone: The model leverages [Specify the architecture, e.g., ResNet-50, MobileNetV2, YOLOv5] as the backbone for feature extraction. This architecture is chosen for its proven performance in object detection tasks and its ability to capture complex patterns in visual data.

- Detection Head: The detection head is responsible for classifying and localizing PPE items in images. It outputs bounding boxes and class labels for each detected object, ensuring that the model can identify multiple types of PPE simultaneously.

- Training Process: The model is trained using a supervised learning approach on a diverse dataset of images containing various PPE. Key hyperparameters include:

- Optimizer: [Specify optimizer, e.g., Adam or SGD] with a learning rate of [Specify learning rate, e.g., 0.001].

  1 Loss Function: A combination of cross-entropy loss for classification and mean squared error for bounding box regression.

  2 Data Augmentation: Techniques such as random cropping, flipping, and color jittering are employed to enhance the robustness of the model.

  3 Evaluation Metrics: The model's performance is evaluated using metrics such as precision, recall, F1-score, and mean Average Precision (mAP). These metrics provide a comprehensive understanding of the model's detection capabilities across different PPE categories.



## Tests Results 

The PPE detection model has demonstrated strong performance across various test scenarios, achieving high accuracy and reliability. The key results are summarized below:

- Accuracy: The model achieved an overall accuracy of [93%] on the test set, indicating its effectiveness in detecting PPE in diverse environments.

- Precision and Recall: The model achieved a precision of [90%] and a recall of [92%], reflecting its ability to accurately identify PPE while minimizing false positives and negatives.

- mAP (mean Average Precision): The mean Average Precision across all PPE classes is [0.85], indicating strong detection performance for each category.

- Qualitative Results: Visual inspections of the detection outputs show that the model consistently identifies PPE even in challenging conditions, such as occlusions, varying lighting, and complex backgrounds.

These results underscore the model's robustness and suitability for deployment in real-world scenarios where PPE detection is critical.
## contributions

I welcome contributions from the community to enhance the PPE detection system. To contribute, please follow the steps below:

- Fork the Repository: Start by forking the project repository to your GitHub account.

- Create a Feature Branch: Clone your fork and create a new branch for your feature or bug fix:

```bash
git checkout -b feature-branch
```
- Implement Your Changes: Make the necessary changes to the codebase, ensuring that your code adheres to the project's coding standards and practices.

- Commit Your Changes: Write clear, concise commit messages that describe the purpose of your changes:

```bash
git commit -m "Add new feature"
```
- Push to Your Branch: Push your changes to your forked repository:

```bash
git push origin feature-branch
```
- Create a Pull Request: Navigate to the original repository and create a pull request, providing a detailed description of your changes and the problem they address.

- Code Review: Your pull request will be reviewed by the project maintainers. Please be responsive to any feedback or requested changes.

- Merge: Once your changes are approved, they will be merged into the main branch.

By contributing to this project, you help improve the safety and reliability of PPE detection systems used across various industries.
