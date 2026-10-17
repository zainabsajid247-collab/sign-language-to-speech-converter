# Sign Language to Speech Converter

A Computer Vision and Deep Learning project for recognizing American Sign Language (ASL) alphabet gestures from images.

## Overview

The **Sign Language to Speech Converter** project explores image-based hand gesture recognition to support communication for people who use sign language.

The current implementation focuses on classifying 24 static ASL alphabet letters using machine learning and deep learning techniques. It compares traditional machine learning models with a Convolutional Neural Network (CNN).

The current notebook demonstrates image dataset inspection, preprocessing, feature extraction, model training, and evaluation.

## Objectives

- Inspect and analyze the ASL alphabet image dataset.
- Preprocess images for machine learning and deep learning.
- Extract Histogram of Oriented Gradients (HOG) features.
- Train and evaluate Support Vector Machine (SVM) and Random Forest classifiers.
- Build and train a CNN for image classification.
- Compare model performance using classification metrics and a confusion matrix.

## Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- OpenCV
- Scikit-learn
- NumPy and Pandas
- Matplotlib and Seaborn
- scikit-image
- Pillow

## Dataset

The project uses the ASL Alphabet dataset from Kaggle.

**Dataset source:** https://www.kaggle.com/datasets/grassknoted/asl-alphabet

The original training dataset contains 29 classes: letters A–Z and the classes Space, Delete, and Nothing. The current HOG and CNN experiments use 24 static letter classes, excluding J and Z.

The notebook includes dataset inspection and a 70% training, 15% validation, and 15% test split.

The dataset is not included in this repository. Please obtain it from the original source and configure the dataset path before running the notebook.

## Project Workflow

1. Dataset loading and folder inspection
2. Image quality and dimension checks
3. Training, validation, and test splitting
4. Image resizing to 64 × 64 pixels and normalization
5. HOG feature extraction
6. SVM and Random Forest training
7. CNN architecture design and training
8. Model evaluation and performance comparison
9. Classification report and confusion matrix

## Models

### 1. Support Vector Machine (SVM)

Uses HOG features to represent hand shape and image gradients before classification.

### 2. Random Forest

Uses the extracted HOG features to classify the selected ASL letters.

### 3. Convolutional Neural Network (CNN)

Learns image features through convolutional and pooling layers, followed by dense layers for classification.

## Evaluation

The notebook evaluates the models using:

- Accuracy
- Precision
- Recall
- Macro F1-score
- Classification report
- Confusion matrix

Final performance values should be taken from the verified notebook outputs. Comparisons should account for differences in the evaluation datasets and procedures.

## How to Run

1. Open the notebook in Google Colab.
2. Download the ASL Alphabet dataset from the source linked above.
3. Upload the dataset ZIP file to your Google Drive or configure an accessible dataset path.
4. Update the dataset paths in the notebook to match your setup.
5. Run the notebook cells in order.
6. Review the training results, classification report, confusion matrix, and model comparison.

Install the required libraries if they are not already available:

```bash
pip install split-folders opencv-python scikit-image scikit-learn matplotlib seaborn pandas pillow
```

TensorFlow is also required for CNN training. Google Colab generally provides TensorFlow, but the installed version may vary.

## Current Scope and Limitations

- The current implementation classifies static images rather than continuous sign language.
- Only 24 static alphabet letters are included in the current model experiments.
- Real-time webcam recognition and speech output are not demonstrated by the current notebook alone.
- A complete speech conversion system would require an additional inference pipeline and text-to-speech integration.

## Future Improvements

- Add real-time hand gesture recognition using a webcam.
- Integrate text-to-speech functionality.
- Improve robustness under different lighting conditions and backgrounds.
- Evaluate the models on independent, real-world hand gesture images.
- Extend the system to support additional signs and dynamic gestures.

## Project Status

The current notebook covers dataset analysis, model development, and offline image classification experiments. Real-time recognition and speech integration remain future development steps.

## Author

**Zainab Sajid**

BS Artificial Intelligence

## Acknowledgements

Thanks to the contributors of the ASL Alphabet dataset for making the dataset available for research and educational use.

