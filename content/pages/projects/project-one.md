---
type: ProjectLayout
title: Hotel Management Analytics
colors: colors-a
date: '2024-11-10'
client: Data Science & Analytics
description: >-
  Analyzing hotel booking data to extract valuable insights and build a
  predictive model for booking status classification (EDA).
featuredImage:
  type: ImageBlock
  url: /images/Unsplash-EDA.jpg
  altText: Hotel Management EDA
media:
  type: ImageBlock
  url: /images/Unsplash-EDA.jpg
  altText: Hotel Management EDA
---
### **Hotel Booking Data Analysis and Machine Learning Model Comparison**

This analysis explores a hotel booking dataset, implementing various machine learning models to predict booking status. The goal is to understand the data, preprocess it, and evaluate multiple models for accuracy and performance. Here’s an updated summary of the exploration and model comparison.



### **1. Basic Understanding of the Data**

#### **Data Types**

*   **Continuous Variables**:

    *   Lead Time

    *   Average Price Per Room

*   **Categorical Variables**:

    *   Meal Plans

    *   Room Type Reserved

    *   Market Segment Type

    *   Repeated Guest

    *   Required Car Parking Space

*   **Non-Categorical Variables**:

    *   Adults

    *   Children

    *   Stays Weekends

    *   Stays Weeks

    *   Arrival Year

    *   Arrival Month

    *   Arrival Date

    *   Number of Previous Bookings Cancelled

    *   Number of Previous Bookings Not Cancelled

    *   Number of Special Requests



### **2. Data Preprocessing**

The dataset was loaded and processed using the following steps:

*   Column names were standardized for clarity.

*   Categorical variables were identified and encoded where necessary.

*   Continuous variables were scaled using a **StandardScaler** for better performance in some machine learning models.

*   The data was split into training and testing sets.



### **3. Machine Learning Model Evaluation**

#### **Logistic Regression**

*   **Accuracy**: 78.2%

*   **Classification Report**:

    *   Precision: 0.78 (for both classes)

    *   Recall: 0.78 (for both classes)

    *   F1-Score: 0.78 (for both classes)

*   **Key Observations**:

    *   Logistic Regression provides a baseline accuracy of 78%, which is decent for a linear model. It performs similarly on both classes.



#### **Support Vector Machine (SVM)**

*   **Accuracy**: 84.0% (with all data), 84.0% (with 30% data)

*   **Training Time**: 4.32 seconds

*   **Prediction Time**: 4.53 seconds

*   **Classification Report**:

    *   Precision: 0.84 (for both classes)

    *   Recall: 0.84 (for both classes)

    *   F1-Score: 0.84 (for both classes)

*   **Key Observations**:

    *   The SVM model shows significant improvement over Logistic Regression, achieving 84% accuracy. It works well even when trained on a subset of the data (30%), reducing training time without losing performance.



#### **Decision Tree Classifier**

*   **Accuracy**: 89.0%

*   **Training Time**: 0.0041 seconds

*   **Prediction Time**: 0.004 seconds

*   **Classification Report**:

    *   Precision: 0.87 (for class 0), 0.91 (for class 1)

    *   Recall: 0.91 (for class 0), 0.87 (for class 1)

    *   F1-Score: 0.89 (for both classes)

*   **Key Observations**:

    *   Decision Trees perform very well with 89% accuracy and are extremely fast during both training and prediction phases. The model exhibits a balanced performance across both classes.



#### **K-Nearest Neighbors (KNN)**

*   **Accuracy**: 89.8%

*   **Prediction Time**: 12.99 seconds

*   **Classification Report**:

    *   Precision: 0.86 (for class 0), 0.95 (for class 1)

    *   Recall: 0.95 (for class 0), 0.85 (for class 1)

    *   F1-Score: 0.90 (for both classes)

*   **Key Observations**:

    *   KNN achieves a higher accuracy (89.8%) than Decision Trees. However, it has slower prediction times, especially when using larger data. Despite this, it provides high precision for class 1 and strong overall performance.



#### **AdaBoost (with Decision Tree as base estimator)**

*   **Accuracy**: 92.5%

*   **Training Time**: 9.0 seconds

*   **Prediction Time**: 0.3 seconds

*   **Classification Report**:

    *   Precision: 0.91 (for class 0), 0.94 (for class 1)

    *   Recall: 0.94 (for class 0), 0.91 (for class 1)

    *   F1-Score: 0.93 (for both classes)

*   **Key Observations**:

    *   AdaBoost achieved the best performance, with an accuracy of 92.5%. It provides a good balance between precision and recall for both classes. Training time is longer than Decision Trees and SVM, but the prediction time is fast.



### **4. Summary of Best Performers**

*   **Best Model**: **AdaBoost Classifier** with Decision Tree as the base estimator (92.5% accuracy).

*   **Other Strong Models**: **Decision Tree Classifier** (89%), **K-Nearest Neighbors** (89.8%).

*   **SVM** and **Logistic Regression** are solid models, but AdaBoost outperforms them in terms of accuracy.



