# Melanoma Detection - Convolutional Neural Network
Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. 

Building A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

Built Multiclass classification model using a custom convolutional neural network in TensorFlow & Keras.

## Table of Contents
* [General Info](#general-information)
* [Process followed](#process-followed)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)


## General Information
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion


## Process followed
In this project, CNN model is bulit with several combinations. Accuracy improvements are summarized with finalized single network structure below.

Built Neural netwrok architecture using keras.

Network structure
- Rescaling layer to normalize the pixel values to be in the `[0, 1]` range,
- Two convolutional layers having 32 filters with Relu activation followed by max pooling layer,
- Two convolutional layers having 64 filters with Relu activation followed by max pooling layer,
- Two convolutional layers having 128 filters with Relu activation followed by max pooling layer,
- and then `Flatten` the output of the pooling layer to give us a long vector, 
- then add a fully connected `Dense` layer with 512 neurons with `Relu` activation, and finally
- add a `softmax` layer with 9 (num_classes) neurons


Used `adam` optimizer and `sparse_categorical_crossentropy` as loss function with `accuracy` as metric

- First model: Baseline model with above structure

- Second model: Data augumentation using keras utilities, batch normalization after every convolution layer, dropout after final convolution layer & fully connected layer, regularization in fully connected layer.

- Third model: Data augumentation with Augumentor library to handle class imbalance. But, architecture is same as second model. This helped to overcome underfitting and overfitting issues upto certain extent.

#### Detailed process, plots, Observations and conclusions are provided in python notebook.


## Technologies Used
- tensorlfow - 2.10.1
- pandas - 2.1.1
- numpy - 1.24.3
- matplotlib - 3.8.0
- seaborn - 0.13.2

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was part of Upgrad-IIITB ML& AI course.
- Learnings from this course helped to complete this study.


## Contact
Created by [Sai Mohan Reddy Neelam](https://github.com/saimohan35) - feel free to contact me!
