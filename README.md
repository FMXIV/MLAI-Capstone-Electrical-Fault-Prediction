# Predicting Failures in Power Transmission Lines

This project aims to develop a predictive model that can accurately forecast failures in power transmission lines before they occur. This will help optimize maintenance schedules, reduce downtime, and improve operational efficiency in utility networks. We applied the CRISP-DM methodology to guide our analysis and modeling. Here’s a summary of our findings:

## Business Understanding

### Objective
The objective of this project is to develop a predictive model that can accurately forecast failures in power transmission lines before they occur. This will help optimize maintenance schedules and reduce downtime.

### Context
Predictive maintenance in utility networks is crucial due to the high costs associated with equipment failures, both in terms of repair expenses and lost productivity. Accurate failure prediction can prevent costly unplanned outages and improve operational efficiency.

### Goals
- Develop a predictive model with high accuracy and precision.
- Enable preemptive maintenance interventions.
- Minimize unplanned downtime and extend the lifespan of machinery.

### Research Question
Can machine learning algorithms accurately predict failures in power transmission lines before they occur, thereby optimizing maintenance schedules and reducing downtime?

## Data Understanding

### Data Sources
- Dataset: [Electrical Fault Detection and Classification](https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification)

### Data Collection
The project uses two CSV files:
1. `detect_dataset.csv`: Contains current and voltage measurements along with an output indicating whether a fault occurred.
2. `classData.csv`: Contains class labels and current and voltage measurements.

### Initial Data Exploration
We performed basic statistics and visualizations to understand the data distribution and checked for any missing values or inconsistencies.

## Data Preparation

### Data Cleaning
- Dropped columns with all missing values from the datasets.

### Data Transformation
- Normalized the current and voltage data for better model performance using StandardScaler.

### Data Splitting
- Split the data into training and testing sets for model training and evaluation.

## Modeling

### Model Selection
We evaluated the performance of four classifiers:
- Logistic Regression
- Random Forest
- Gradient Boosting Machine (GBM)
- Neural Networks

### Model Training
Trained each model on the training data and evaluated their performance.

## Evaluation

### Model Evaluation
Each model was evaluated based on accuracy, precision, recall, F1-score, and ROC-AUC. Here are the key findings:

1. **Logistic Regression:**
   - Accuracy: 73.72%
   - Precision: 100%
   - Recall: 42.37%
   - F1 Score: 59.53%
   - ROC AUC: 71.19%

2. **Random Forest:**
   - Accuracy: 99.79%
   - Precision: 99.64%
   - Recall: 99.91%
   - F1 Score: 99.77%
   - ROC AUC: 99.80%

3. **Gradient Boosting Machine (GBM):**
   - Accuracy: 99.63%
   - Precision: 99.73%
   - Recall: 99.45%
   - F1 Score: 99.59%
   - ROC AUC: 99.61%

4. **Neural Network:**
   - Accuracy: 99.38%
   - Precision: 99.63%
   - Recall: 98.99%
   - F1 Score: 99.31%
   - ROC AUC: 99.34%

### Insights

- Logistic Regression: While Logistic Regression achieved a high precision, it struggled with recall. This indicates that while the model is good at identifying true positives (faults), it misses many actual faults, leading to a lower recall and F1 score.

- Random Forest: The Random Forest model performed exceptionally well across all metrics, indicating a balanced ability to correctly identify faults and non-faults. It achieves high accuracy, precision, recall, and F1 score, making it a robust model for this task.

- Gradient Boosting Machine (GBM): The GBM also performed very well, slightly lower than the Random Forest in some metrics but still providing high accuracy, precision, recall, and F1 score. This indicates it is also a strong model for predicting faults.

- Neural Network: The Neural Network model showed strong performance, slightly lower than Random Forest and GBM. It achieved high accuracy and precision, with a very good recall and F1 score, indicating it is effective at predicting faults.
