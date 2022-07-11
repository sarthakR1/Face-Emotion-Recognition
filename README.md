# Face-Emotion-Recognition
Deep Learning + Machine Engineering Project 

AlmaBetter Verified Project - AlmaBetter School


# Problem Statement and Project Description

The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms. Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge. In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (exZoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analysed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analysed and tracked. The solution to this problem is by recognizing facial emotions. This is a live face emotion detection system. The model is able to real-time identify the emotions of students in a live class. The demo application is developed using OpenCV-Python, CNN and Streamlit Frameworks.

# FER2013 Dataset
The dataset used in training the CNN model for the above mentioned problem statement is FER2013 and can be downloaded from Kaggle or Data folder of the repository. The data consists of grayscale images of faces at a resolution of 48x48 pixels. The faces have been automatically registered such that they are more or less centred in each image and take up around the same amount of area. The seven categories based on the emotion expressed in the facial expression are (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). There are 28,709 examples in the training set and 3,589 examples in the public test set.

# Project Files Description
This project contains three major executable files, the model output, two documentation files as well as a data directory as follows:

Executable Files:
Face_Emotion_Recognition_Vithika_Karan.ipynb - Google Collab notebook containing data summary, exploration, visualisations and modeling.
real_time_demo.py - Local Real Time Emotion Detection through Open CV - Python.
app.py - Streamlit Web Application for Emotion Detection
Output File:
emotion_detection.h5 - Custom CNN model trained on FER2013 Data
Documentation:
Technical Documentation.pdf.pdf - Includes the complete documentation about the project.
Project Presentation- Deep Learning.pdf.pdf - Presentation of the same.
Source Directory:
Data - Includes FER2013 data, train and validation data as well.
-----------------------------------------------------

# Convolutional Neural Netwroks
A Convolutional Neural Network is a Deep Learning technique that can take an input image and assign weights and biases to various objects in the image, allowing it to distinguish between them. In comparison to other classification algorithms, ConvNet requires substantially less pre-processing. While basic approaches require hand-engineering filters, ConvNets can learn these features with enough training. Conv Neural network

The convolutional layer is the most important component of a CNN because it is where the majority of the computation takes place. It requires input data, a filter, and a feature map, among other things. A feature detector, also known as a kernel or a filter, will traverse across the image's receptive fields, checking for the presence of the feature. Convolution is the term for this procedure.

Pooling Layer reduces the number of parameters in the input by performing dimensionality reduction. The pooling process sweeps a filter across the entire input, similar to the convolutional layer, however this filter does not have any weights. Instead, the kernel uses an aggregation function to populate the output array from the values in the receptive field.

Each node in the output layer, on the other hand, connects directly to a node in the previous layer in the fully-connected layer. This layer performs classification tasks based on the features retrieved by the previous layers and their various filters. While convolutional and pooling layers typically utilize ReLu functions to categorize inputs, FC layers typically use a softmax activation function to provide a probability from 0 to 1.

-----------------------------------------------------

# Exploratory Data Analysis
The number of happy pictures were the highest and disgusted pictures lowest in the dataset. Emotion Classes

# Real Time Emotion Detection Results
The model gave an accuracy of 0.68 on the test data which was kept aside. This indicates the model is generalizing well on unseen data as well. Here are some results of the real time test. Since the observations for disgust class were pretty low, the model is able to correctly recognize rest of the classes pretty well.

# Execution Instructions
The order of execution to run emotion detector locally is as follows:

1. Create a project folder

2. Create a virtual environment, for windows:

python3 -m venv env-name
env-name\Scripts\activate.bat\
3. Download real_time_demo.py, emotion_detection.h5 and haarcascade_frontalface_default.xml in the same folder.

4. Install the dependencies from requirements.txt

Note: Install opencv-python as well, opencv-python-headless in the requirements file is to adjust the size requirements for web app deployment purposes. To run app.py requirements.txt is enough.

5. Run real_time_demo.py

# Conclusion
With this, the notebook comes to an end. Some important conclusions in the project includes:
Model Training results: loss: 0.7801 - accuracy: 0.7084 - val_loss: 0.9670 - val_accuracy: 0.6646
Next step is to create a streamlit web-app for the same and deploy it for real time use. Further work can be explored in the github repository.
