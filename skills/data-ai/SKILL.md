---
name: data-ai
description: Master data science, machine learning, MLOps, and AI engineering. Learn Python data analysis, statistical modeling, neural networks, LLM applications, and prompt engineering. Build data-driven solutions and AI applications. Use when learning data science, machine learning, or AI development.
---

# Data & AI Skill

## Quick Start

### Python Data Analysis
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Load & explore data
df = pd.read_csv('data.csv')
print(df.head())
print(df.describe())

# Data manipulation
df['new_column'] = df['col1'] + df['col2']
df_filtered = df[df['age'] > 25]

# Grouping & aggregation
sales_by_region = df.groupby('region')['sales'].sum()

# Visualization
plt.scatter(df['x'], df['y'])
plt.show()
```

### Machine Learning with Scikit-Learn
```python
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, precision_score

# Data splitting
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Preprocessing
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)

# Model training
model = RandomForestClassifier(n_estimators=100)
model.fit(X_train_scaled, y_train)

# Evaluation
y_pred = model.predict(X_test)
print(f"Accuracy: {accuracy_score(y_test, y_pred)}")
print(f"Precision: {precision_score(y_test, y_pred)}")
```

### Deep Learning with TensorFlow
```python
import tensorflow as tf
from tensorflow import keras

# Model architecture
model = keras.Sequential([
    keras.layers.Dense(128, activation='relu', input_shape=(784,)),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(10, activation='softmax')
])

# Compilation
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)

# Training
model.fit(X_train, y_train, epochs=10, batch_size=32, validation_split=0.2)

# Evaluation
test_loss, test_acc = model.evaluate(X_test, y_test)
print(f"Test accuracy: {test_acc}")
```

### LLM Integration (Anthropic Claude)
```python
import anthropic

client = anthropic.Anthropic()

# Simple message
message = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Explain machine learning"}
    ]
)
print(message.content[0].text)

# Multi-turn conversation with RAG
messages = [
    {"role": "user", "content": "What is vector search?"}
]
response = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=1024,
    messages=messages
)

messages.append({"role": "assistant", "content": response.content[0].text})
messages.append({"role": "user", "content": "How is it implemented?"})

response = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=1024,
    messages=messages
)
```

### Prompt Engineering Techniques
```python
# Few-shot learning
prompt = """
Classify the following reviews as positive or negative:

Review: "Great product, highly recommend!"
Label: Positive

Review: "Terrible quality, waste of money"
Label: Negative

Review: "It's okay, nothing special"
Label: """

# Chain-of-thought prompting
prompt = """
Solve this step by step:
What is 25% of 200?

Step 1: Convert percentage to decimal
Step 2: Multiply by the number
Step 3: Result
"""

# System prompt for AI agents
system_prompt = """You are a helpful data analyst.
- Ask clarifying questions
- Provide step-by-step analysis
- Explain your reasoning
- Suggest improvements"""
```

## Data Analysis Fundamentals

### Python Libraries
- **Pandas:** Data manipulation & analysis
- **NumPy:** Numerical computing
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical visualization
- **Plotly:** Interactive visualizations
- **SciPy:** Scientific computing

### Data Exploration
- Data types & structure
- Missing values handling
- Outlier detection
- Statistical summary
- Correlation analysis
- Distribution analysis

### Data Cleaning
- Missing value imputation
- Outlier removal/treatment
- Duplicate detection
- Data type conversion
- Normalization & scaling
- Handling categorical variables

### Exploratory Data Analysis (EDA)
- Univariate analysis
- Bivariate analysis
- Correlation heatmaps
- Distribution plots
- Categorical analysis
- Feature relationships

## Machine Learning

### Machine Learning Types
- **Supervised:** Classification, Regression
- **Unsupervised:** Clustering, Dimensionality reduction
- **Reinforcement:** Learning from feedback

### Classification Algorithms
- **Logistic Regression:** Linear classifier
- **Decision Trees:** Interpretable model
- **Random Forest:** Ensemble method
- **SVM:** Support Vector Machines
- **Naive Bayes:** Probabilistic classifier
- **K-Nearest Neighbors:** Instance-based

### Regression Algorithms
- **Linear Regression:** Simple linear relationship
- **Polynomial Regression:** Non-linear relationships
- **Ridge/Lasso Regression:** Regularized regression
- **Gradient Boosting:** Ensemble boosting (XGBoost, LightGBM)
- **Neural Networks:** Deep learning regression

### Clustering Algorithms
- **K-Means:** Centroid-based clustering
- **Hierarchical Clustering:** Tree-based clustering
- **DBSCAN:** Density-based clustering
- **Gaussian Mixture Models:** Probabilistic clustering

### Dimensionality Reduction
- **PCA:** Principal Component Analysis
- **t-SNE:** Visualization technique
- **UMAP:** Modern dimensionality reduction
- **Feature Selection:** Selecting important features

### Model Evaluation
- **Classification Metrics:** Accuracy, Precision, Recall, F1, ROC-AUC
- **Regression Metrics:** MAE, MSE, RMSE, R²
- **Cross-validation:** K-fold, stratified
- **Hyperparameter Tuning:** Grid search, random search, Bayesian

## Deep Learning

### Neural Network Basics
- **Neurons:** Activation functions (ReLU, sigmoid, tanh)
- **Layers:** Input, hidden, output
- **Backpropagation:** Gradient computation
- **Optimization:** SGD, Adam, RMSprop
- **Regularization:** Dropout, L1/L2, batch normalization

### CNN (Convolutional Neural Networks)
- **Use Cases:** Image classification, object detection
- **Layers:** Convolutional, pooling, flattening
- **Architectures:** LeNet, AlexNet, VGG, ResNet, EfficientNet
- **Transfer Learning:** Pre-trained models

### RNN (Recurrent Neural Networks)
- **Use Cases:** Time series, NLP, sequence modeling
- **Types:** LSTM, GRU
- **Applications:** Language modeling, sentiment analysis
- **Encoder-Decoder:** Sequence-to-sequence models

### Transformers & LLMs
- **Attention Mechanism:** Query, key, value
- **Transformer Architecture:** Multi-head attention, feed-forward
- **LLM Training:** Pre-training, fine-tuning
- **Prompt Engineering:** Instruction tuning, few-shot learning
- **RAG (Retrieval Augmented Generation):** Combining knowledge bases with LLMs

## MLOps & Model Deployment

### Model Development Lifecycle
1. **Problem Definition:** Business understanding
2. **Data Collection:** Gather training data
3. **EDA & Preprocessing:** Understand & clean data
4. **Feature Engineering:** Create meaningful features
5. **Model Development:** Train & validate
6. **Hyperparameter Tuning:** Optimize performance
7. **Model Evaluation:** Comprehensive testing
8. **Deployment:** Production deployment
9. **Monitoring:** Ongoing performance tracking
10. **Retraining:** Update with new data

### Experiment Tracking
- **MLflow:** Experiment logging & model registry
- **Weights & Biases:** Comprehensive ML management
- **Neptune.ai:** Experiment tracking
- **Tracking Metrics:** Loss, accuracy, hyperparameters

### Model Serving
- **TensorFlow Serving:** REST API for models
- **TorchServe:** PyTorch model serving
- **BentoML:** Multi-framework serving
- **FastAPI:** Custom REST APIs
- **Docker:** Containerized serving

### Monitoring & Retraining
- **Data Drift:** Detecting distribution changes
- **Model Drift:** Performance degradation
- **Alerting:** Automated notifications
- **Retraining Pipelines:** Automated updates
- **A/B Testing:** Comparing model versions

## AI Engineering & Prompt Engineering

### Prompt Engineering Techniques
- **System Prompts:** Setting context & behavior
- **Few-Shot Learning:** Providing examples
- **Chain-of-Thought:** Step-by-step reasoning
- **Constraint-Based:** Specific output requirements
- **Role-Based:** Adopting personas

### RAG (Retrieval Augmented Generation)
- **Vector Embeddings:** Semantic representations
- **Vector Databases:** Pinecone, Milvus, Weaviate
- **Semantic Search:** Finding relevant information
- **Context Integration:** Combining retrieval with generation

### AI Agent Development
- **Tool Integration:** API/function calling
- **Decision Making:** Planning & execution
- **Memory:** Conversation history
- **Multi-agent Systems:** Coordination between agents

### LLM Safety & Ethics
- **Bias Detection:** Identifying fairness issues
- **Jailbreaking:** Understanding vulnerabilities
- **Red Teaming:** Adversarial testing
- **Responsible AI:** Ethical guidelines
- **Transparency:** Explainability & interpretability

## Data Engineering for Data Science

### Data Pipeline
- **ETL/ELT:** Extract, transform, load
- **Airflow:** Workflow orchestration
- **dbt:** Data transformation
- **Apache Spark:** Distributed processing
- **Kafka:** Event streaming

### Databases
- **SQL Databases:** PostgreSQL, MySQL
- **NoSQL:** MongoDB, Cassandra
- **Data Warehouses:** Snowflake, BigQuery
- **Data Lakes:** S3, HDFS
- **Vector DBs:** For embeddings

## Statistics & Mathematics

### Statistics for Data Science
- **Descriptive Statistics:** Mean, median, variance
- **Probability:** Distributions, independence
- **Hypothesis Testing:** T-tests, chi-square
- **Bayesian Statistics:** Prior, likelihood, posterior
- **Time Series Analysis:** ARIMA, seasonality

### Linear Algebra
- **Vectors & Matrices:** Operations, properties
- **Eigenvalues & Eigenvectors:** Dimensionality reduction
- **Matrix Decomposition:** SVD, QR
- **Norms & Distances:** Similarity metrics

### Calculus
- **Derivatives:** Gradient computation
- **Chain Rule:** Backpropagation
- **Optimization:** Gradient descent
- **Integration:** Area under curves

## When to Use This Skill

### Data Science Scenarios
- Analyzing datasets
- Building ML models
- Time series forecasting
- Classification tasks
- Recommendation systems
- Anomaly detection

### AI Engineering
- Developing LLM applications
- Building AI agents
- Prompt optimization
- RAG systems
- Chatbots & assistants

### MLOps
- Model deployment
- Monitoring systems
- Retraining pipelines
- Experiment tracking
- Data & model versioning

## Resources

- **Python Libraries:** Pandas, NumPy, scikit-learn docs
- **Deep Learning:** TensorFlow, PyTorch documentation
- **ML:** Coursera ML specialization, Andrew Ng courses
- **Data Science:** Kaggle datasets & competitions
- **LLMs:** OpenAI, Anthropic, HuggingFace
- **Statistics:** StatQuest with Josh Starmer
- **Best Practices:** MLOps.community, papers with code
