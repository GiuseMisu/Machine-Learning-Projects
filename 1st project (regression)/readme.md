
# First Project: Forward Kinematics Prediction 

## Project Overview
This project addresses the application of machine learning models to solve the forward kinematics problem for robotic systems. Specifically, it explores three robotic configurations:

- **R2**: A 2-joint planar robot.
- **R3**: A 3-joint planar robot.
- **R5**: A 5-joint 3D robot.

The primary goal is to predict the end-effector's position and orientation based on the robot’s joint angles. The project involves:
- Developing predictive models for forward kinematics.
- Estimating the Jacobian matrix using learned models.
- Evaluating performance across varying dataset sizes and configurations.


## Features and Datasets

### Datasets
- Three datasets correspond to the robot configurations (R2, R3, R5).
- Each dataset contains 100,000 samples generated via simulations with random joint angles.
- A smaller subset (1,000 samples) was used to evaluate model performance under limited data conditions.

### Features
- Input: Joint angles.
- Outputs: Position and orientation of the end-effector.
- Additional derived features (e.g., sine and cosine values of joint angles) were excluded to simplify learning.

### Data Preprocessing
- No normalization applied, as joint angles are already within defined numerical ranges.
- Training and testing splits: 70% training and 30% testing.


## Methodology

### Models and Approaches
1. **R2 Task**: Utilized a deep ensemble of shallow neural networks.
2. **R3 Task**: Applied AdaBoost regression with decision tree estimators.
3. **R5 Task**: Used a wide neural network architecture.

### Jacobian Estimation
- **Gradient-based method**: Leveraged TensorFlow’s `GradientTape` for R2 and R5 tasks.
- **Numerical differentiation**: Used for R3 task due to limitations of AdaBoost.
- **Evaluation**: Frobenius distance between learned and analytical Jacobians.


## Results

### Model Performance

| Task   | MSE (Limited Data) | MSE (Original Dataset) |
|--------|----------------------|------------------------|
| R2     | 0.00004             | 0.000005              |
| R3     | 0.004041            | 0.000225              |
| R5     | 0.000185            | 0.000028              |


## Tech Used
 ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)  ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
 ![Seaborn](https://img.shields.io/badge/Seaborn-%2300B4D8.svg?style=for-the-badge&logo=seaborn&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) 
