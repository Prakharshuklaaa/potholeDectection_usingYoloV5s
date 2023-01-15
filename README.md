
# Object Detetcion by YOLOv5
YOLO, an acronym for "You Only Look Once," is an algorithm that detects and recognizes various objects in a picture in real-time. Object detection in YOLO is done as a regression problem, providing the class probabilities of the detected images. This algorithm utilizes convolutional neural networks (CNN) to detect objects quickly and efficiently. As the name implies, YOLO requires only a single forward propagation through a neural network to detect objects, making the prediction of the entire image possible in a single algorithm run.

YOLO has several variants, including tiny YOLO and YOLOv3, which are both widely used. This algorithm is a powerful tool for object detection, allowing for quick and accurate recognition of objects in images.




## What is YOLOv5 ?
YOLOv5 is the latest object detection model developed by ultralytics, the same company that developed the Pytorch version of YOLOv3, and was released in June 2020.

YOLOv5 is available in four models namely s (small), m (medium), l (large) and x (extra large), each model has different accuracy and performance. Each model takes different time to train.


## YOLOv5 Architecture
As we all know YOLOv5 is designed for object detection, which involves creating features from input images. These features are then fed through a prediction system to draw boxesaround objects and predict their classes

The YOLO network consists of three main pieces:

1. Backbone
2. Neck
3. Head
## Working of YOLO

Explaining the working of YOLO with help of an example:

Suppose we have been given a task to detect pothole in a image or video

1. ![App Screenshot](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/test_04.jpg?raw=true)

2. ![App Screenshot](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/result_04.jpg?raw=true)

The algorithm of YOLO works in a step wise manner:

1. **Residual blocks**: First, we will divide our image into an N x N grid of equal size cells. Each cell in the grid is responsible for predicting the class of the object it covers, along with the associated probability or confidence value. This approach allows us to accurately identify objects in an image with greater precision and confidence value

2. **Bounding box regression**: The next step is to identify the bounding boxes, which are rectangles that outline all the objects in the image. We can have as many bounding boxes as there are objects in a given image. YOLO then uses a single regression module to determine the characteristics of these bounding boxes.

3. **Intersection Over Unions (IOU)**: Most of the time, a single object in an image can have multiple grid box candidates for prediction, though not all of them are relevant. The goal of the Intersection over Union (IoU) metric, which is a value between 0 and 1, is to filter out such grid boxes and only retain those that are pertinent.
4. **Non-Max Suppression or NMS**: Setting a threshold for the IOU is not always sufficient, as an object can have multiple boxes with IOUs beyond the threshold, which may include noise. To combat this, we can use Non-Maximum Suppression (NMS) to retain only the boxes with the highest probability score of detection.
## Result

We have successfully implemented the modified version of YOLOv5s for pothole detection. Our results show that the algorithm has accurately detected potholes on our created dataset. The F1-Confidence curve, PR_curve, P_curve, and R_curve all demonstrate the efficacy of our model, making it a viable option for automated pothole detection applications. Moreover, when tested on a dataset of more than 3000 images, the model revealed considerable improvements in both precision and recall rates, further demonstrating its efficiency in the task. Therefore, we can confidently conclude that YOLOv5 is an effective method for automated detection of potholes on roads and other surfaces.

1. F1-Confidence curve ![F1-Confidence curve](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/F1_curve.png?raw=true)
2. PR_curve ![PR_curve](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/PR_curve.png?raw=true)
3. P_curve  ![P_curve](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/P_curve.png?raw=true)
4. R_curve  ![R_curve](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/results/R_curve.png?raw=true)


- For code [Click Here](https://github.com/Prakharshuklaaa/potholeDectection_usingYoloV5s/blob/main/YOLOV5_modified.ipynb)
- For dataset and modified.yaml file [LinkedIn](https://www.linkedin.com/in/prakhar-shukla-91aaa0202/)
