
# Second Project: Racing Car Classification

## Project Overview
This project focuses on a machine learning classification task aimed at predicting the actions a car can perform based on input images captured in a simulated driving environment. The objectives of the study include:

- Developing two convolutional neural network (CNN) models.
- Evaluating the impact of data augmentation on model performance.
- Addressing challenges posed by an imbalanced and noisy dataset.


## Dataset
- **Source**: Images from Gymnasium's CarRacing environment.
- **Dataset Size**:
  - Training set: 6,369 images.
  - Testing set: 2,749 images.
- **Image Dimensions**: (96, 96, 3).
- **Label Distribution**: Highly imbalanced, with significant disparities across classes.

The possible car actions (Labels) include:
1. Do nothing.
2. Steer left.
3. Steer right.
4. Accelerate.
5. Brake.

### Data Processing
1. **Preprocessing**:
   - Resized and normalized images.
   - One-hot encoding for labels.
   - Training set split: 80% training, 20% validation.

2. **Data Augmentation**:
   - Techniques: Random rotation, random zoom, Gaussian noise.



## Training
- Hyperparameter tuning via grid search.
- Early stopping based on validation loss.
- Models trained on original and augmented datasets for comparative analysis.


## Results

### Model Performance


| Model         | Custom Weighted F1  | Standard Weighted F1 | Accuracy |
|---------------|---------------------|----------------------|----------|
| First NO DA   | 0.74                | 0.66                 | 0.63     |
| First DA      | 0.61                | 0.53                 | 0.54     |
| Second NO DA  | 0.70                | 0.64                 | 0.61     |
| Second DA     | 0.64                | 0.58                 | 0.58     |


<div><video controls src="https://github.com/user-attachments/assets/578bcdca-8159-45ec-8b66-be72901dd876" muted="false" ></video> Video of my best model (2nd CNN, trained without data augmentation) loaded in the Gymnasium's CarRacing
environment </div>

## Tech Used
 ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)  ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) 



