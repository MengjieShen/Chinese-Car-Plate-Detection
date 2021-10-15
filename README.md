# Chinese-Car-Plate-Detection
Final project for Machine learning Course

This project aims at building an end-to-end Chinese car-plate detection and recognition system using deep neural net- works. The project is divided into two parts: car-plate detection and character recognition. In the first stage of the system, we would customize the YOLOv5 object detection model to locate the bounding box coordinates and take the sub-image containing the car-plate. Then, we would conduct pre-processing on the sub- image: pre-scaling the images, transforming to grayscale images, and drawing contours of each character in the car-plate. The main contribution of this project is that we perform a modified version of LeNet 5 CNN to recognize the Chinese character and apply pytesseract to recognize the numerals and alphabets.

## Data preprocessing and augmentation
The data set we will be using in the project is from a GitHub open source project, which mainly consists of images that were taken by digital cameras, with various dimensions, in different places and times. As a standard Chinese car plate consists of one character and a string of alphabets and numbers, below is an illustration of a sample image in the data set we found:

![alt text](https://github.com/MengjieShen/Chinese-Car-Plate-Detection/blob/aa683184dcdae3f51364a30010ffc4bfa8546e50/dataset/images/train/%E4%BA%ACH99999.jpg?raw=true)

In addition, before feeding our data set into text recognition models, we would conduct a series of pre-processing procedures to increase the recognition accuracy. The pre-processing procedure is divided into three parts: 
#### Training the car plate detector to find the rough location of the car plate 
#### detect the edges of the area and locate the vertices of the rectangle 
#### apply perspective transformation to obtain the flattened image of the car plate.

## Methodology for character recognition

This includes:
#### Tesseract for Number and Alphabet Recognition
#### Modified LeNet for Chinese Character Recognition
