# Malaria-Detection

Malaria Cell Image Classification
An AI-powered classifier to detect parasites in blood smear images.
Project Overview
This project uses Deep Learning to automate the detection of Malaria in cell images. By leveraging Transfer Learning, the model can distinguish between healthy and parasitized cells with high accuracy, assisting in faster medical diagnosis.
Dataset
The model was trained using the NIH Malaria Cell Images Dataset hosted on Kaggle. It contains 27,558 images of individual cells.
Dataset Link: Kaggle - Malaria Cell Images Dataset
Performance Results
The model was evaluated on 5,512 unseen images (data it never saw during training) to ensure reliability:
Test Accuracy: 95.66%
AUC Score: 0.98 (Shows excellent class separation)
Validation Accuracy: 97.1%
Technical Approach
Architecture: Used MobileNetV2 (Transfer Learning) with a custom Global Max Pooling head.
Input Pipeline: Built a high-speed tf.data pipeline to handle 27,000+ images efficiently.
Preprocessing: All images were resized to 120x120 and normalized to a 0-1 range.
Loss Function: A single-unit Sigmoid layer with Binary Crossentropy loss.
Confusion Matrix Analysis
Out of the 5,512 test images:
True Negatives (Healthy): 2,730
True Positives (Infected): 2,543
False Negatives (Missed Cases): 149
Tech Stack
Framework: TensorFlow & Keras
Language: Python
Libraries: NumPy, Scikit-Learn, Matplotlib
Hardware: Kaggle Tesla T4 GPU
