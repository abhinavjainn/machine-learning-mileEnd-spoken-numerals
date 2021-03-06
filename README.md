# Mile End Spoken Numerals - Machine Learning classification model - Building and Deployment

This project has three major parts:
1. Dataset creation
2. Building a classifier to identify the intonation of short audio clips using the Mile End Spoken Numerals dataset.
3. Deploying the model as a backend Rest API over internet using a cloud platform.

# Dataset creation
Dataset was developed by the School of Electonics Engineering & Computer Science of the Queen Mary University of London. Roughly 185 postgraduate students contributed wth audio clips. Audio clips were further separated, cleaned and published by the team led by Dr. Jesus Requena-Carrion. Audio clips contain different numbers spoken by students in different intonations viz. Excited, Bored, Question and Neutral.

Dataset URL: https://collect.qmul.ac.uk/down?t=4LO0R0TSLPGGHJPC/45O137K56GGVDFUT9AH4ST0

# Model building
All the steps in model building such as dataset preprocessing, feature extraction, model training, validation and evaluation have been explained in detail in the notebook: Classification_Model_Bulding_MLEnd_Spoken_Numerals.ipynb

To summarize this part, several spectral (spectral centroid, bandwidth etc.) and rhythmic features were extracted from the audio clips. Various candidate models such as Logistic Regression, K-Nearest Neighbours (KNN), Support Vector Machines (SVM) and Neural Network were trained and finally a model was selected after evaluating the validation accuracies of candidate models.
This repository also contains the supporting csv and txt files used during model building.

# Deployment
The final chosen model was deployed as a Rest API on Heroku cloud platform. This repository contains the required python and Heroku configuration files. All the predictions made by this model are logged in the database which can be used to further improve model's performance.

Application URL: https://mile-end-spoken-numerals.herokuapp.com/

Endpoint: /predict-intonation
