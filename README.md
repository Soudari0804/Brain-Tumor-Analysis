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
![Screenshot (261)](https://github.com/user-attachments/assets/d9c2cc9d-4a26-42cf-a6c1-7bb233924679)
![Screenshot (262)](https://github.com/user-attachments/assets/986ff6e1-6442-496a-a726-28112bf73751)

New users can register with their credentials.
Existing users can log in securely.

2. Dashboard:
![Screenshot (263)](https://github.com/user-attachments/assets/883453a9-0f3f-415c-9146-21b157d8ec83)
After logging in, users are directed to a dashboard containing three main components:

Symptom Analyzer: Assists in preliminary symptom assessment.
![Screenshot (264)](https://github.com/user-attachments/assets/cfec5f5b-e3bb-43fd-9a45-2c03ae39af3d)


Brain Tumor Analyzer: Enables users to upload MRI/CT images for tumor analysis.
![Screenshot (267)](https://github.com/user-attachments/assets/11f1c9c0-39bd-450e-a7e3-9cdc572500ec)
![Screenshot (266)](https://github.com/user-attachments/assets/259842cb-2b8e-498a-82c2-18d7a33f83c5)
![Screenshot (265)](https://github.com/user-attachments/assets/860d0825-fe9f-4018-bb42-f554c39e05b8)

Chatbot: Provides real-time support for queries related to tumor types, treatment options, and recommendations.
![Screenshot (269)](https://github.com/user-attachments/assets/c5978f40-c129-43a9-afe3-84e011f2d72f)
![Screenshot (268)](https://github.com/user-attachments/assets/c1e32eb5-a028-4598-a3d5-3932927da426)

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
