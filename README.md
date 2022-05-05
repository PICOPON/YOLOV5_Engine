# YOLOv5_engine (TensorRT, YOLOV5 6.1, .engine)
## This project is used to deploy the engine model (.engine) generated by YOLOV5 6.1 (export.py) to jetsonnano or running in a separate environment. You only need to install the *tensorRT* framework without *torch*
### You only need to install tensorrt and pycuda for model(.engine) forward prediction. ###
## Prepare ##
- **My environment**
 ```
 CUDA: 11.3.1
 cudnn: 8.2.1
 python:3.9
 ```
- **Installation**
If you use a **Linux** based system, you can easily install by:
```
  pip install -r requirements.py
 ```
else if you use a **Windows**  system, only the installation method of **tensorrt** library  is different, please reference by follow url https://docs.nvidia.com/deeplearning/tensorrt/install-guide/index.html#installing-tar
## Usage ##
- Predict Support **2 MODE**（--source camera or image)
You can easily start by following command.
```
  python yolov5pred.py 
```
Other optional extra parameters：
```
--engine runs/yolov5s.engine  # Trained engine file path
--categories runs/names.txt   # Network prediction class file
--source camera               # camera or image for camera prediction or single image prediction
--conf-thres 0.25             # confidence threshold
--iou-thres 0.1               # iou threshold
```
## Result ##
Prediction results of Windows or Linux platforms:
![image](https://github.com/PICOPON/yolov5_engine/blob/master/output/bus.jpg)
