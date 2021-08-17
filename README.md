# Human-Detection-Counting

In this python project, we are going to build the Human Detection and Counting System through Webcam or you can give your own video or images. This is an intermediate level deep learning project on computer vision, which will help you to master the concepts and make you an expert in the field of Data Science. Let’s build an exciting project.

Building a person counter with OpenCV has been one of the most-requested topics here on the PyImageSearch and I’ve been meaning to do a blog post on people counting for a year now — I’m incredibly thrilled to be publishing it and sharing it with you today.

![](https://d2h0cx97tjks2p.cloudfront.net/blogs/wp-content/uploads/sites/2/2020/07/human-counting-output.jpg)

# Project Prerequisites

The project in Python requires you to have basic knowledge of python programming and the OpenCV library. We will be needing following libraries:

* OpenCV: A strong library used for machine learning
* Imutils: To Image Processing
* Numpy: Used for Scientific Computing. Image is stored in a numpy array.
* Argparse: Used to give input in command line.

**Understanding object detection vs. object tracking**

There is a fundamental difference between object detection and object tracking that you must understand before we proceed with the rest of this tutorial.

When we apply object detection we are determining where in an image/frame an object is. An object detector is also typically more computationally expensive, and therefore slower, than an object tracking algorithm. Examples of object detection algorithms include Haar cascades, HOG + Linear SVM, and deep learning-based object detectors such as Faster R-CNNs, YOLO, and Single Shot Detectors (SSDs).

An object tracker, on the other hand, will accept the input (x, y)-coordinates of where an object is in an image and will:

Assign a unique ID to that particular object
Track the object as it moves around a video stream, predicting the new object location in the next frame based on various attributes of the frame (gradient, optical flow, etc.)
Examples of object tracking algorithms include MedianFlow, MOSSE, GOTURN, kernalized correlation filters, and discriminative correlation filters, to name a few.

**Histogram of Oriented Gradient Descriptor**

HOG is a feature descriptor used in computer vision and image processing for the purpose of object detection. This is one of the most popular techniques for object detection, to our fortune, OpenCV has already been implemented in an efficient way to combine the HOG Descriptor algorithm with Support Vector Machine or SVM.

![](https://www.researchgate.net/publication/315327257/figure/fig5/AS:668320193867782@1536351359258/Methodology-of-image-features-extraction-using-the-histogram-of-oriented-gradients-HOG.png)

![](https://learnopencv.com/wp-content/uploads/2016/12/hog-cell-gradients.png)

# Steps :

* Import the libraries
* Create a model which will detect Humans(HOG)

   cv2.HOGDescriptor_getDefaultPeopleDetector() calls the pre-trained model for Human detection of OpenCV and then we will feed our support vector machine with it.

* Detect() method

  Here, the actual magic will happen.

  Video: A video combines a sequence of images to form a moving picture. We call these images as Frame. So in general we will detect the person in the frame. And show it one after another that it looks like a video.

  That is exactly what our Detect() method will do.  It will take a frame to detect a person in it. Make a box around a person and show the frame..and return the frame with person bounded by a green box.

  Everything will be done by detectMultiScale(). It returns 2-tuple.

  List containing Coordinates of bounding Box of person.
  Coordinates are in form X, Y, W, H.
  Where x,y are starting coordinates of box and w, h are width and height of box respectively.
  Confidence Value that it is a person.
  Now, We have our detect method. Let’s Create a Detector.

* DetectByPathimage() method

  This method is used if a person needs to be detected from an image.

* DetectByPathVideo() method

  This method is very similar to the previous method except we will give a path to the Video. First, we check if the video on the provided path is found or not.
  

  
# Summary
  
 In this deep learning project, we have learned how to create a people counter using HOG and OpenCV to generate an efficient people counter. We developed the project where you can supply the input as: video, image, or even live camera. This is an intermediate level project, which will surely help you in mastering python and deep learning libraries.

