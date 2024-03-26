# Melanoma Detection using Convolutional Neural Network

This repository contains the implementation of a Convolutional Neural Network (CNN) for the diagnosis of Melanoma Cancer. The model leverages the ResNet-18 architecture with ImageNet weights for initialization. This model weights are fine-tuned on the cancer dataset achieving an accuracy of over 83%.

### Model Architecture

The model used here is ResNet-18, the powerful image classification network. The network was initialized with weights from ImageNet to leverage pre-learned features. While the type of data in the ImageNet data and this dataset are vastly different, the pre-trained weights can still be useful for extracting low-level features such as edges and shapes which are similar.

### Training Process

Adam is used to adjust the learning rate. However, to ensure information learned from ImageNet training is not lost, there are different initializations for the learning rate based on each layer's placement within the larger model. Low-level features from the earliest convolutional layers need the least adjustment so their initial learning rate is small, while the last convolutional layers extract fine details and need more learning so the initial learning rate is set to a larger value.

## Dataset

The dataset used for this project consists of dermatoscopic images with labels indicating the presence or absence of melanoma. It was obtained from the following Kaggle competition: [Melanoma Detection Challenge](https://www.kaggle.com/datasets/fanconic/skin-cancer-malignant-vs-benign?select=test).

## Results

The model achieved an accuracy of over 83% on the test set, demonstrating its effectiveness in classifying dermatoscopic images for melanoma presence.
