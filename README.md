# Image Classification (Dicoding Submission - Belajar Machine Learning untuk Pemula (Machine Learning for Beginners))

## Author

Ryan Gading Abdullah

## Date Created

December 2023

## Description

This project is a computer vision-based image classification model built as a final submission for the **"Belajar Machine Learning untuk Pemula"** course offered by Dicoding Indonesia.

The model classifies images into three categories: **rock**, **paper**, and **scissors**, based on the classic hand game. The dataset used was provided by Dicoding and consists of labeled images of hands showing rock, paper, or scissors gestures. The workflow includes downloading and extracting image data, preprocessing it with data augmentation, training a Convolutional Neural Network (CNN), and then using the trained model for predictions.

## Technologies Used

- **Python 3.10+**
- **TensorFlow 2.15**
- **Keras**
- **Scikit-learn** (for train-validation split)
- **Matplotlib** (for image handling and visualization)
- **Google Colab** (as the development environment)
- **ImageDataGenerator** (for data augmentation)

## Model Architecture

The CNN model has the following structure:

- 4 Convolutional Layers with ReLU activation and MaxPooling
- Flatten Layer
- Dropout Layer (rate: 0.8) to prevent overfitting
- Dense Layer (512 neurons, ReLU)
- Output Layer (3 neurons, Softmax activation for multi-class classification)

Early stopping is used with a custom callback that halts training once the model reaches 98% accuracy.

## How to Use

1. **Environment**: This project is best run in [Google Colab](https://colab.research.google.com/).
2. **Dataset**: Automatically downloaded from Dicoding GitHub assets (`rockpaperscissors.zip`).
3. **Steps**:
   - Dataset is extracted and split into training and validation sets using `train_test_split`.
   - Data is augmented using `ImageDataGenerator`.
   - Model is trained using a CNN architecture for up to 20 epochs (early stopping at 98% accuracy).
   - After training, the model can predict uploaded image classes.

4. **Prediction Usage**:
   After training, you can upload your own image (e.g., `yourimage.png`), and the model will predict whether it is a **rock**, **paper**, or **scissors** gesture.

   Example:
   ```python
   files.upload()
   ```
The prediction result is printed based on the model's inference.

## Result

- Training Accuracy: Up to 98.3%
- Validation Accuracy: Up to 98.2%
- Loss and Accuracy curves are plotted to evaluate the model's performance visually.

## LICENSE

Copyright &copy; 2023 Ryan Gading Abdullah. All rights reserved.

This project is licensed under the MIT License - see the [MIT LICENSE](LICENSE) for details.
