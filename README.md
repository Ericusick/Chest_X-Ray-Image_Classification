# Chest-X-Ray-Image_Classification

## Itroduction 

In this project we take in a data set with images of chest x-rays with people with and without pneumonia. We performed Image classification using neural networks and convolutional neural networks (CNN). We first built a baseline model with a traditional neural network then improved upon it using a CNN for our final model.  

## Business Case

A hospital reach out to a team of data scientists to create a learning model that would look at chest X-ray to predict whether or not the patient has pneumonia.
Given the dataset from Kaggle, the team are expected to:

- Create an image classification model using Convolutional Neural Network (CNN)

- High accuracy

## Exploratory Data Analysis


This is a normal picture of an x ray image of lungs without pneumonia:

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/normal.jpeg?raw=true" width="400" height="400" />

This is an image of lungs with pneumonia from our data set as you can she it is much more cloudy than the normal:

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/pneumonia.jpg" width="400" height="400" />

### Data Imbalance

Upon further inspection of the datasets we found that there is a severe class imbalance within the train set and test set. Where the images of pneumonia is over saturated in comparison to the normal cases. Which can result in skew result from the image classification models.

__Train Set:__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Test%20Imbalance.PNG" width="400" height="400" />

__Test Set:__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Train%20Imbalance.PNG" width="400" height="400" />

__Validation Set:__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Val%20Imbalance.PNG" width="400" height="400" />

This is interesting to remember when we look at the training accuracy because we have to keep in mind that if the machine just predicts pneumonia the accuracy will actually be fairly high so our validation accuracy is one of the most important metrics because that data is balanced. 

## Modeling Process for CNN

- Convert all X-ray images to grayscale so that the model will run faster and the extra colors are not very import in this data. 

- Resized all of the images to 128 X 128 pixels so we have decent fedelity but it is not to many pixels for our nueral network to process. 

- Created batch size for each datasets.

- Gave more ‘weight’ to the Normal cases to balance the class imbalance.

- Created multiple layers for the neural networks.

### Final CNN Model

<img align="center" width="300" height="600" src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Final%20CNN%20Graphs.PNG">

__Final model results:__

- Training Accuracy: 99.56%

- Training Loss: 0.0191

- Validation Accuracy: 93.75%

- Validation Loss: 0.1840





