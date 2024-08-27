# ClearVision

## Overview
Clear Vision AI is a deepfake detection system designed to protect individuals, organizations, and society from the growing threat of manipulated digital content. This project leverages advanced machine learning techniques, combining Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTM) networks, to accurately detect deepfakes in images and videos. The system is integrated into existing IT infrastructures using web-based interfaces and APIs, providing a reliable solution for verifying the authenticity of digital media.

## Project Objectives
1. Web-Based Platform: Develop an intuitive web app for users to submit and verify movies and images, handling various multimedia content.
2. API Integration: Provide an API for integrating the detection tool with other systems, enabling businesses to incorporate Clear Vision AI into their tech ecosystems.
3. Advanced Detection: Use cutting-edge computer vision and machine learning techniques to accurately detect deepfakes and media manipulation.
4. Scalability & Cloud Deployment: Deploy the platform on cloud infrastructure to handle large datasets and user requests efficiently.
5. Future Enhancements: Plan to add full-body manipulation detection and audio deepfake detection to expand the tool's capabilities.

## Business Problem
The proliferation of deepfake technology has made it easier to create highly realistic but deceptive content, posing significant risks to industries reliant on trust and identity verification. Clear Vision AI aims to tackle this issue by creating a powerful tool for identifying manipulated media, thereby safeguarding the security and integrity of user verification processes.

# Data Sources and Preprocessing
## Data Collection
Video recordings: Collected from various datasets, both real and fake, to train the model.
•	Preprocessing Steps:
1.	Frame Extraction: Split videos into individual frames.
2.	Face Detection and Cropping: Isolate and focus on face portions of each frame.
3.	Video Reconstruction: Reassemble cropped frames into a new video.
4.	Frame Filtering: Ignore frames without detected faces.
5.	Uniformity and Thresholding: Retain only the first 150 frames per video to manage computational load.
6.	Sequential Processing: Save frames in sequence for LSTM model usage.

## Model Architecture
The deepfake detection model merges CNNs with LSTMs, optimized using the Adam optimizer and trained with Cross Entropy Loss for classification. Key features include:
1. Train-Test Split: 80% training, 20% testing.
2. Batch Size: 4 videos per batch.
3. Training: 20 epochs with a learning rate of 0.001.
4. Evaluation: Confusion matrix to assess accuracy and error types.

## System Integration
Clear Vision AI is designed to fit seamlessly into existing IT infrastructures:
1. Frontend Interface: Users can upload images or videos for deepfake detection.
2. Backend Processing: The trained model evaluates media content and returns results via API.
3. Optimization: Includes chunked uploading, batch processing, and automated deletion for enhanced performance.

