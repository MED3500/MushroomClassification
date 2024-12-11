![](UTA-DataScience-Logo.png)

# Mushroom Classification Project

* **One Sentence Summary**: This repository tackles the problem of classifying mushrooms as edible or poisonous using the [Kaggle Mushroom Classification dataset](https://www.kaggle.com/datasets/uciml/mushroom-classification/data), employing machine learning models to predict mushroom safety based on their physical characteristics.

## Overview

* **Task/Challenge**: The goal is to predict whether a mushroom is edible or poisonous based on its physical traits, like cap shape, odor, and habitat, in this binary classification problem.

* **Approach**: The dataset is split into training and testing sets, with the features (excluding the target variable) being one-hot encoded using a pipeline that integrates preprocessing and model training. A Random Forest classifier is used, and the model is trained on the training data and evaluated on the test data. The performance is measured using accuracy, with results printed as a percentage.

* **Performance Summary**: I achieved an accuracy of 100%.

## Summary of Work Done

### Data

* **Data**:
  * **Type**: CSV file with 23 categorical features describing mushrooms, and a target variable (`class`) indicating whether the mushroom is edible (e) or poisonous (p).
  * **Size**: 8124 rows and 23 columns.
  * **Split**: The dataset is balanced, with 4208 edible and 3916 poisonous mushrooms. I used an 80/20 split to train.

#### Preprocessing

* No missing values were found, and all features are categorical. One-hot encoding was used to convert categorical features into numerical format for model input.

#### Data Visualization

* Class distribution is nearly balanced, with edible mushrooms slightly outnumbering poisonous ones. Being edible or inedible is very highly correlated to the rest of the data, as is shown by the heatmap.

### Problem Formulation

* **Input/Output**:  
  * **Input**: 23 categorical features describing mushroom attributes.  
  * **Output**: Binary classification (edible `e` or poisonous `p`).

* **Models**:  A **Random Forest Classifier** is used for its ability to handle categorical data and provide accurate predictions.

* **Loss, Optimizer, and Hyperparameters**:  
  The model uses **accuracy** as the evaluation metric. Hyperparameters include 100 trees and a fixed random seed. Preprocessing is done with **OneHotEncoder**.

### Training

* **How**:  The model is trained using a **Pipeline** that applies **OneHotEncoder** for categorical features and **Random Forest Classifier** with 100 trees.

* **Training Time**: Training is quick, taking only a minute or two.

* **Stopping Criteria**: The model trains until fully fitted, with no early stopping needed.

* **Challenges**:  The main challenge was ensuring proper encoding of categorical features, which was managed within the pipeline.

### Performance Comparison

* **Key Metrics**: Accuracy was the primary metric, with confusion matrices and classification reports to evaluate model performance.

* **Results (values written down from other test files)**:
  | Model            | Accuracy |
  |------------------|----------|
  | Decision Tree    | 100%     |
  | Logistic Reg.    | 98%      |
  | SVM (RBF)        | 97%      |

* **Visualization**: Confusion matrices highlight model performance across true positives, false positives, etc.

### Conclusions

* Logistic regression was the most accurate model, achieving 98%. This suggests it is well-suited for this classification task.

### Future Work

* From here I would like to take a try at the other datasets. I was originally working on the Bank Churn data set but my work was deleted. The same thing happened when I first tried to add the Mushroom Classification file. Because of the time constraint I had to switch to the Mushroom dataset to be able to submit everything on time, though I would like to go back and attempt the Bank Churn project again.

## How to Reproduce Results

* **Reproduce**: 
  1. Clone this repository.
  2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/uciml/mushroom-classification/data).
  3. Run the Python file to train and evaluate the models.

* **Resources**: I used Jupyter Notebook, I'd recommend using the same.

### Overview of Files

There are only two files in the repo - the README file and the MushroomClassification.ipynb. The ipynb file is the only one you need to run to reproduce my results.

### Software Setup

* **Packages**:
  * pandas
  * scikit-learn
  * matplotlib
  * seaborn

* **Installation**:
  ```bash
  pip install pandas scikit-learn matplotlib seaborn
  ```

### Data

* Download the dataset from [Mushroom Classification Dataset](https://www.kaggle.com/datasets/uciml/mushroom-classification/data). You will likely need to create an account before you can view and download the data.

### Training

* The test and training sections of the dataset is already divided in the .ipynb file in a 80/20 split.

### Performance Evaluation

* The .ipynb file currently runs with 100% accuracy. All numbers from earlier attempts were written down, and the files have since been deleted (the files were corrupted - it was pure luck that they were written down)

## Citations

[Pipeline Documentation](https://scikit-learn.org/1.5/modules/generated/sklearn.pipeline.Pipeline.html)

[OneHotEncoder Documentation](https://scikit-learn.org/dev/modules/generated/sklearn.preprocessing.OneHotEncoder.html)
