# 🧠 Customer Churn Prediction with Artificial Neural Networks

This project uses an Artificial Neural Network (ANN) built with TensorFlow and Keras to predict customer churn using the **Churn_Modelling.csv** dataset. The dataset includes customer information like credit score, geography, gender, tenure, and whether or not the customer exited the bank.

---

## 📂 Dataset

The dataset contains 14 columns:
- CustomerID, Surname, CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, Exited

Only features from column 3 to 12 were used for training:
- `X` = columns 3 to 12
- `y` = column 13 (Exited)

---

## 🧪 Preprocessing Steps

1. **Selected Features**  
   Selected relevant features from the dataset (`CreditScore` to `EstimatedSalary`).

2. **Created Dummy Variables**  
   Applied one-hot encoding to categorical variables (`Geography`, `Gender`).

3. **Feature Scaling**  
   Scaled numeric features using `StandardScaler`.

4. **Train-Test Split**  
   Split the data into 80% training and 20% testing sets.

---

## 🏗️ ANN Architecture

- Built using TensorFlow 2.8.0 and Keras
- Architecture:  
  - Input layer: 11 features  
  - Hidden layers: Dense layers with activation functions like `ReLU`, `LeakyReLU`, `ELU`  
  - Output layer: 1 neuron with `sigmoid` activation for binary classification

---

## 🚀 Model Training

- Optimizer: Adam
- Loss: Binary Crossentropy
- Epochs: 50
- Batch Size: 32
- Performance Metrics:
  - Accuracy steadily improved across epochs
  - Final training accuracy: ~85%
  - Validation accuracy: ~84–85%

---

## 📊 Results

- The ANN model effectively predicts customer churn
- Training and validation loss/accuracy show good performance and generalization
- No signs of significant overfitting

---

## 🧰 Requirements

- Python 3.x
- TensorFlow 2.8.0
- pandas, numpy, matplotlib, scikit-learn

Install dependencies using:

```bash
pip install tensorflow==2.8.0 pandas numpy matplotlib scikit-learn
