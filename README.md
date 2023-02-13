# Object_Classification_From_Scratch
Create an classification model from scratch on Oxford IIT Data Set



## Objective of this notebook
- The purpose of this notebook is to build a image classification on the given data set
- Details of the **problem statement**  , **data set** ,  **summary of the code/solution**  , **sample output/Prediction** from the program and **final result** of the project are listed in the sections to follow.

## Problem Statement 
Build a model to classify pet


## Data Description:
 - Data Set :Oxford IIT Pet Data , a 37 category data set
 - Link : https://www.robots.ox.ac.uk/~vgg/data/pets/


## Summary of the Solution/Code:
The code aims at building a image classification model
- We begin by building a utility class to to read the input images ,convert them to a structured format for further processing and model building and pickle the created input data files Code @ **Read_& Structure_Input.ipynb**
- We then do an EDA on the data and  check various statistics on the images such as total no of images , whether classes are balanced and display a few images with their bounding boxes for visulaization . Code @ **EDA.ipynb**
- We will then we will pre-process the input data to make it compatible for model building wherein we first do a Train-Test split and create 2 subsets (70:30 split), convert all images to tensors for both subsets,resize all the images to one pre-defined size & visualize data and see that everything looks good. Code @ **Pre-Processing_Data.ipynb**
- Finally we build the model, train the model , log the results and run an inference.We  build an image classifier.We will try 3 different variants of the model
The first variant is we  will build a Convolution Neural Network from SCRATCH ,train it & capture results.
The second variant is  a model which a pre-trained MobileNet base with a basic top layer re-built ,re-trained and log results.The third variant is a model with pre-trained MobileNet base with a  slightly more sophisticated  top layer re-built, re-trained and log results.At the end of this program , we will have trained model with scores logged for all the different models tried and tested.We compare and contrast score , pick the best model and run an inference. Code @ **Train_And_Inference.ipynb



## Sample Ouput/Prediction :
Here is a sample Ouput image from  the program/model 

![image](https://user-images.githubusercontent.com/68383273/218541480-b7c10a01-6618-4a28-85a4-fb4ce9b9c463.png)




## Result

- 3 Different models were tried to build the classification model
- A model with pre-trained mobile Net base with a basic top layer reconstructed gave the best results with an accuracy of .9936 in 7 epochs
- A model with pre-trained mobile Net base with a more complex top layer reconstructed gave us a result of .8739 in 7 epochs . Further training could possible give us higher numbers because accuracy was steadily increasing with each epoch
- A 6 layer deep CNN model built from scratch gave us a poor result of 0.097 in 7 epochs and was stagnating at that score. This clearly shows us the importance of using  CNN architectures created by the pioneers of vision with transfer learning enabled.  
- The best model is model no 1( model with pre-trained mobile Net base with a basic top layer reconstructed)

## References & Guidance
- PGP GL/UAT study material 
- https://colab.research.google.com/github/zaidalyafeai/Notebooks/blob/master/Localizer.ipynb


