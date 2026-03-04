# CNN Transfer Learning Image Classification

## Project Overview

This project demonstrates **multiclass image classification using Convolutional Neural Networks (CNNs) and transfer learning**. The goal is to build a custom CNN model and compare its performance with a pretrained deep learning model.

The experiment highlights important deep learning concepts such as:

* Convolution operations
* Pooling layers
* Data augmentation
* Transfer learning
* Model evaluation using classification metrics

---

## Dataset

The project uses the **Fashion-MNIST dataset**, a popular benchmark dataset for image classification.

Dataset characteristics:

* Total images: 70,000
* Training images: 60,000
* Test images: 10,000
* Image size: 28 × 28 grayscale
* Number of classes: 10

Classes included in the dataset:

1. T-shirt / Top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle Boot

---

## Data Preprocessing

Several preprocessing steps were performed before training the models:

* Image normalization (pixel values scaled between 0 and 1)
* Reshaping images for CNN input
* Train–validation split
* Data augmentation to improve generalization

Data augmentation techniques used:

* Random rotation
* Zoom transformation
* Width and height shift

---

## Custom CNN Architecture

A custom Convolutional Neural Network was implemented using TensorFlow/Keras.

Model structure:

| Layer        | Description                          |
| ------------ | ------------------------------------ |
| Conv2D       | 32 filters with ReLU activation      |
| MaxPooling2D | Downsampling layer                   |
| Conv2D       | 64 filters with ReLU activation      |
| MaxPooling2D | Downsampling layer                   |
| Flatten      | Converts feature maps to vector      |
| Dense        | Fully connected layer                |
| Dense        | Output layer with Softmax activation |

Loss Function:
Sparse Categorical Crossentropy

Optimizer:
Adam

---

## Transfer Learning Model

To improve classification performance, **MobileNetV2** pretrained on ImageNet was used as a feature extractor.

Steps performed:

1. Loaded pretrained MobileNetV2 model.
2. Removed the top classification layer.
3. Frozen the pretrained layers.
4. Added custom dense layers for classification.

Transfer learning helps leverage knowledge from large datasets and improves model accuracy.

---

## Model Evaluation

The models were evaluated using the test dataset.

Evaluation metrics include:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

Training and validation curves were plotted to analyze the learning behavior of the models.

---

## Results

| Model                           | Accuracy |
| ------------------------------- | -------- |
| Custom CNN                      | ~88–90%  |
| Transfer Learning (MobileNetV2) | ~92–94%  |

The transfer learning model achieved better performance because pretrained networks already capture important visual features.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Project Structure

```
cnn-transfer-learning-image-classification
│
├── CNN_Transfer_Learning_Image_Classification.ipynb
├── CNN_Image_Classification_Report.pdf
└── README.md
```

---

## How to Run the Project

Clone the repository:

```
git clone https://github.com/King87429/cnn-transfer-learning-image-classification.git
```

Navigate to the project directory:

```
cd cnn-transfer-learning-image-classification
```

Install required libraries:

```
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

Run the notebook to train and evaluate the models
## Conclusion

This project demonstrates how CNNs can be used for image classification and how transfer learning significantly improves model performance. The experiment highlights the importance of pretrained models in modern deep learning workflows.
