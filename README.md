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

Upon further inspection of the datasets we found that there is a severe class imbalance within the train set and test set. Where the images of pneumonia is over saturated in comparison to the normal cases. Which can skew the results for our image classification models.

__Train Set: Skewed in the direction of pneumonia __

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Test%20Imbalance.PNG" width="400" height="400" />

__Test Set: Skewed in the direction of pneumonia__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Train%20Imbalance.PNG" width="400" height="400" />

__Validation Set: Balanced__

<img src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Val%20Imbalance.PNG" width="400" height="400" />

This was good to keep in mind when we made our models. If we look at the training acuracy of our models and it is high it could be achived but just predicting pneumonia everytime. We put more weight on the normal images to help to give more importance and to balance out the data in our models.  

## Modeling Process for CNN

- Convert all X-ray images to grayscale so that the model will run faster and the extra colors are not very import in this data. 

- Resized all of the images to 128 X 128 pixels so we have decent fedelity but it is not to many pixels for our nueral network to process. 

- Created batch size for each datasets.

- Gave more ‘weight’ to the Normal cases to balance the class imbalance.

- Created multiple layers for the neural networks.

### Final CNN Model

<img align="right" src="https://github.com/Ericusick/Chest-X-Ray-Image_Classification/blob/main/Pictures%20for%20non-technical/Final%20CNN%20Graphs.PNG">

__Final model results:__

- Training Accuracy: 99.56%

- Training Loss: 0.0191

- Validation Accuracy: 93.75%

- Validation Loss: 0.1840

Our accuracy is good in this model but with more training data and tweaking the layers and parameters or adding more data with a data augmenter we would like to get our validation loss lower but due to time restraints we could not do that. Aslo our validation set was small that is why it looks so inconsistent on the graph so adding more validation data would help get a clearer picture of how this model is performing.  

---

## Recommendations and Future Work 

Looking at the model, we would recommend:

We would recommend radiologist to use this as a supplementary tool to speed up the diagnostic process and as a secondary opinion.

### Future Work:

- Get more data for the validation set to gain a better/realistic model accuracy.

- Trying/explore different parameters and layers for the neural network modeling.

- Create more unique images by augmenting some of given data to give the machine more data to train from
























