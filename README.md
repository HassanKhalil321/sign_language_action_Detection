## AbstractParser
<div align="center">
  <img src="https://github.com/HassanKhalil321/sign_language_action_Detection/blob/main/assets/model.jpg" width="1000"/>
</div>


## Introduction
Sign Language Action Detection is a deep learning project aimed at recognizing and interpreting sign language gestures from video inputs. This repository contains the implementation of a model that takes videos as input and predicts the corresponding sign language action classes

## Dataset
The WLAS dataset, or Word-Level American Sign Language Dataset, is a specialized collection of video recordings designed for training and evaluating automatic sign language recognition systems. It comprises videos depicting various American Sign Language (ASL) words performed by different signers, capturing the nuances of hand gestures, facial expressions, and body movements. Each video is annotated with ground-truth labels corresponding to the specific ASL word being signed, facilitating supervised learning approaches
## Model Overview

**Input Handling:**
After receiving the video each video will be separated to 25 frames drawing the landmarks of the body on the images before passing it tp our model 

**videos Input Processing:**

- The frames are first passed through our 3 CNN blocks.
- They are then processed through a dense layer 
-  This is followed by a flatten layer and a dropout layer (0.5) before passing it through a dense layer with softmax activation.
-  and end up a classification label like (GO)

## Loss
<div align="center">
  <img src="https://github.com/HassanKhalil321/sign_language_action_Detection/blob/main/assets/CCE.jpg" alt="Gesture Recognition" width="600"/>
</div>
