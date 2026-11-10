# Laboratory Work No. 6 - Working with Open-Source Code

## Project Overview

This project demonstrates the use of the YOLOv7 object detection algorithm for detecting and classifying objects in images.

The project was completed as part of Laboratory Work No. 6. The main goal was to explore an existing open-source machine learning solution, understand its implementation, and run a practical demonstration.

## Research Paper

**Title:** YOLOv7: Trainable Bag-of-Freebies Sets New State-of-the-Art for Real-Time Object Detectors

**Authors:** Chien-Yao Wang, Alexey Bochkovskiy, Hong-Yuan Liao

**Year:** 2022

- [Research Paper (arXiv)](https://arxiv.org/abs/2207.02696)
- [Official YOLOv7 GitHub Repository](https://github.com/WongKinYiu/yolov7)

## About YOLOv7

YOLOv7 is a real-time object detection algorithm based on deep learning.

It can:
- Detect multiple objects in images and videos.
- Classify detected objects into different categories.
- Determine the location of objects using bounding boxes.
- Estimate the confidence score for each detection.

The algorithm uses an improved neural network architecture and training optimization techniques to achieve high detection accuracy and speed.

## Environment

The experiment was performed using Google Colab.

| Component | Configuration |
|---|---|
| Programming language | Python 3.13 |
| Deep learning framework | PyTorch 2.14.1 |
| GPU | NVIDIA Tesla T4 |
| CUDA | 13.0 |
| Object detection model | YOLOv7 |
| Image size | 640 × 640 |
| Confidence threshold | 0.25 |

## Implementation

The official YOLOv7 repository was cloned from GitHub.

The pretrained model `yolov7.pt` was downloaded and used for object detection.

The detection command:

```bash
python detect.py --weights yolov7.pt --conf 0.25 --img-size 640 --source inference/images/horses.jpg --device 0
```

The original implementation required a small compatibility adjustment for loading model weights in the newer PyTorch version.

The complete implementation and execution steps are provided in the Jupyter Notebook included in this repository.

## Results

The model was tested on the `horses.jpg` image.

**Detection results:**
- Detected objects: 5 horses.
- Inference time: 17.8 ms.
- GPU acceleration: NVIDIA Tesla T4.

The resulting image with detected objects and bounding boxes is available in the `results` folder.

## Project Structure

```text
lab6-yolov7-object-detection/
│
├── README.md
├── lab6_yolov7.ipynb
│
└── results/
    └── horses_result.jpg
```

## Possible Improvements

Possible improvements include:
- Using higher-resolution input images.
- Applying image preprocessing techniques.
- Training the model on additional datasets.
- Adjusting the confidence threshold for different detection tasks.

## Conclusion

During this laboratory work, the YOLOv7 object detection algorithm was explored and successfully executed using its open-source implementation.

The experiment demonstrated that the model can detect multiple objects in an image and identify their classes with high processing speed.

The practical result confirmed the successful use of an existing deep learning solution.

