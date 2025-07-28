# 🛑 Traffic Sign Classification with CNN (GTSRB)

This project builds a Convolutional Neural Network (CNN) to classify traffic signs using the [GTSRB (German Traffic Sign Recognition Benchmark)] dataset.

It includes data loading, preprocessing, model building, training, evaluation, and visualization of a confusion matrix.

---

## 📂 Dataset

The dataset used is the GTSRB (German Traffic Sign Recognition Benchmark), which contains images of 43 traffic sign classes.

- Source: Available on [Kaggle](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign)
- The dataset is organized in folders:  
  `Train/` contains one folder per class with images inside  
  `Meta.csv` contains metadata and label descriptions (not used in training)

---

## 🧠 Model Architecture

The CNN model is built using TensorFlow/Keras with the following layers:

- Conv2D + MaxPooling2D + BatchNormalization (3 blocks)
- Flatten
- Dense (128 units) + Dropout
- Dense output layer with Softmax (for 43 classes)

> Optimizer: Adam  
> Loss: Categorical Crossentropy  
> Metrics: Accuracy

---

## 🔍 Features

- Load a **subset** of the dataset to train faster
- One-hot encoding of labels using `to_categorical`
- Train/Test split using `train_test_split`
- Visualize training & validation accuracy
- Plot a Confusion Matrix to analyze model performance
