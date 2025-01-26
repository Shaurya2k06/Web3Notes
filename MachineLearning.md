# Machine Learning Overview

Machine learning is a field of artificial intelligence (AI) that has its roots in statistics and mathematical data modeling. The fundamental idea is to enable systems to learn from data and make predictions or decisions without being explicitly programmed. By analyzing past data observations, machine learning models can identify patterns and relationships, allowing them to predict unknown outcomes or values.

Below is a comprehensive overview of machine learning concepts, types, evaluation metrics, and algorithms.

---

## Fundamental Concepts of Machine Learning

1. **Training Data**  
   - Training data consists of past observations. These observations include:  
     - **Features**: Attributes or characteristics of the observation (e.g., temperature, age, height).  
     - **Labels**: Known values you want the model to predict (e.g., sale price, species).  

2. **Mathematical Representation**  
   - Features are often denoted as **x**, representing a vector of multiple values:  
     \[
     x = [x_1, x_2, x_3, \dots]
     \]  
   - Labels are denoted as **y**, representing the target value.  
   - During training, an algorithm finds a relationship between **x** (features) and **y** (label), expressed as a function:  
     \[
     y = f(x)
     \]  
   - After training, the model can use the function **f** to predict new labels **ŷ** ("y-hat") for unseen data.

3. **Inferencing**  
   - Inferencing refers to using a trained model to predict the label for a new set of feature values. The output, **ŷ**, is a prediction rather than an observed value.

4. **Supervised and Unsupervised Learning**  
   - Supervised learning involves training with both features and known labels.  
   - Unsupervised learning uses data with only features, identifying patterns or clusters.

---

## Types of Machine Learning

### 1. **Supervised Learning**  
In supervised learning, the training data contains both input features (**x**) and corresponding labels (**y**). The goal is to learn a mapping function that predicts labels for new data.

#### **Regression**
- Used when the label is a numeric value.  
- Example:  
  - Predicting the number of ice creams sold on a given day based on temperature, rainfall, and windspeed.  

#### **Classification**
- Used when the label represents a category or class.  
- Two main types of classification:  
  - **Binary Classification**: Predicts one of two mutually exclusive outcomes.  
    Example:  
    - Determining whether a patient is at risk for diabetes (Yes/No).  
  - **Multiclass Classification**: Predicts one of multiple possible classes.  
    Example:  
    - Identifying the species of a penguin (Adelie, Gentoo, or Chinstrap).  

---

### 2. **Unsupervised Learning**  
In unsupervised learning, the training data contains only features (**x**) without labels. Models are used to find patterns or structures in the data.

#### **Clustering**
- Groups data points into clusters based on feature similarities.  
- Example:  
  - Grouping flowers by their size, number of petals, and number of leaves.

- **K-Means Clustering** Steps:  
  1. Convert features into n-dimensional coordinates (e.g., `[x1, x2]` for 2D data).  
  2. Choose the number of clusters (**k**) and initialize centroids at random positions.  
  3. Assign each data point to the nearest centroid.  
  4. Move centroids to the mean position of assigned points.  
  5. Repeat until centroids stabilize or a maximum number of iterations is reached.

---

## Evaluation Metrics

### Regression Metrics
1. **Mean Absolute Error (MAE)**  
   - Measures the average difference between predicted and actual values.  

2. **Mean Squared Error (MSE)**  
   - Calculates the average squared difference between predicted and actual values.  

3. **Root Mean Squared Error (RMSE)**  
   - Square root of MSE, providing error in the same units as the label.  

4. **Coefficient of Determination (R²)**  
   - Indicates how well the model explains variance in the data.

---

### Classification Metrics
Classification models are evaluated using a **confusion matrix**, which summarizes predictions into:  
- True Positives (TP)  
- False Positives (FP)  
- True Negatives (TN)  
- False Negatives (FN)  

Key metrics derived from the confusion matrix:  

1. **Accuracy**  
   - Proportion of correct predictions:  
     \[
     \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
     \]

2. **Recall**  
   - Measures the proportion of actual positives correctly predicted:  
     \[
     \text{Recall} = \frac{TP}{TP + FN}
     \]

3. **Precision**  
   - Measures the proportion of predicted positives that are true positives:  
     \[
     \text{Precision} = \frac{TP}{TP + FP}
     \]

4. **F1-Score**  
   - Harmonic mean of precision and recall:  
     \[
     F1 = \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
     \]

---

### Clustering Metrics
Clustering models are evaluated based on how well-separated the clusters are. Common metrics include:

1. **Average Distance to Cluster Center**  
   - Measures how close data points are to the centroid of their cluster.  

2. **Silhouette Score**  
   - A value between -1 and 1 summarizing cluster separation (closer to 1 indicates better separation).  

---

## Specialized Algorithms

### Binary Classification
- Trains a model to predict one of two possible outcomes (e.g., true/false).  
- Evaluated using metrics like accuracy, precision, recall, and F1-score.

### Multiclass Classification
1. **One-vs-Rest (OvR)**:  
   - Trains a binary classifier for each class, calculating the probability of each class against all others.  

2. **Multinomial Algorithms**:  
   - Creates a single function that outputs a probability distribution across all classes, summing to 1.  

### Clustering
- **K-Means Clustering**: Groups data into **k** clusters through centroid assignment and iterative refinement.

---

## Deep Learning
Deep learning is an advanced branch of machine learning inspired by the structure of the human brain. It uses **artificial neural networks** to model complex patterns and relationships in data.

- Neural networks simulate biological neurons using mathematical functions.  
- They consist of layers of interconnected nodes that process and transform input data to learn patterns.

Deep learning is particularly powerful for tasks like image recognition, natural language processing, and speech synthesis.

---
