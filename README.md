# Facial Expression Recognition (MEY) Machine Learning By C22-PS155 Capstone Project Bangkit 2022.

## Overview
MEY is an application based on Deep Learning. This application can detect the user's expression by using facial recognition technology. With this technology MEY can detect user expressions and connect to the list of songs that we have offered and users can open the playlist via Youtube.
MEY was created with the aim of elevating the mood of the user and can make the user to adapt the song to the expression that has been detected by our application.

## Credit
The dataset that we use for the prediction of the built model is [DATASET](https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset).

Then the reference we used in building our model from Kaggle [Reference](https://www.kaggle.com/code/jonathanoheix/face-expression-recognition-with-deep-learning).


## Making Prediction Models (Machine Learning)
From the dataset there are 32,887 data and for this model we use 7 facial expressions which will produce output in the form of facial expression categories that are inputted in the form of anger, disgust, fear, happy, neutral, sad, and surprised. In general, we do data preprocessing, which is to divide the data for training and model validation. In this model we use 28,821 data samples for training and 7,066 data samples for validation. After that we build the model with tensorflow. Then the model will generate a predictive output of [REF](https://github.com/MEY-Mental-Education-Yes/MEY-Workflow/blob/main/Face_Expression_Recognition.ipynb).
The Machine Learning Path uses Jupyter Lab to build models and pre-implementation processes.



## Mobile Development
### Overview In MEY APP For Android
- Enter Ml model into android and receive service from Cloud. Build XML and Build back end from Kotlin.
- Build design from Figma Link figma for you see design MEY APP -> [Design MEY APP](https://www.figma.com/file/FL57bUQYkV7VvdvqbUxEL2/MEY?node-id=255%3A193)


### Libary Use
- [Coil](https://coil-kt.github.io/coil/) -> **For fect image from internet**
- [Tensor Flow](https://www.tensorflow.org/lite/inference_with_metadata/lite_support) -> **For model machine learning to android**
- [Retrofit](https://square.github.io/retrofit/) -> **For request API**
- [DataStore](https://developer.android.com/topic/libraries/architecture/datastore?hl=id) -> **For local saved in android**
- [Shimmer](https://facebook.github.io/shimmer-android/) -> **For loading Cardview in android**
- [Karumi Dexter](https://github.com/Karumi/Dexter) -> **For permission in android**
- [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel) -> **For observer live data**
- [Dagger Hilt](https://developer.android.com/training/dependency-injection/hilt-android?hl=id) -> **For inject to constructor in viewmodel**
- [Firebase Auth](https://firebase.google.com/products/auth?gclsrc=aw.ds&gclid=CjwKCAjw14uVBhBEEiwAaufYx_byR8Qg-gpiqSa2sBK6Kh04k0UaCVVXoyVaw9AAQYgXD-0NtY6FLBoCrwwQAvD_BwE) -> **For authentication for user**
- [Firebase database](https://firebase.google.com/products/realtime-database?gclsrc=aw.ds&gclid=CjwKCAjw14uVBhBEEiwAaufYx6T0mwE4qaer1nVB4A20GkmtkOnEz3aQCkRLorW1z9fyI1mSEFCLHxoCeSMQAvD_BwE) -> **For database all data user in android**
- [ViewPager](https://developer.android.com/training/animation/screen-slide) -> **For slider in OnBoarding**

### Architecture Use In Android
|Architecture MVVM | Overview Architecture |
|--|--|
|![alt text](https://raw.githubusercontent.com/MEY-Mental-Education-Yes/The-Logo-MEY/main/mvvm.png)| Model–view–viewmodel (MVVM) is a software architectural pattern that facilitates the separation of the development of the graphical user interface (the view) – be it via a markup language or GUI code – from the development of the business logic or back-end logic (the model) so that the view is not dependent on any specific model platform.



## Cloud Computing

### General Info
This is Backend repository for Song List Category expression for showing list music (Which is use Method GET for showing song) Using RESTFul API
See the documentation for use REST API [Documentation](https://docs.google.com/document/d/1NCTTqN59Q8eLiBxomA3eMT-jUVpUbQtHhZEKWyTFMYQ/edit?usp=sharing)

### Technologies
Project is Created with : 
<ul>
  <li>Node Version v14.17.0</li>
  <li>Npm version 6.14.13</li>
  <li>Google Cloud Sql: Mysql 8.0</li>
  <li>Google App Engine</li>
  <li>Google Cloud Storage</li>
</ul>

### Create Google Cloud SQL (MYSQL)
<ol>
  <li>Create and setup your Cloud SQL</li>
  <li> Open Folder Database </li>
  <li>Import db.sql to cloud sql</li>
</ol>

### Deploy To GCP
Follow the Step to run on GCP

> Clone Repository
``` bash
# Clone Your Repository 
$ git clone https://github.com/MEY-Mental-Education-Yes/MEY-APP-BACKEND.git
#Go to Directory
$ cd MEY-APP-BACKEND
```
> Configure Database
```
- Open koneksi.js
- Change Configuration With Your Database (This App Using MySQL) : 
  host:'CHANGE_WITH_YOUR_DATABASE_IP',
  port: 'CHANGE_WITH_MYSQL_PORT',
  user: 'CHANGE_WITH_YOUR_USERNAME',
  password: 'CHANGE_WITH_YOUR_PASSWORD',
  database: 'CHANGE_WITH_YOUR_DATABASE_NAME'
```
> Configure Node.js
``` bash
# Reinstall The node_modules
$ npm install
# Test your App (Don't Forget Change Your Port App to 8080 because App Engine using Port 8080)
$ npm start
```
> Deploy APP to Google Cloud App Engine
```
- Before Deploy You Can Change The app.yaml Configuration If You Have Spesific Configuration
# Initialize your SDK
$ gcloud init
# Deploy to Google Cloud App Engine
$ gcloud app deploy
```
