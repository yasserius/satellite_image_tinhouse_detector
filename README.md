# Tin House Detection from Satellite/Aerial Images

[![TensorFlow 2.x](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow)](https://github.com/tensorflow/tensorflow/releases/tag/v2.1.2)

Detection of tin houses from satellite/aerial images, trained using the Tensorflow 2 Object Detection API.

Satellite images are rich with information about people and the Earth. The latest advancements in deep learning and object detection has allowed very accurate analysis of satellite images. This project is a proof-of-concept of how satellite images can be applied to understand rural Bangladesh better. The project have a lot of potential in revealing various insights about villages in Bangladesh.

<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/poster.png?raw=true" height=300px>

# Demo

The Jupyter notebook for inference using the pretrained model: [[Github]](https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/inference.ipynb) | [[Colab]](https://colab.research.google.com/github/yasserius/satellite_image_tinhouse_detector/blob/main/inference.ipynb)

# Dataset

* Google Drive link to dataset: [[Train]](https://drive.google.com/drive/folders/1Rn8xcyczl1cUinarS99K0LysUk8zqwpW?usp=sharing) - [[Validation]](https://drive.google.com/drive/folders/1--iWbI43MKuK6WYbj5Q3337L3BN6NnMm?usp=sharing)
* The satellite images were screenshotted from Google Maps.
* There are a total of 1260 images, with a training set of 1134 images and validation set of 126 images.
* The images are 500x500 PNG images.
* The labels are in XML files (PASCAL VOC format) with the same name as the corresponding image file, and were labelled using [labelImg](https://github.com/tzutalin/labelImg).

# How to train

The Jupyter notebook for training: [[Github]](https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/training.ipynb) | [[Colab]](https://colab.research.google.com/github/yasserius/satellite_image_tinhouse_detector/blob/main/training.ipynb)

The notebook contains detailed instructions and a link to the data.
The training was done using the Tensorflow 2 Object Detection API.

# Wrong Detections
See all 128 test output images: [Google Drive](https://drive.google.com/drive/folders/1Mbgk4ga5AqiwxFoQ9OJjuIBLIB7i0kb-?usp=sharing)
## Missed detections
<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/bad_1.png?raw=true">
<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/bad_3.png?raw=true">
<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/bad_4.png?raw=true">

## Double counting the same house
<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/bad_2.png?raw=true">

## False positive
<img src="https://github.com/yasserius/satellite_image_tinhouse_detector/blob/main/images/bad_5.png?raw=true">

# How to improve detection
* Train on larger dataset. (Active learning is a very good option.)
* Use image augmentations like change in brightness, contrast, random crops and rotations.
