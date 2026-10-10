# Spam Classification

## Overview
This project aims to predict whether an email is spam or not using Machine Learning to support automated email filtering. A robust spam filter reduces exposure to phishing and malware, protects user inboxes, and saves time.

## Files
- `exploration.ipynb`: The main Jupyter Notebook containing the full pipeline: problem framing, data wrangling, model training, evaluation, and hyperparameter tuning.
- `emails.csv`: The dataset containing email text data and their respective binary labels (`1` for spam, `0` for not spam).
- `archive.zip`: Compressed archive of related project data.

## Workflow Pipeline
1. **Problem Framing**: Defining the primary goal (spam detection as a binary classification problem) and the evaluation metrics (ROC-AUC and F1-score).
2. **Data Collection & Exploration**: Loading the dataset and analyzing the distribution of classes.
3. **Data Wrangling & Feature Engineering**: 
   - Extracting various numerical features from the text (number of characters, words, sentences, punctuation, uppercase ratio, digits).
   - Employing `TfidfVectorizer` for text vectorization.
   - Creating a scikit-learn `Pipeline` and `ColumnTransformer` to handle both numeric and text features seamlessly.
4. **Modeling**: Training several baseline and advanced classifiers:
   - Support Vector Classifier (SVC)
   - Decision Tree
   - Naive Bayes (MultinomialNB)
   - Random Forest
   - Gradient Boosting
5. **Evaluation**: Comparing model performance using cross-validation over the training data and computing metrics like Accuracy, ROC-AUC, and F1-score.
6. **Hyperparameter Tuning**: Identifying the best hyperparameters for optimal generalization using `GridSearchCV`.

## Requirements
- Python 3.x
- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `wordcloud`

## Usage
Simply start a Jupyter Notebook server and run all the cells within `exploration.ipynb` to follow the workflow from data preprocessing to final model evaluation.
