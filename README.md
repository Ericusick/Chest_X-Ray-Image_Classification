# Chest-X-Ray-Image_Classification

## Contributors
- Trevor Mott
- Eric Cusick

## Introduction 

In this project we take in a dataset with images of chest x-rays that are normal and x-rays with pneumonia. We created an Image Classification model using Convolutional Neural Networks (CNN). We first built a baseline model with a traditional neural network and then improved upon it using CNN for our final model.  

## Business Case

A hospital reach out to a team of data scientists to create a learning model that would look at chest X-ray to predict whether or not the patient has pneumonia.
Given the dataset from [Kaggle](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia), the team are expected to:

- Create an image classification model using Convolutional Neural Network (CNN)

- High accuracy

## Exploratory Data Analysis


X-ray of a patient with normal lungs:

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/normal.jpeg?raw=true" width="400" height="400" />

X-ray of a patient with pneumonia:

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/pneumonia.jpg" width="400" height="400" />

### Data Imbalance

Upon further inspection of the datasets we found that there is a severe class imbalance within the train set and test set. Where the cases of pneumonia is oversaturated in comparison to the normal cases. Which can skew the results for our image classification models.

__Train Set__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Test%20Imbalance.PNG" width="400" height="400" />

__Test Set__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Train%20Imbalance.PNG" width="400" height="400" />

__Validation Set__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Val%20Imbalance.PNG" width="400" height="400" />

This is good to keep in mind when we make our models. Without changes to the class imbalance, the model could be high in accuracy however the machine may be more likely to predict every images it sees as positive for pneumonia. We gave the normal cases more weight to help gain equality in class balance for the final modeling process.  

## Modeling Process for CNN

- Convert all X-ray images to grayscale so that the model will run more efficiently

- Resized all of the images to 128 X 128 pixels for consistency  

- Created batch size for each datasets

- Gave more ‘weight’ to the normal cases to balance the class imbalance

- Created multiple layers for the neural networks

### Final CNN Model

<img align="right" src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Final%20CNN%20Graphs.PNG">

__Final model results:__

- Training Accuracy: 99.56%

- Training Loss: 0.0191

- Validation Accuracy: 93.75%

- Validation Loss: 0.1840

Our accuracy is good in this model but with more training data, tweaking the layers, and messing with other parameters, we can lower the validation loss but due to time time constraint we were unable to achieve it. Also our validation set was small which can be a reason why the graphs looks inconsistent, to fix this issue we may want to add more validation data/images to solve this issue. In return, paint a clearer performance of the model.

---

## Recommendations and Future Work 

Looking at the model, we would recommend:

We would recommend the radiologist to use this as a supplementary tool to speed up the diagnostic process and it can be use as a secondary opinion.

### Future Work:

- Get more data for the validation set to gain a better/realistic model accuracy

- Trying/explore different parameters and layers for the neural network modeling

- Create more unique images by augmenting some of given data to give the machine more data to train from
























