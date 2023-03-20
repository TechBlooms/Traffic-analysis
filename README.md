# Edge AI based Decision support system for Traffic Control

 **Edge AI based Decision support system for Traffic Control** is an helpful tool for traffic cops to analyze the traffic using ML and IoT.
                                        <center><img src="https://user-images.githubusercontent.com/118420309/226430850-7a4f9bf3-0e46-4993-82c0-ce4ad6476e75.png" width=400 height =300 > </center>




# 01 Motivation
 
Knowing that traffic officers won’t have the view of the whole traffic, this project has a web-based dashboard to assist traffic officers in making decisions depending on the volume of traffic only by visualizing the count of vehicles from each lane. This would serve as a hybrid way of traffic support to the cop instead of fully automating traffic control.In this project we have also implemented the algorithm using Intel oneAPI Toolkit.

# 02 Setup
We have used intelOneApi devcloud,


# 03 Implementation - Algorithm
Deep Learning Algorithm - Yolov5 + Deepsort with PyTorch
The detections generated by YOLOv5, a family of object detection architectures and models pretrained on the COCO dataset, are passed to a Deep Sort algorithm which tracks the objects. 
For backend, Flask and Jinga was used
For database - Firebase (No-SQL) in cloud and Sqlite in edge was used.


# 04 Deployment of OneAPI
OneAPI is used enable the use of one platform for a range of different hardware, hence it eliminated the need for different languages, tools, and libraries when to code for CPUs and GPUs. 
Openvino was used in this project which helped in optimization of the computer vision packages that were used including OpenCV and other DL packages required for it.

![tool-thumbnail-beta-oneapi-logo](https://user-images.githubusercontent.com/118420309/226315524-f3a075ce-8102-42d6-9199-0189c9589735.jpg)
Implementing OpenVINO  [link](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/download.html)

Steps

Step 1: Create virtual environment
``` bash
python -m venv openvino_env
```
Step 2: Activate virtual environment
``` bash
openvino_env\Scripts\activate
```
Step 3: Upgrade pip to latest version
``` bash
python -m pip install --upgrade pip
```
Step 4: Download and install the package
``` bash
pip install openvino-dev==2022.3.0
```








How to run,


•	Create a virtual environment and activate it
•	Download the packages using the command,
``` bash
pip install -r requirements.txt
```
•	In a terminal, run mainProgram.py
``` bash
python mainProgram.py
```
![OPENVINO_ENV](https://user-images.githubusercontent.com/118420309/226317165-1e3ad93a-a734-420c-b921-dfb87077b5d5.png)


•	In another terminal, run the frontend using the command,

``` bash
python -m flask run
```
![OPENVINO 2](https://user-images.githubusercontent.com/118420309/226316559-6520e8c4-8022-4e85-a035-64980afd5255.png)

•	CTRL + click on the link to open the web dashboard.

 
# 05 Output - Count taken

Real time dataset

<div>

<img src="https://user-images.githubusercontent.com/118420309/226319816-9d528b24-e86a-43ff-9088-4cd7869eee01.png" width=500 height =300> <img src="https://user-images.githubusercontent.com/118420309/226319835-aa773d40-f714-4004-8d85-157681f648fe.png" width=500 height =300>

<img src="https://user-images.githubusercontent.com/118420309/226319840-7a083950-93e6-4ad7-9586-761b0ec3b028.png" width=500 height =300> <img src="https://user-images.githubusercontent.com/118420309/226319846-e29b74dd-ebb1-4399-b39c-bb8f9cc39207.png" width=500 height =300>




Prototype live detection and count
 
 <img src="https://user-images.githubusercontent.com/118420309/226427078-05891c33-41df-45ed-b3dc-e785d750ea46.png" width=500 height =300> <img src="https://user-images.githubusercontent.com/118420309/226427100-6908cea0-8cef-4c67-a8de-effc529b0740.png" width=500 height =300>
 
 <img src="https://user-images.githubusercontent.com/118420309/226427111-d80c6220-3f5e-4bac-aa80-0618113fb422.png" width=500 height =300> <img src="https://user-images.githubusercontent.com/118420309/226427129-fb7f6c7d-b752-441e-8196-f73ac25b3789.png" width=500 height =300>





# 06 Web dashboard
Final view of the Traffic shown in the web dashboard.


![wb1](https://user-images.githubusercontent.com/118420309/226320383-9fbf0c35-a422-4ac8-8ea6-2cd150df685f.png)
![wb2](https://user-images.githubusercontent.com/118420309/226320397-def3e802-d4d3-43e6-b10a-4e78d0845f7b.png)

# 07 Overview of the project
 
 Video [Link](https://youtu.be/-uzCXNjXNBQ)
 
 Drive [Link](https://drive.google.com/drive/folders/1wCd9z_YpQytijO36T0_t2LJWqR4Lclt-?usp=sharing)


