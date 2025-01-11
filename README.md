# Recognizing-HandWritten-Digits-using-Machine-Learning :rocket:
Recognizing HandWritten digits using Machine Learning Techniques - MLP &amp; SVM

# Project Overview :sparkles:
Develop a model to recognize handwritten digits (0-9). 
Used handwritten digits data set provided by scikit-learn.
Divided data set into train and test data.
Two machine learning techniques were mainly followed to develop the model.
MLP and SVM were used.

####  :point_right: MLP
The Multi-Layer Perceptron Classifier was used under the Neural Network to develop the model.
&nbsp;&nbsp;&nbsp;&nbsp; Proven 0.9146800501882058 Accuracy.

#### :point_right: SVM
The SVC ( Support Vector Classifier) of SVM was used.
&nbsp;&nbsp;&nbsp;&nbsp; Proven 0.9698870765370138 Accuracy.

## Conclusion :white_check_mark:
In summary, SVM's superior performance is likely due to its suitability for small to medium-sized, well-structured datasets while MLP requires more careful tuning and sufficient data to shine.

## Reasons for why SVM was the most suitable model for this :question:

- Handwritten digits are often linearly or near-linearly separable in transformed spaces, which SVM handles well.
- If the dataset is noise-free and has a clear structure, SVM can efficiently utilize this for better accuracy.

- Less prone to overfitting with appropriate regularization (C parameter).

- Faster to train on smaller datasets since it uses fewer parameters.
- while MLP-training a neural network can be computationally expensive, especially with many iterations and layers.

- SVM - Simpler and optimized for binary or multi-class classification tasks, especially with kernel functions like RBF (Radial Basis Function).

- SVM - Works well with smaller datasets and can effectively find the optimal decision boundary.
- MLP - Requires larger datasets to train effectively because it learns complex patterns through multiple layers.


##  :pushpin: Optimize SVM for better results in Recognizing Handwritten digits

Focused on tuning hyperparameters for the SVM model. Hyperparameters are as follows:
  - 'C': Regularization parameter
  - 'gamma': Kernel coefficient
  -  'kernel': Kernel type

### :point_right: Grid search method  
- Obtained (gamma=0.001, C = 10, kernel = 'rbf') combination.
- Proven accuracy - 0.9698870765370138

### :point_right: Random Search method
- Obtained (gamma= 0.597850157946487, C=78.06910002727692, kernel='linear') combination.
- Proven accuracy - 0.9422835633626098

Therefore, 
Grid search cv gives the best hyperparameter tuning for recognizing handwritten digits.

## Insights gain from this hyperparameters tuning :bulb:
- Grid Search systematically evaluates all parameter combinations in the search space. Random Search samples parameters randomly and might miss the optimal region, especially if the search space is large and the number of iterations is limited.
- For simpler datasets (like handwritten digit recognition), the search space may not be too large, making Grid Search more feasible and effective. Random Search is more advantageous for large, complex datasets with high-dimensional hyperparameter spaces.
- Grid Search systematically covers the entire space, ensuring the best parameters in the given search space are found. Random Search depends on random sampling, introducing variability that could lead to suboptimal results.
- Random Search evaluates a fixed number of parameter combinations (n_iter). If this number is too low, the search may not explore enough combinations to find the global optimum, unlike Grid Search, which exhaustively evaluates all combinations.
- Recognition of handwritten digits often benefits from specific ranges of hyperparameters. Grid Search may have better captured the interaction between C and gamma parameters because of its exhaustive approach, especially for nonlinear kernels like RBF.









