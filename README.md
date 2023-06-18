# RealTimeObjectDetection
OpenCV provides pre-trained models for object detection, such as Haar cascades deep learning-based models like Single Shot MultiBox Detector (SSD) and You Only Look Once (YOLO). YOLO is a popular object detection algorithm known for its real-time performance. OpenCV provides a convenient way to implement YOLO using its deep neural network (dnn) module.
Load  pre-trained YOLOv3 model (https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg)
Load the class labels from this file. (https://github.com/pjreddie/darknet/blob/master/data/coco.names)
Load the yolo model weight ( https://pjreddie.com/media/files/yolov3.weights)
Set up video stream with webcam
Read frame(image) from video stream
Perform object detection with blobFromImage function which take image frame and preprocess  for the neural network. It resizes the image to the specified size of (416, 416) pixels.The scale factor of  1/255.0 is applied to normalize the pixel values between 0 and 1. Then set this blob to neural network. Then and performs a forward pass to obtain the output predictions.
Process the outputs by predicting from the neural network. It extracts the class ID, confidence score, and bounding box coordinates for each detected object and stores them in lists. These lists will be used later to draw bounding boxes and labels on the objects in the image.
Apply non-maximum suppression to eliminate redundant overlapping boxes.
Labeling on the frame and display these.
[N.B. Put yolov3.cfg, coco.names and yolov3.weights in the same directory where the .py/.ipynb file exist.]
