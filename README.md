# Object detection using deep learning with OpenCV and Python 

OpenCV `dnn` module supports running inference on pre-trained deep learning models from popular frameworks like Caffe, Torch and TensorFlow. 

When it comes to object detection, popular detection frameworks are
 * YOLO
 * SSD
 * Faster R-CNN
 
 Support for running YOLO/DarkNet has been added to OpenCV dnn module recently. 
 
 ## Dependencies
  * opencv
  * numpy
  
`pip install numpy opencv-python`

**Note: Compatability with Python 2.x is not officially tested.**

 ## YOLO (You Only Look Once)
 
 Download the pre-trained YOLO v3 weights file from this [link](https://pjreddie.com/media/files/yolov3.weights) and place it in the current directory or you can directly download to the current directory in terminal using
 
 `$ wget https://pjreddie.com/media/files/yolov3.weights`
 
 Provided all the files are in the current directory, below command will apply object detection on the input image `dog.jpg`.
 
 `$ python yolo_opencv.py --image dog.jpg --config yolov3.cfg --weights yolov3.weights --classes yolov3.txt`
 
 
 **Command format** 
 
 _$ python yolo_opencv.py --image /path/to/input/image --config /path/to/config/file --weights /path/to/weights/file --classes /path/to/classes/file_
 
 
 
 ## Sample output:
 ![complex_yolo_architecture](https://user-images.githubusercontent.com/71749153/236652919-efab4115-d12f-473d-9854-1e930080bb7f.png)
 ![](object-detection.jpg)
 
 
 ## Process Flow Diagram 
 ![System-overview-of-object-recognition-in-video](https://github.com/dhruvaop/Object-Detection-For-Autonomous-Vehicles-using-SYCL-DPC-/assets/71749153/1e6d5b65-b05d-4406-a37e-562616a3f45f)
 
 ## Architecture Diagram
 ![Screenshot 2023-05-20 004140](https://github.com/dhruvaop/Object-Detection-For-Autonomous-Vehicles-using-SYCL-DPC-/assets/71749153/06e0983d-a007-4514-800c-b4effaf13ac2)

 
Checkout the object detection implementation available in [cvlib](http:cvlib.net) which enables detecting common objects in the context through a single function call `detect_common_objects()`.
 
 
 (_SSD and Faster R-CNN examples will be added soon_)
