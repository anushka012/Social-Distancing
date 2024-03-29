# Social-Distancing-Detector
Social Distancing is a method which helps in the control of spread of contagious diseases such as COVID-19 . Though government is taking various safety measures, people are not maintaining social distance. So we at SRM Hackerearth has developed a project which could detect people who are not maintaining social distance. This can be used in crowded places such as malls, railway station, bus stops, etc. 

![my_output](https://user-images.githubusercontent.com/60866104/105572798-66b06c80-5d7f-11eb-8a86-ac7854243800.gif)

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




![BLOG-1](https://user-images.githubusercontent.com/66209295/105576808-64f4a200-5d9b-11eb-8c5d-0fd5d3c3d6a1.jpeg)

![BLOG-3](https://user-images.githubusercontent.com/66209295/105576858-b4d36900-5d9b-11eb-8be3-5ab9158db1be.jpeg)

![BLOG-8](https://user-images.githubusercontent.com/66209295/105576851-aa18d400-5d9b-11eb-8cdc-b02fbceb2d9a.jpeg)





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
<div align="center">
    <a href="https://allcontributors.org">
        <img width="30%" height="50%" src="xd.svg" alt="✨ All Contributors ✨" width="800px" />
    </a>
</div>

</br>

<table>
  <tr>



<td align="center"><a href="https://github.com/anushka012"><img src="https://github.com/SRM-HackerEarth/Social-Distancing/blob/main/images/anushka.jpg?raw=true" width="210px;" height="230px;" alt=""/><br /><sub><b> </b></sub></a><br /><p align="center">
    
   <a href="https://www.linkedin.com/in/anushka-s-b049a2190/" alt="Linkedin"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/linkedin-fill.svg"></a>
    <a href="https://www.linkedin.com/in/anushka-s-b049a2190/" alt="Contact me"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/mail-fill.svg"></a>
    <a href="" alt="My site"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/external-link-line.svg"></a>
  </p>
</td>

<td align="center"><a href="https://github.com/Harikrishnaa3131"><img src="https://github.com/SRM-HackerEarth/Social-Distancing/blob/main/images/hari%20photo.jpg" width="210px;" height="230px;" alt=""/><br /><sub><b> </b></sub></a><br /><p align="center">
    
   <a href="" alt="Linkedin"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/linkedin-fill.svg"></a>
    <a href="" alt="Contact me"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/mail-fill.svg"></a>
    <a href="" alt="My site"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/external-link-line.svg"></a>
  </p>
</td>

<td align="center"><a href="https://github.com/Dineshkumar013"><img src="https://github.com/SRM-HackerEarth/Social-Distancing/blob/main/images/dinesh_photo.jpeg?raw=true" width="210px;" height="230px;" alt=""/><br /><sub><b> </b></sub></a><br /><p align="center">
    
   <a href="" alt="Linkedin"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/linkedin-fill.svg"></a>
    <a href="" alt="Contact me"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/mail-fill.svg"></a>
    <a href="" alt="My site"><img src="https://raw.githubusercontent.com/jayehernandez/jayehernandez/3f5402efef9a0ae89211a6e04609558e862ca616/readme/external-link-line.svg"></a>
  </p>
</td>
      
   </tr>
    </table>




