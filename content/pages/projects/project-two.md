---
type: ProjectLayout
title: Gamma and Hadron Ray Classification
colors: colors-e
date: '2024-10-15'
client: Machine Learning
description: >-
  A machine learning project focused on classification to distinguish between
  gamma rays and hadron rays using various algorithms.
featuredImage:
  type: ImageBlock
  url: /images/MAGIC.jpg
  altText: MAGIC Telescope
  caption: Image of MAGIC Telescope @ Night
media:
  type: ImageBlock
  url: /images/bg2.jpg
  altText: Project image
---
## **MAGIC Gamma Telescope Dataset Analysis**

### **Project Overview**

This project utilizes the MAGIC Gamma Telescope dataset to classify high-energy particle events, focusing on distinguishing between gamma rays and hadronic interactions. Donated in 2007, the dataset represents particle events captured by the MAGIC (Major Atmospheric Gamma Imaging Cherenkov) telescope, which uses advanced atmospheric Cherenkov imaging to document particle-induced air showers. The project applies various machine learning models and a neural network to identify gamma-ray events based on key imaging features.

### **Dataset Summary**

*   **Source**: MAGIC Gamma Telescope

*   **Instances**: 19,020

*   **Features**: 10 continuous, real-valued features with no missing values

*   **Task**: Binary Classification (Gamma vs. Hadron)

**Key Features**:

| **Variable** | **Description**                                     | **Units** |
| ------------ | --------------------------------------------------- | --------- |
| **fLength**  | Major axis of the ellipse                           | mm        |
| **fWidth**   | Minor axis of the ellipse                           | mm        |
| **fSize**    | Logarithmic sum of pixel content                    | -         |
| **fConc**    | Ratio of the sum of the two highest pixels to fSize | -         |
| **fAlpha**   | Angle of the major axis with vector to origin       | deg       |
| **fDist**    | Distance from origin to ellipse center              | mm        |

### **Objectives**

The main goals of this project are:

1.  **Classification**: Accurately classify gamma-ray versus hadronic events.

2.  **Insight Extraction**: Analyze the distinctive physical attributes of particle showers.

### **Methodology**

The project includes data preprocessing, feature analysis, and classification modeling to enhance performance.

1.  **Data Preprocessing**: Cleaned and normalized data, and applied feature scaling.

2.  **Exploratory Data Analysis (EDA)**: Analyzed feature distributions and correlations to understand data variability.

3.  **Model Development**:

    *   **Classical Models**: Implemented models including K-Nearest Neighbors (KNN), Naive Bayes, Logistic Regression, and Support Vector Classifier (SVC).

    *   **Neural Network Model**: Developed a neural network using **TensorFlow** with hyperparameter tuning for optimal performance. This model architecture included two hidden layers with **ReLU** activations, dropout layers for regularization, and an output layer with a **sigmoid activation** for binary classification.

4.  **Model Tuning and Evaluation**: Evaluated models with accuracy, precision, recall, and F1-score metrics. Conducted extensive hyperparameter tuning for the neural network, testing configurations of hidden layer nodes, dropout probabilities, learning rates, and batch sizes to minimize validation loss.

### **Results**

The Support Vector Classifier (SVC) and the neural network provided the best performance:

*   **Support Vector Classifier (SVC)**

    *   **Accuracy**: 87%

    *   **Weighted F1-Score**: 0.87

*   **Neural Network Model**

    *   **Architecture**: Two dense layers with dropout, trained over 100 epochs.

    *   **Hyperparameters**: Optimized for nodes (16, 32, 64), dropout rates (0, 0.2), learning rates (0.1, 0.005, 0.001), and batch sizes (32, 64, 128).

    *   **Performance**: Achieved an accuracy of 88% with balanced precision and recall.

        *   **Precision**: 0.88 (Class 0), 0.88 (Class 1)

        *   **Recall**: 0.75 (Class 0), 0.94 (Class 1)

        *   **F1-Score**: 0.81 (Class 0), 0.91 (Class 1)

### **Visual Analysis**

Training history was visualized to assess model performance over time. Plots of loss and accuracy for both training and validation data illustrated model convergence and stability. The optimized neural network demonstrated a consistently low validation loss, indicative of effective learning without overfitting.

### **Conclusion**

Through thorough model experimentation and hyperparameter optimization, this project effectively classified gamma and hadron events with high accuracy. With carefully tuned parameters, the neural network model proved highly effective, achieving a balanced accuracy of 88%. This demonstrates the capability of deep learning to enhance classification tasks in high-energy physics contexts, particularly in analyzing particle interactions as captured by Cherenkov telescopes.
