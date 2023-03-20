# Edge AI based Decision support system for Traffic Control

 **Edge AI based Decision support system for Traffic Control** is an helpful tool for traffic cops to analyze the traffic using ML and IoT.

![](https://miro.medium.com/v2/resize:fit:4800/format:webp/1*HF_Bjk4gMPohESQggXaW7g.jpeg)


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


![2 OP](https://user-images.githubusercontent.com/118420309/226319816-9d528b24-e86a-43ff-9088-4cd7869eee01.png)
![1 op](https://user-images.githubusercontent.com/118420309/226319835-aa773d40-f714-4004-8d85-157681f648fe.png)
![3OP](https://user-images.githubusercontent.com/118420309/226319840-7a083950-93e6-4ad7-9586-761b0ec3b028.png)
![4OP](https://user-images.githubusercontent.com/118420309/226319846-e29b74dd-ebb1-4399-b39c-bb8f9cc39207.png)



# 05 Bonus — Streamlit App

Wouldn’t it be great if we could use this app in the web. We could just upload image of a crop and it gives the areas where weed is present. We can do exactly that using streamlit.

![](https://miro.medium.com/max/1200/1*bkMoiV4ErVFkZ355Ay9CfA.gif)

For a more detailed explanation of coding in streamlit, take a look at this  [article](https://pub.towardsai.net/deep-learning-a692669f6f42), and go to the section  _Hosting As a Streamlit Application (Locally and then in the cloud)._ The code follows a similar pattern and can be found in  [github](https://github.com/ashhadulislam/medium_weedVcrop-main)  and the running app can be found  [here](https://ashhadulislam-medium-weedvcrop-main-main-ppo37r.streamlit.app/).

First we have shown how a single image can be processed by different yolo models and the corresponding results as shown in the gif below.

![](https://miro.medium.com/max/1200/1*YJFfygi_4JR5fDdKNIhoEQ.gif)

Single image processed by different yolov8 models

However, you might need to upload a set of images and apply the models on them. In that case, it would be tedious to drag and drop every image one by one. Rather, we have another page in the same application where you can drag and drop a zip file containing multiple images.

![](https://miro.medium.com/max/1200/1*0BDHmo-iISYYQWNHTa9qfg.gif)

Processing zipped files

You can even choose the from a list of models (yolov8 — nano, small, medium and large). You will get a zipped file containing folders corresponding to each model with a set of result in each.
