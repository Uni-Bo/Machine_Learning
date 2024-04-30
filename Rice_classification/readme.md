# Rice Image Classification Project

In this project, I built a Convolutional Neural Network (CNN) for image classification using a rice dataset. Here's a breakdown of the key steps:

## 1. Dataset Preparation:

I utilized the Kaggle API to download a comprehensive rice image dataset containing various rice types, including Arborio, Basmati, Ipsala, Jasmine, and Karacadag. After downloading, I extracted and explored the dataset to grasp its structure.

## 2. Data Exploration and Visualization:

I examined the distribution of images in each category, specifically Arborio and Basmati. To gain visual insights, I employed matplotlib to display sample images from different rice varieties.
![visual](https://github.com/Uni-Bo/Machine_Learning/blob/main/Rice_classification/img/classification.png)

## 3. Data Preprocessing:

Loaded images and organized their paths into separate lists for each rice type. Created a dictionary to map rice varieties to numerical labels. Converted images to arrays and assigned corresponding labels.

## 4. Data Splitting:

Split the dataset into training and testing sets using the `train_test_split` function from scikit-learn.

## 5. Model Building:

Constructed a Sequential model using Keras and TensorFlow, comprising convolutional layers (`Conv2D`), max-pooling layers (`MaxPooling2D`), flattening layers (`Flatten`), and densely connected layers (`Dense`). Incorporated dropout layers to prevent overfitting. Compiled the model using the Adam optimizer and sparse categorical crossentropy loss.

## 6. Model Training:

Trained the model on the training data for 5 epochs.

## 7. Model Evaluation:

Evaluated the trained model on both the training and testing datasets. Generated classification reports to assess precision, recall, and F1-score for each class. The model demonstrated good accuracy on the training set and reasonable effectiveness on the testing set, indicating its ability to generalize.

Classification Report of train set:
              
              precision    recall  f1-score   support

           0       0.84      0.98      0.90      1206
           1       0.93      0.99      0.96      1173
           2       0.98      1.00      0.99      1210
           3       0.99      0.76      0.86      1209
           4       0.99      0.98      0.99      1202

    accuracy                               0.94      6000
    macro avg          0.95      0.94      0.94      6000
    weighted avg       0.95      0.94      0.94      6000

Classification Report of test set:
              
               precision    recall    f1-score   support

           0       0.81      0.94      0.87       294
           1       0.89      0.98      0.93       327
           2       0.96      0.99      0.98       290
           3       0.95      0.71      0.81       291
           4       0.96      0.93      0.95       298

    accuracy                               0.91      1500
    macro avg          0.92      0.91      0.91      1500
    weighted avg       0.92      0.91      0.91      1500

## 8. Model Saving:

Saved the trained model as 'Rice.h5' for future use.

## 9. Conclusion:

This project successfully showcased the development of a CNN model for rice image classification. The model's performance on both training and testing sets provides a solid foundation for further refinements and exploration. To enhance generalization, potential improvements may involve hyperparameter tuning, architectural adjustments, or experimenting with data augmentation techniques.
