# Action and Action Class Prediction: Project Overview

- Aim of the project is to develop Convolutional Neural Network for a multi-output predictions.
- Obtained 3030 training and 2100 testing images containing 21 different actions under 5 action classes.
- Since the number of training samples is small of approximate 1940 images, data augmentation is used which is a technique to randomly transform the images to artificially expand the training size.
- Model developed comprised of two parts: one is used as the feature extractor with Transfer Learning that is made up of ‘MobileNetV2’ blocks, and the other is the classifier part which is made up of the fully connected layers and the output layer with Softmax as the chosen activation function for the final layer. 
- Model achieved 81% in predicting action and 92% in predicting action class.


## Reference

**Python Version:** 3.6 Google Colab <br/>
**GPU:** NVIDIA Tesla K80 GPU  <br/>
**Packages:** numpy, pandas, seaborn, matplotlib, tensorflow, keras, Image <br/>
**CNN Article:** [F-beta Score in Keras](https://towardsdatascience.com/f-beta-score-in-keras-part-i-86ad190a252f) <br/>
**Metric Article:** [A Simple CNN: Multi Image Classifier](https://towardsdatascience.com/a-simple-cnn-multi-image-classifier-31c463324fa) <br/>
**Data Generators:** [Keras data generators and how to use them](https://towardsdatascience.com/keras-data-generators-and-how-to-use-them-b69129ed779c) <br/>

# Introduction

**Aim:** develop a deep convolutional neural network (CNN) for a multi-output classifier that can identify the actions of a person from still images.

- A custom data generator is required as there is insufficient memory to load the dataset.
- 

# Exploratory Data Analysis 

![](https://github.com/roywong96/cnn_action_prediction/blob/master/images/diffSizeimages.png)

Several Observations can be made from the intitial exploration of these images.

- Images have good similarity to common natural laguage dataset like imagenet. Transfer learning is an option.
- Images have different shapes. These images requires a common shape for transformation.
- Some exmaple images are ambiguous. The final performance for the model may be affected.
- In some images, the important information and features is toward a corner of the image. Data Augmentation needs to be done carefully.

Now, we can augment the images within the data generator.

![](https://github.com/roywong96/cnn_action_prediction/blob/master/images/augmented_images.png)

# Model Building

- Before any neural network is being developed, 
- Baseline model is developed with Keras functional API that has a VGG-type network which have two convolutional layers with 3x3 filters along with a max pooling layer.
- Since the baseline model failed

![](https://github.com/roywong96/cnn_action_prediction/blob/master/images/model.png)

## Feature Extraction

# Error Analysis

![](https://github.com/roywong96/cnn_action_prediction/blob/master/images/action_error.png)
![](https://github.com/roywong96/cnn_action_prediction/blob/master/images/action_class_error.png)
