# ECG Anomaly Detection Using Autoencoders & Clustering

## Overview  
This project explores an unsupervised deep learning approach for detecting anomalies in electrocardiogram (ECG) signals. By leveraging **Convolutional Autoencoders (CAE)** and **density-based clustering (DBSCAN)**, the model learns normal heartbeat patterns and identifies deviations without requiring labeled data.

## Key Features  
- **Dataset Utilization**: MIT-BIH Arrhythmia Database & PhysioNet 2017 Challenge Dataset for training, validation, and testing.  
- **Preprocessing Pipeline**: Band-pass filtering, R-peak segmentation, per-patient normalization, and RAAD-based artifact rejection to enhance signal quality.  
- **Model Architecture**: CAE trained on normal ECG signals to reconstruct waveforms, with reconstruction errors analyzed for anomaly detection.  
- **Comparative Benchmarking**: Evaluates CAE against LSTM Autoencoders, Variational Autoencoders (VAE), and 1D CNNs.  
- **Performance Metrics**: Assesses models using **Fβ-score, AUC-ROC, specificity, and inference time** to ensure clinical applicability.  

## Goals  
✔ Reduce reliance on large annotated datasets for ECG anomaly detection.  
✔ Minimize false alarms while maintaining high sensitivity for critical cardiac events.  
✔ Develop an interpretable and reproducible model for potential real-world deployment.  

## Status  
✅ **Data preprocessing (filtering, segmentation, normalization, artifact rejection)**  
🚧 **CAE model trained on normal ECG data**  
🔜 **Threshold tuning and benchmarking in progress**  
🔜 **Final testing & model evaluation**  

## Contributors
Noah Safar (noahsafar) 
