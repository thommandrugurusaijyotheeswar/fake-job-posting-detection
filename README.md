Fake Job Posting Detection Using Deep Learning
Project Overview
This project uses a Bidirectional Long Short-Term Memory (BiLSTM) neural network to detect potentially fake job postings from job-related text.

The model analyzes textual information from job postings and predicts whether a posting is likely genuine or potentially fake.

Objective
The main objective is to develop a deep learning-based system that can identify suspicious job postings and help reduce the risk of fraudulent job advertisements.

Dataset
Dataset: Real or Fake Fake Job Posting Prediction

The dataset contains real and fraudulent job postings.

The dataset is highly imbalanced, with genuine job postings being much more common than fake job postings.

Methodology
The project follows these steps:

Load the job posting dataset
Clean and combine relevant text fields
Remove duplicate and empty records
Split the data into training, validation and testing sets
Tokenize the job-posting text
Apply sequence padding
Train a BiLSTM deep learning model
Evaluate the model using accuracy, precision, recall and F1-score
Analyze classification errors
Perform an ablation study with and without dropout
Model Architecture
The final model consists of:

Embedding Layer
Bidirectional LSTM Layer
Dropout Layer
Dense Layer
Dropout Layer
Output Layer with Sigmoid activation
Class weights were used during training to handle the class imbalance.

Dataset Split
Training samples: 11,024
Validation samples: 2,362
Testing samples: 2,363
Final Results
The verified final BiLSTM model achieved:

Metric	Score
Accuracy	98.05%
Precision (Fake)	80.61%
Recall (Fake)	74.53%
F1-score (Fake)	77.45%
Confusion Matrix
Predicted Genuine	Predicted Fake
Actual Genuine	2,238	19
Actual Fake	27	79
Error Analysis
The final test evaluation identified:

19 false positives
27 false negatives
These errors were analyzed to understand cases where genuine postings were classified as fake and fake postings were classified as genuine.

Ablation Study
A second BiLSTM model without dropout was trained to study the effect of dropout.

The comparison showed that dropout produced a slightly better F1-score in the experiments, while the difference was relatively small.

Technologies Used
Python
TensorFlow / Keras
NumPy
Pandas
Scikit-learn
Matplotlib
Google Colab
Project Files
Fake_Job_Detection_BiLSTM.ipynb - Complete project notebook
requirements.txt - Python dependencies
project_results/ - Model, tokenizer, metrics, graphs and analysis results
Limitations
The dataset is imbalanced, so accuracy alone is not sufficient to measure fake-job detection performance. Precision, recall and F1-score for the fake class are also considered.

The model prediction should be treated as a screening result and not as proof that a job posting is fraudulent.

Future Work
Future improvements could include:

Larger and more diverse datasets
Transformer-based models
Better handling of class imbalance
Hyperparameter optimization
Deployment as a web or mobile application
Author
Fake Job Posting Detection Using Deep Learning
