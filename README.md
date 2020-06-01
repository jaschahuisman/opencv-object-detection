![GitHub top language](https://img.shields.io/github/languages/top/jaschahuisman/opencv-object-detection?style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/jaschahuisman/opencv-object-detection?color=light-green&style=plastic)

This opencv realtime object detection script is a simple experimental tool to detect common objects (COCO) easily with your built-in webcam. It uses opencv's readNet method and uses the external yolov3-tiny model (which can be upgraded to the full sized model). Opencv's readNet method only runs on CPU (and not GPU), is very intensive, and therefore, it will be not be optimal for big AI projects. 

> ## See it as just a funny experimental tool, which is not very scalable.

## Installation
* Make sure to install python 3 or higher on your computer.
* Setup a virtual environment and install the dependencies (opencv-python & numpy) from requirements.txt
```bash
python3 -m venv venv
```
```bash
$ pip3 -r install requirements.txt
```
* If you now run `python3 object-detection.py`, your built-in camera will be shown in a new window, and if everything is okay the model will recognise objects, such as people, computers, books etc.
This all will happen on CPU because of opencv, and that's why it is slower than other object-detection software.

## Using other models
If the tiny yolov3 model doesn't work well enough for your project, you might try using other, bigger yolov3 models. It will be a little slower, but more accurate. You can download models from the link below, and put them into the configuration folder, and change the `object-detection.py` script.

```python
net = cv2.dnn.readNet("./weights/[WEIGHT-FILE]", "./configuration/[CONFIG-FILE]")
```

* [Download Yolov3 Models](https://drive.google.com/drive/folders/1LezFG5g3BCW6iYaV89B2i64cqEUZD7e0)
