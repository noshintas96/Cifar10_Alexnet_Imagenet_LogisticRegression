# Cifar 10 Dataset Analysis with AlexNet and Logistic Regression

This repository contains code for analyzing the CIFAR-10 dataset using pre-trained AlexNet and logistic regression classifiers.

## Dataset Preparation

1. Download the CIFAR-10 dataset.
2. Unpickle the files and prepare the data for further processing.
3. Separate the data into train, validation, and test sets.
4. Perform data augmentation.

## Pre-trained Model

1. Download the AlexNet model pretrained with ImageNet dataset.
2. Remove the last two fully connected layers from the classifier.

## Prediction and Confusion Matrix

1. Use the AlexNet model to make predictions on the test batch.
2. Extract top 10 predicted names from the prediction list.
3. Create a confusion matrix using the top predictions and true labels.

## Feature Extraction and Logistic Regression

1. Remove the last fully connected layer from the AlexNet classifier.
2. Extract features using the fc6 layer.
3. Train a logistic regression classifier on the extracted features.
4. Evaluate the model on the train, validation, and test sets.

## Results

- The fc6 layer output gives better results than fc7.
- Validation accuracy is much less than training accuracy, indicating potential overfitting.
- Extracting feature vectors from earlier fully connected layers can result in higher accuracies.
- Going from fc6 to fc7 layer caused a loss of valuable feature information.

## Conclusion

This project demonstrates the effectiveness of using pre-trained deep learning models like AlexNet for feature extraction and subsequent classification tasks. By selecting appropriate layers for feature extraction, higher accuracies can be achieved. Additionally, careful consideration should be given to potential overfitting when training classifiers on extracted features.
