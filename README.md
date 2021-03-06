# Scar-Detection

## SCARS DETECTION USING YOLO V5 MODEL 

#### Aim - 
To create a scars detection which will detect the type of scars.

#### Objectives -

The main objective of the project is to create a program which can be either run on Jetson nano or any pc with YOLOv5 installed and start detecting using the camera module on the device.

Using appropriate datasets for recognizing and interpreting data using machine learning.

To identify scars based on in the input skin images texture analysis based on threshold and neural network to detect.

#### Abstract –
Object detection is a computer vision method that deals with the tasks of localizing and classifying objects within an image. The number of usages for 
the method is constantly growing, and this thesis investigates the unexplored area of using YOLO V5 for scar detection.

We have completed this project on jetson nano which is a very small computational device.

A lot of research is being conducted in the field of Computer Vision and Machine Learning (ML), where machines are trained to identify various objects from one another. Machine Learning provides various techniques through which various objects can be detected.

One such technique is to use YOLOv5 with Roboflow model, which generates a small size trained model and makes ML integration easier.

#### Introduction   -

This thesis will investigate the unexplored area of using YOLO V5 for scar detection.

This project is based on a scars detection model with modifications. We are going to implement this project with Machine Learning and this project can be even run on jetson nano which we have done.

This project can also be used to gather information about scars,
i.e., clear or damage

Scars can be classified into Fine line scars, Hypertrophic scar , Pitted scar , Keloid scar , Scar Construct  based on the image annotation we give in roboflow.

Neural networks and machine learning have been used for these tasks and have obtained good results.

Machine learning algorithms have proven to be very useful in pattern recognition and classification, and hence can be used for scars detection as well.

#### Literature Review –

This project is based on a scars detection model with modifications. We are going to implement this project with Machine Learning and this project can be even run on jetson nano which we have done.

Scars can be classified into Fine line scar , Hypertrophic scar , Pitted scar , Keloid scar , Scar Construct  based on the image annotation we give in roboflow.

Neural networks and machine learning have been used for these tasks and have obtained good results.

#### Jetson Nano Compatibility  -

The power of modern AI is now available for makers, learners, and embedded developers everywhere.

• NVIDIA® Jetson Nano™ Developer Kit is a small, powerful computer that lets you run multiple neural networks in parallel for applications like image 
classification, object detection, segmentation, and speech processing. All in an easy-to-use platform that runs in as little as 5 watts.

• Hence due to ease of process as well as reduced cost of implementation we have used Jetson nano for model detection and training.

• NVIDIA JetPack SDK is the most comprehensive solution for building end-to-end accelerated AI applications. All Jetson modules and developer kits are supported by JetPack SDK.

• In our model we have used JetPack version 4.6 which is the latest production release and supports all Jetson modules.
Proposed System  - 

• Study basics of machine learning and image recognition.

• Start with implementation
    Front-end development

    Back-end development

• Testing, analysing and improvising the model. An application using python and Roboflow and its machine learning libraries will be using machine    learning to identify the scars of the skin.
   
• Use datasets to interpret the scars and suggest whether the skin are clean or damage.

#### Methodology  -

The scars detection system is a program that focuses on implementing real time scars detection. 

This Module is divided into two parts:

#### 1] scars detection 

Ability to detect the scar on skin in any input image or frame. The output is the bounding box coordinates on the detected scars.
This Datasets identifies scars in a Bitmap graphic object and returns the bounding box image with annotation of scars name present in a given image.

#### 2] clear skin Detection

Classification of the scars based on whether it is clean.

Hence YOLOv5 which is a model library from roboflow for image classification and vision was used.

There are other models as well but YOLOv5 is smaller and generally easier to use in production. Given it is natively implemented in PyTorch (rather than 
Dark net), modifying the architecture and exporting and deployment to many environments is straightforward.

YOLOv5 was used to train and test our model for various classes like clean, damage. We trained it for 299 epochs and achieved an accuracy of approximately 91%.

#### Jetson Nano 2GB Developer Kit.


![IMG_20220125_115121](https://user-images.githubusercontent.com/98605645/169959421-36875c0e-743f-4112-9d19-23cb16c4d8c2.jpg)

 
 



## Installation

#### Initial Configuration

```bash
sudo apt-get remove --purge libreoffice*
sudo apt-get remove --purge thunderbird*

```
#### Create Swap 
```bash
udo fallocate -l 10.0G /swapfile1
sudo chmod 600 /swapfile1
sudo mkswap /swapfile1
sudo vim /etc/fstab
# make entry in fstab file
/swapfile1	swap	swap	defaults	0 0
```
#### Cuda env in bashrc
```bash
vim ~/.bashrc

# add this lines
export PATH=/usr/local/cuda/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATh=/usr/local/cuda/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
export LD_PRELOAD=/usr/lib/aarch64-linux-gnu/libgomp.so.1

```
#### Update & Upgrade
```bash
sudo apt-get update
sudo apt-get upgrade
```
#### Install some required Packages
```bash
sudo apt install curl
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
sudo python3 get-pip.py
sudo apt-get install libopenblas-base libopenmpi-dev
```
#### Install Torch
```bash
curl -LO https://nvidia.box.com/shared/static/p57jwntv436lfrd78inwl7iml6p13fzh.whl
mv p57jwntv436lfrd78inwl7iml6p13fzh.whl torch-1.8.0-cp36-cp36m-linux_aarch64.whl
sudo pip3 install torch-1.8.0-cp36-cp36m-linux_aarch64.whl

#Check Torch, output should be "True" 
sudo python3 -c "import torch; print(torch.cuda.is_available())"
```
#### Install Torchvision
```bash
git clone --branch v0.9.1 https://github.com/pytorch/vision torchvision
cd torchvision/
sudo python3 setup.py install
```
#### Clone Yolov5 
```bash
git clone https://github.com/ultralytics/yolov5.git
cd yolov5/
sudo pip3 install numpy==1.19.4

#comment torch,PyYAML and torchvision in requirement.txt

sudo pip3 install --ignore-installed PyYAML>=5.3.1
sudo pip3 install -r requirements.txt
```
#### Download weights and Test Yolov5 Installation on USB webcam
```bash
sudo python3 detect.py
sudo python3 detect.py --weights yolov5s.pt  --source 0
```
## Scar Dataset Training

### We used Google Colab And Roboflow

#### train your model on colab and download the weights and pass them into yolov5 folder.


## Running Scar Detection Model
source '0' for webcam

```bash
!python detect.py --weights best.pt --img 416 --conf 0.1 --source 0
```
## Demo







https://www.youtube.com/watch?v=hmHtYewCTj4










#### Advantages -

The Floor detection system will be of great advantage where a user has lack of time, motivation, unwell or differently abled.

It will be useful to users who are very busy because of work or are because of prior schedules.

Just place the viewfinder showing the skin on screen and it will detect it.

It might be easy to find the scar.

#### Application -

Detects marks and discoloration of skin in a given image frame or viewfinder using a camera module.

Can be used to detect scars of skin when used with proper hardware like machines which can clean.

Can be used as a reference for other ai models based on skin disease detection.

#### Future Scope -

As we know technology is marching towards automation, so this project is one of the step towards automation.
Thus, for more accurate results it needs to be trained for more images, and for a greater number of epochs.

#### Conclusion -

In this project our model is trying to find the unwanted legions on face, marks, pigmentation, discoloration blister on over all body called as a unclear skin.

This model helps to solve the problems which is commonly faced by people in daily routing. It may easy   work on the problem solving for the people in daily life style to control the morbidity level.

#### Reference -

1]Roboflow :- https://roboflow.com/

2] Google images




