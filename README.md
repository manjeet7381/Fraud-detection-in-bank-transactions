Project Title
Fraud Detection using Machine Learning

Description
This project focuses on building and evaluating machine learning models to identify fraudulent transactions from a dataset of financial transactions. The notebook Fraud Detection.ipynb demonstrates data loading, exploration, preprocessing, model training, and performance evaluation for various classification algorithms.
Introduction
This section provides a brief background on the problem of fraud detection and the importance of machine learning in addressing it. It also outlines the main objectives of this project.

Dataset
The project utilizes two main datasets:

transactions_obf.csv: Contains obfuscated transaction details.
labels_obf.csv: Contains the corresponding fraud labels for events.
Data Description:
The transactions_obf.csv dataset contains approximately 120,000 transactions and includes 10 features, with 9 being categorical (objects and integers) and 1 continuous (transactionAmount). Key columns include:

transactionTime
eventId
accountNumber
merchantId
mcc
merchantCountry
merchantZip (contains ~23,005 null values, which are handled by encoding as a category)
posEntryMode
transactionAmount
availableCash
Methodology
This project employs various machine learning algorithms for fraud detection. The general workflow involves:

Data Importation and Formatting: Loading transaction and label data.
Data Exploration: Analyzing data distributions, checking for null values, and identifying duplicated transactions.
Preprocessing: Handling missing values (e.g., in merchantZip) and preparing categorical features for modeling.
Model Training: Experimenting with a range of models, including:
Support Vector Machines (SVC, NuSVC, OneClassSVM)
Decision Tree Classifier
Random Forest Classifier
AdaBoost Classifier
Gradient Boosting Classifier
Logistic Regression
K-Means (likely for anomaly detection/feature engineering)
K-Nearest Neighbors Classifier
TensorFlow/Keras models (indicating potential for deep learning approaches)
Evaluation: Assessing model performance using metrics such as ROC AUC score, F1 score, confusion matrix, and precision-recall curves. The notebook also includes a bootstrap analysis to evaluate model selection against random selection.
Results
The notebook presents the performance of the trained models. The bootstrap analysis indicates:

Model Selection on Test Set: On average, the model detected [insert average percentage of frauds detected by your model here]% of frauds across 20 bootstrapped datasets.
Random Selection on Test Set: A random selection detected [insert average percentage of frauds detected by random selection here]% of frauds.
(You would replace the bracketed placeholders with the actual results from your notebook's output, for example, np.mean(percent_frauds) and np.mean(percent_frauds_control)).

Conclusion
Summarize the findings and the effectiveness of the models in detecting fraud based on the evaluation metrics. Discuss any insights gained from the data exploration and model performance.
