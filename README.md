# Social-Distancing-Detector
Social Distancing is a method which helps in the control of spread of contagious diseases such as COVID-19 . Though government is taking various safety measures, people are not maintaining social distance. So we at SRM Hackerearth has developed a project which could detect people who are not maintaining social distance. This can be used in crowded places such as malls, railway station, bus stops, etc. 

## Requirements
- Numpy
- OpenCV
- Yolov3 weights for coco dataset. You can download it from [here](https://pjreddie.com/darknet/yolo/)

## Features
- Using YOLOV3 object detection model to detect the people.
- Compute the pair-wise distance between all detected people.
- Based on the computed distance, find whether social distancing norm is violated or not.
- Count the number of violations.

## Screenshots


- to be added


## How to get started?
- to be added


## Simple Theory
   ### Object Detection:
   - We will be using YOLOv3, trained on COCO dataset for object detection.
   - YOLO treats object detection as a regression problem, taking a given input image and simultaneously learning bounding box coordinates and corresponding class label probabilities.
   - In general, single-stage detectors like YOLO tend to be less accurate than two-stage detectors (R-CNN) but are significantly faster.
   - It used to detect people, person prediction probability, coordinates of bounding boxes of the people detected, centroid of the bounding box (to calculate distance).  
   ### Distance Calculation:
   - NMS (Non-maxima suppression) is also used to reduce overlapping bounding boxes to only a single bounding box, thus representing the true detection of the object.
   - Euclidean distance is then computed between all pairs of the returned centroids.
   - Check whether the pairwise distance is greater than social distancing norm length.
   - If yes , bound a box about the people with green colored outline.
   - If no , bound a box about the people with red colored outline and increase the count.

## References
- YOLOv3 paper: https://arxiv.org/pdf/1804.02767.pdf
- OpenCV documentation: https://docs.opencv.org/master/

## Community and Contributors
When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change. Please note we have a code of conduct, follow it in all your interactions with the project.

## License
The Project is released under the terms of the [GPL-3.0 License]().

## Contributors
- to be added


