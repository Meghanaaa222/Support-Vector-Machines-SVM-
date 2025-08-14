# Support Vector Machines (SVM) 

## Project Overview
This project applies the **Support Vector Machines (SVM)** classification algorithm to the well-known **Breast Cancer Wisconsin dataset**.  
The dataset contains features derived from breast mass cell nuclei measurements, with the goal of classifying tumors as **malignant** or **benign**.  
For simplicity and visualization purposes, only the **first two features** of the dataset were used in this experiment.

## What I Did
1. **Data Loading and Preprocessing**  
   - Loaded the **Breast Cancer Wisconsin dataset** from scikit-learn’s built-in datasets.  
   - Selected only the first two features for visualization in a 2D space.  
   - Split the dataset into **training (70%)** and **testing (30%)** sets.  
   - Standardized the feature values to have zero mean and unit variance.

2. **Model Training**  
   - Trained two different SVM models:
     - **Linear Kernel SVM** with C = 1.0.  
     - **RBF Kernel SVM** with C = 1.0 and gamma = 0.7.  

3. **Model Evaluation**  
   - Evaluated both models on the test set using:
     - **Accuracy Score** for overall correctness.  
     - **Classification Report** for precision, recall, and F1-score.

## What I Got (Results)
- **Test Accuracy:**
  - Linear SVM → 91.23%  
  - RBF SVM → 95.32%  

- **Classification Report:**  
  - **Linear SVM:** High precision and recall for both malignant and benign classes, with slightly lower recall for malignant cases compared to RBF.  
  - **RBF SVM:** Overall better balance of precision and recall across both classes, leading to higher accuracy.

## Conclusion
The RBF kernel SVM outperformed the linear kernel SVM in this experiment, achieving higher accuracy and balanced classification metrics.  
Using only two features limited the model's potential, but it allowed for easier visualization and interpretation of decision boundaries.  
For real-world applications, using **all features** and performing **hyperparameter tuning** (via GridSearchCV) could further improve performance.

## How to Use
- Open the notebook in **Jupyter Notebook** or **JupyterLab**.  
- Run all cells in order.  
- The notebook will:
  - Train both Linear and RBF SVM models.  
  - Print accuracy scores and classification reports.  
  - Display visualizations of decision boundaries (if included).  
