# Object-Detection-and-Text-Extraction

### Overview:
This project aims to classify images of wine and wine bottles using the ResNet deep learning model. The dataset used in this project is the Wine category subset 
of the Google Open Image Dataset V5. The project is divided in three sections as mentioned below:
<br> 1. Exploratory Data Analysis (EDA)
<br> 2. Model Evaluation
<br> 3. Text Extraction using OCR
#### 1. EDA:
In this part, we will perform the Exploratory Data Analysis and Feature Extraction on the wine dataset to get and learn the statistics of the dataset. 
We will use matplotlib as well as seaborn library for visualization and plotting purposes. The metadata EDA includes:
* Confidence distribution of the images
* Counts and distribution of the images containing wine glasses, wine bottles in the picture
* Statistics on the confidence of the images with the bounding boxes
* Difference between train and test dataset

For Feature extraction data has been:
* Normalized
* Reshaped
* Checked for disparity between train and validation+test dataset 
 
This will help us extract the features like label name, counts of the wine glass or bottle, etc from the image. The above analysis will be a essential in 
determining the models to implement. For now, ResNet model has been used. 

#### 2. Model Evaluation:
ResNet is a top image classification model that has achieved state-of-the-art results in image recognition tasks. In this project, we use the ResNet50 
function in the Keras API to evaluate the wine image classification task. The model will be evaluated using a classification matrix, identifying both accuracy 
but also recall and precision. Wine Images have been filtered from all the classes of the images.
<p> Wine bottles are classified from the images using RESNET50. The images of wine predicted correctly and incorrectly is computed to see the impact of each
feature by using correlation. The images are converted in PIL form, reshaped, preprocessed before feeding it to the model for prediction.</p>

#### 3. Text Extraction:
OCR and Easy OCR libraries are used with the help of Keras, to extract text from the wine class images to get the brand name and wine type. Pipeline is created
to load the saved avro files and feed it to the model for prediction.
Below screenshot is attached to show the type of wine predecited with its probability score:
<br> ![image](https://user-images.githubusercontent.com/68314057/235008151-ec0a95dc-24e0-4488-b2c2-21abf7dae7ff.png) </br>

### About Dataset:
The dataset we will be working on is of Wine category from the Google Open Image Dataset V5. This Wine subset dataset includes the photos of
wine in glasses, in the bottles taken in the random dinner, gathering or events. Some of the photos have bounding boxes around the ‘wine’. 
This dataset contains the training and validation+test data. 
<br> ![image](https://user-images.githubusercontent.com/68314057/235008789-fbf42b11-132f-4291-acaf-6367bb133c4a.png) </br>
<p> Each dataset is read for the analysis. Other metadata files like class description, bounding boxes, etc. is fetced as well and converted in to avro files before
  feeding it to the model for prediction.</p>

### Instruction: 
To run this project, the required libraries must be installed. Please see dependencies and requirements files.

**Note:** This project was created in a group as a part of UMBC Data Science graduate program's Big Data Processing Class. The Hadoop cluster access was provided from
UMBC with the help of professor and the code is referred from professor's lecture material.
