# Action and Action Class Prediction: Project Overview

- Aim of the project is to develop Convolutional Neural Network for a multi-output predictions.
- Obtained 3030 training and 2100 testing images containing 21 different actions under 5 action classes.
- Model


## Reference

**Python Version:** 3.6 Google Colab <br/>
**GPU:** NVIDIA Tesla K80 GPU  <br/>
**Packages:** numpy, pandas, seaborn, matplotlib, tensorflow, keras, Image <br/>
**CNN Article:** [F-beta Score in Keras](https://towardsdatascience.com/f-beta-score-in-keras-part-i-86ad190a252f) <br/>
**Metric Article:** [A Simple CNN: Multi Image Classifier](https://towardsdatascience.com/a-simple-cnn-multi-image-classifier-31c463324fa) <br/>


# Introduction

Aim of the study is to develop a deep convolutional neural network (CNN) for a multi-output classifier that can identify the actions of a person from still images.


# Exploratory Data Analysis 

Several Observations can be made from the intitial exploration of these images.

- Images have good similarity to common natural laguage dataset like imagenet. Transfer learning is an option.
- Images have different shapes. These images requires a common shape for transformation.
- Some exmaple images are ambiguous. The final performance for the model may be affected.
- In some images, the important information and features is toward a corner of the image. Data Augmentation needs to be done carefully.

# Model Building

## Feature Extraction

# Error Analysis

