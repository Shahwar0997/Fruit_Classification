# Fruit Classification Project

## Overview

This project focuses on building an image classification system to identify five types of fruits: apples, bananas, grapes, mangoes, and strawberries. The dataset consists of 10,000 RGB images, evenly distributed across all categories. The goal is to evaluate multiple deep learning and hybrid models to determine the most effective approach for accurate fruit recognition.

## Dataset

- Total Images: 10,000
- Classes: Apple, Banana, Grape, Mango, Strawberry
- Split:
  - Training Set: 9,700 images (97%)
  - Validation Set: 200 images (2%)
  - Test Set: 100 images (1%)

Each fruit class is equally represented across all subsets. The dataset is available on Kaggle under the name **"fruits-classification"** and is structured for easy integration with libraries such as Keras and TensorFlow.

## Exploratory Data Analysis

Key steps during data exploration included:

- Class distribution visualization to confirm balance
- Sample image inspection for visual diversity
- Image shape and resolution analysis
- RGB channel histograms per class
- Pixel intensity distributions for brightness and contrast insight

This helped validate the dataset's readiness for modeling.

## Model Performance

Several model architectures were implemented and compared for accuracy:

| Model                                | Accuracy |
|-------------------------------------|----------|
| Simple CNN with Batch Normalization | 71.00%   |
| MobileNetV2 + Data Augmentation     | 88.00%   |
| MobileNetV2 + Hyperparameter Tuning | 86.00%   |
| VGG16 + Random Forest               | 85.50%   |
| **VGG16 + SVM (Best Model)**        | **93.00%**   |

The best-performing model used **VGG16 as a feature extractor combined with an SVM classifier**, showing that hybrid architectures can outperform end-to-end CNNs in specific scenarios.

## Techniques and Tools

- Transfer learning using pretrained models (VGG16, MobileNetV2)
- Feature extraction with classical classifiers (SVM, Random Forest)
- Data augmentation to improve generalization
- Hyperparameter tuning using Keras Tuner
- Dimensionality reduction with PCA for visual analysis

## Future Work

Opportunities to improve the model include:

- Fine-tuning pretrained models beyond the final layers
- Experimenting with advanced data augmentation strategies
- Implementing ensemble learning techniques
- Testing the model on real-world fruit images

## Potential Applications

- Automated fruit classification in agriculture
- Quality control in food production
- Mobile applications for fruit identification
- Educational tools for computer vision

## License

This project uses publicly available data and is intended for educational and research purposes.
