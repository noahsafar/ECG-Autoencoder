# ECG Anomaly Detection with Autoencoders

This project explores unsupervised ECG anomaly detection using multiple autoencoder architectures (CAE, CNN-AE, LSTM-AE, VAE, and LSTM-VAE) on the MIT-BIH Arrhythmia Database. The notebook walks through all major stages of the pipeline including preprocessing, model training, evaluation, and reflection.

The notebook follows the author's experiments and thought process; the **best-performing models are clearly marked** both **in the notebook** and **in the accompanying project report PDF**.

---

## 📄 Getting Started

Follow these steps to run the project:

### 1. Open the Notebook

Open the main notebook file: 

ecg_autoencoder-3.ipynb

This notebook contains the full codebase for preprocessing, training, and evaluation.

### 2. Download the MIT-BIH Dataset

Download the MIT-BIH Arrhythmia Database from PhysioNet:

👉 [https://physionet.org/content/mitdb/1.0.0/](https://physionet.org/content/mitdb/1.0.0/)

After downloading, **rename the folder** to: 

mit-bih-arrhythmia-database


Upload the folder to your **Google Drive**, or make sure it's available at a path accessible from Colab.

---

## 🛠️ Setup Instructions

### 3. Mount Google Drive

Run the following cell to mount your Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Follow the on-screen prompt to authenticate.

### 4. Set Dataset Path

Update the dataset path in the notebook to match your Google Drive structure:

```python
dataset_path = "/content/drive/My Drive/Colab Notebooks/Final Project/mit-bih-arrhythmia-database"  # ← CHANGE THIS IF NEEDED

```
Ensure this folder contains .dat, .atr, and .hea files.



### 5. Install Dependencies

Install the required Python packages by running:

```python
!pip install numpy pandas matplotlib scipy py-ecg-detectors wfdb

```
Ensure this folder contains .dat, .atr, and .hea files.

### 6. Verify Dataset Files

Optional but recommended: run this to check your dataset folder:
```python
import os
files = os.listdir(dataset_path)
print("Files in dataset folder:", files)

```
You should see a list of ECG-related files (e.g. 100.hea, 100.dat, 100.atr etc.)

---

## 🚀 Run the Pipeline

Once setup is complete, proceed to run the cells in `ecg_autoencoder-3.ipynb`. The notebook will:

- Preprocess the raw ECG signals  
- Segment them around R-peaks  
- Normalize and filter the data  
- Train multiple autoencoder architectures  
- Evaluate reconstruction-based anomaly detection  

---

## ⚠️ Notes

- The notebook uses Google Colab, and training time may vary depending on your GPU availability.
- Some models (e.g. LSTM-VAE) are trained with fewer epochs due to Colab constraints.
- If you run into memory issues, reduce batch size or latent dimensions.
- All final evaluation metrics (e.g. F2-Score, Precision, Recall) are computed and printed for each model.
- The best model's performance is highlighted in the notebook and project report PDF.

---

## 📊 Dataset Summary

We use the MIT-BIH Arrhythmia Database, a benchmark dataset consisting of 48 half-hour ECG recordings sampled at 360 Hz. It contains over 109,000 annotated heartbeats and provides high-quality labels for both normal and arrhythmic events.
