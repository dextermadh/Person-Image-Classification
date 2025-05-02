# 👤 Person Image Classification Model

This repository contains a **Person Image Classification** project built using **Python**, **NumPy**, **Pandas**, **Scikit-learn**, **Matplotlib**, **Seaborn**, **OpenCV**, and **Flask**. The goal of this model is to classify images of individuals into respective classes based on visual features extracted from the dataset.

## 📂 Dataset

The dataset used in this project consists of labeled images of different individuals and is hosted on Google Drive.

🔗 [Download Dataset from Google Drive](https://drive.google.com/drive/folders/1u3JTM71gS9NHE8--q41MbPOue3bDofbw?usp=sharing)

> **Note:** Make sure to download and extract the dataset into a folder named `dataset/` within the model directory of the project.

## 🧹 Dataset Cleaning

The dataset cleaning process involves two key steps:

1. **Automated Cleaning**  
   - Utilizes **Haar Cascade Classifier** (via OpenCV) to detect and crop facial regions from images.
   - Non-face areas are discarded to ensure the dataset contains relevant features.

2. **Manual Cleaning**  
   - A human review is conducted to remove incorrectly detected or poor-quality images that may negatively impact model performance.

## 🛠️ Technologies Used

- Python 3
- Flask (for serving the model)
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- OpenCV (cv2)

## 🧠 Model Overview

- Image data is loaded using OpenCV.
- Preprocessing steps include resizing, converting to grayscale, and flattening images.
- Labels are automatically extracted from folder names (each folder represents a class/individual).
- The dataset is split into training and testing subsets.
- A machine learning algorithm (e.g., SVM or KNN) is trained using Scikit-learn.
- Evaluation metrics like accuracy and classification reports are used to measure model performance.

## 🌐 Flask Server

This project includes a **Flask server** for deploying the trained model. Users can upload an image via a simple web interface or REST API endpoint, and the server will return the predicted class/individual.

## 📁 Project Structure

```bash
person-image-classification/
│
├── model/                  # Trained model and utility scripts
├── server/          # Flask Server
├── UI/                 # UI
└── README.md               # Project documentation
```
## 🚀 Getting Started

1. **Clone the Repository**
```bash
git clone https://github.com/your-username/person-image-classification.git
cd person-image-classification
```
2. **Install Dependacies**
```bash
cd model
pip install -r requirements.txt
```
3. **Run the Flask Server**
```bash
cd server
python server.py
```
