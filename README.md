Brain Tumor Analysis
Enhancing Brain Tumor Visualization through Deep Learning-Based Fusion of MRI and CT Images with VGG Network and Chatbot Integration

Project Overview
This project leverages deep learning to enhance brain tumor visualization by fusing MRI and CT images using the VGG Network. It integrates advanced detection techniques with YOLOv7, enriched by attention modules and feature pyramids. An NLP-powered chatbot provides real-time support for healthcare professionals, answering queries about tumor types, stages, and treatments while offering personalized recommendations.

Objectives
Improve diagnosis, treatment planning, and patient management in neuro-oncology.
Enhance the accuracy of tumor detection through deep learning techniques.
Provide an interactive and real-time support system via an NLP-powered chatbot.
Develop an intuitive web-based interface for users to interact with the system seamlessly.
Dataset Structure

Ensure your dataset is organized in the following structure:
dataset/
    train/
        tumor/
            image1.jpg
            image2.jpg
            ...
        normal/
            image1.jpg
            image2.jpg
            ...
    val/
        tumor/
            image1.jpg
            image2.jpg
            ...
        normal/
            image1.jpg
            image2.jpg
            ...

Project Implementation

Step 1: Data Preparation
Preprocess MRI and CT images.
Normalize image sizes and formats.
Augment data for improved model robustness.

Step 2: Training the Model
Utilize the VGG Network for feature extraction.
Implement YOLOv7 for enhanced detection accuracy.
Integrate attention modules and feature pyramids for better visualization.
Train using PyTorch with optimal hyperparameters.

Step 3: Saving and Loading the Model
Save the trained model for future inference.
Implement functionality for loading pre-trained weights.
Optimize model performance using validation accuracy metrics.

Streamlit Web Application
pip install streamlit

Installation
To install Streamlit, run:
pip install streamlit


Web App Structure

The Streamlit application consists of the following pages:
1. Registration & Login Page:
   The Registration & Login Page is the entry point of the Streamlit web application, ensuring secure access to the system.
Features:
User Registration:
New users can create an account by providing essential details such as name, email, and password.
User credentials are securely stored in a database for authentication.

User Login:
Existing users can log in using their registered email and password.
Secure authentication ensures only authorized access.

Password Recovery:
Users can reset their passwords in case of a forgotten password.
Main Page - Registration
New users can create an account by providing their name, email, and password.
User credentials are securely stored for authentication.
Upon successful registration, users can log in and access the dashboard.
<img src="https://github.com/user-attachments/assets/d9c2cc9d-4a26-42cf-a6c1-7bb233924679" width="500"/>


Sign-In Page
Existing users can log in using their email and password.
If users forget their password, they can reset it using the "Forgot Password" option.
After logging in, users are redirected to the dashboard to access all features.
<img src="https://github.com/user-attachments/assets/986ff6e1-6442-496a-a726-28112bf73751" width="500"/>
New users can register with their credentials.
Existing users can log in securely.

2. Dashboard:
 The Dashboard is the central hub of the Streamlit web application, providing users with access to various functionalities
 for brain tumor analysis and real-time assistance.
Features:
User-Friendly Interface: Displays key components in an organized layout for seamless navigation.
Real-Time Data Processing: Allows users to analyze symptoms, upload medical images, and receive AI-based insights.
Interactive Chatbot: Provides quick responses to queries related to tumor detection, treatment options, and personalized recommendations.
How It Works:
Upon logging in, users land on the Dashboard.
They can navigate between the three components.
Clicking on a component will open its dedicated interface for analysis or support.
The system processes the user’s input (symptoms, images, or queries) and provides appropriate responses.
<img src="https://github.com/user-attachments/assets/883453a9-0f3f-415c-9146-21b157d8ec83" width="500"/>
After logging in, users are directed to a dashboard containing three main components:
Once users successfully log in, they are redirected to the Dashboard, which serves as the central interface
for interacting with the system. The dashboard is designed for seamless navigation and contains three primary components:

Symptom Analyzer
Helps users assess potential brain tumor symptoms.
Uses a predefined symptom-checking algorithm.
Provides insights based on user inputs.
Symptom Analyzer: Assists in preliminary symptom assessment.
<img src="https://github.com/user-attachments/assets/cfec5f5b-e3bb-43fd-9a45-2c03ae39af3d" width="500"/>

Brain Tumor Analyzer
Allows users to upload MRI/CT images for tumor detection.
Uses deep learning models (VGG Network, YOLOv7) to analyze images.
Displays detection results, highlighting any abnormalities.
Brain Tumor Analyzer: Enables users to upload MRI/CT images for tumor analysis.

Step 1: Upload MRI Scan
Users can begin the tumor analysis by uploading their MRI or CT scan images through the Brain Tumor Analyzer.
The system accepts medical image formats such as JPG, PNG, or DICOM for processing. Once uploaded, the image
is preprocessed and prepared for deep learning-based analysis.
<img src="https://github.com/user-attachments/assets/11f1c9c0-39bd-450e-a7e3-9cdc572500ec" width="500"/>

Step 2: Click on "Analyze" to Get Results
After uploading the MRI, users need to click the "Analyze" button. The system then processes the image using
the VGG Network and YOLOv7 models, enhanced with attention mechanisms and feature pyramids. The deep learning
model detects abnormalities and segments the tumor region if present.
<img src="https://github.com/user-attachments/assets/259842cb-2b8e-498a-82c2-18d7a33f83c5" width="500"/>

Step 3: View Detection Results
The analyzed image is displayed with detection highlights, showing whether a tumor is present or not. If 
detected, the system provides information about tumor type, size, and possible stages. Users can then proceed 
with further analysis or consult the chatbot for treatment options and recommendations.
<img src="https://github.com/user-attachments/assets/860d0825-fe9f-4018-bb42-f554c39e05b8" width="500"/>

Provides real-time support using NLP.
Answers queries about tumor types, stages, and treatment options.
Offers personalized recommendations based on user input.
Chatbot: Provides real-time support for queries related to tumor types, treatment options, and recommendations.

Find Nearby Hospitals
Users can enter their location name or allow location access.
The chatbot fetches a list of nearby hospitals specializing in brain tumor treatment.
<img src="https://github.com/user-attachments/assets/c5978f40-c129-43a9-afe3-84e011f2d72f" width="500"/>

Hospital Address & Details
Once a hospital is selected, the chatbot provides its full address, contact details, and website (if available).
Users can also get directions or additional details for consultation and treatment options.
<img src="https://github.com/user-attachments/assets/c1e32eb5-a028-4598-a3d5-3932927da426" width="500"/>

Component Interaction
Clicking on a component (e.g., Brain Tumor Analyzer) opens the corresponding module.
Users can upload MRI/CT images, and the system will predict and highlight tumor presence.
The chatbot will assist users by answering questions and providing relevant information.

Embedding HTML for Symptom Analyzer
If you have a pre-built HTML file for the Symptom Analyzer, you can embed it using:
st.components.v1.html(""" <iframe src='symptom_analyzer.html' width='100%' height='600'></iframe> """)

Project Details in JSON
To store project details, including the model, dataset path, training parameters, and best validation accuracy, use a JSON file:
{
  "model": "VGG + YOLOv7",
  "dataset_path": "dataset/",
  "training_parameters": {
    "learning_rate": 0.001,
    "epochs": 50,
    "batch_size": 32
  },
  "best_validation_accuracy": 92.5
}
