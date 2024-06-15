This Machine Learning Cheat Sheet provides a concise overview of various machine learning algorithms, categorized by their types and whether they use supervised or unsupervised learning. It includes brief descriptions, typical use cases, advantages, and disadvantages for each algorithm. This guide is designed to help you quickly understand the key features and applications of popular machine learning models, aiding in the selection of the appropriate algorithm for your data science projects. Whether you're predicting housing prices with Linear Regression or segmenting customers with K-Means clustering, this cheat sheet serves as a handy reference for both beginners and experienced practitioners.

# Machine Learning Cheat Sheet

## Linear Models

### Linear Regression
- **Type**: Supervised Learning
- **Description**: A simple algorithm that models a linear relationship between inputs and a continuous numerical output variable.
- **Use cases**:
  - Stock price prediction
  - Predicting housing prices
  - Predicting customer lifetime value
- **Advantages**:
  - Explainable method
  - Interpretable results by its output coefficients
  - Faster to train than other machine learning models
- **Disadvantages**:
  - Assumes linearity between inputs and outputs
  - Sensitive to outliers
  - Can underfit with small, high-dimensional data

### Ridge Regression
- **Type**: Supervised Learning
- **Description**: Part of the regression family, it penalizes features that have low predictive outcomes by shrinking their coefficients closer to zero. Can be used for classification or regression.
- **Use cases**:
  - Predictive maintenance for automobiles
  - Sales revenue prediction
- **Advantages**:
  - Less prone to overfitting
  - Best suited where data suffer from multicollinearity
  - Explainable and interpretable
- **Disadvantages**:
  - All predictors are kept in the final model
  - Doesn't perform feature selection

### Lasso Regression
- **Type**: Supervised Learning
- **Description**: Part of the regression family, it penalizes features that have low predictive outcomes by shrinking their coefficients to zero. Can be used for classification or regression.
- **Use cases**:
  - Predicting housing prices
  - Predicting clinical outcomes based on health data
- **Advantages**:
  - Less prone to overfitting
  - Can handle high-dimensional data
  - No need for feature selection
- **Disadvantages**:
  - Can lead to poor interpretability as it can keep highly correlated variables

### Logistic Regression
- **Type**: Supervised Learning
- **Description**: A simple algorithm that models a linear relationship between inputs and a categorical output (1 or 0).
- **Use cases**:
  - Credit risk score prediction
  - Customer churn prediction
- **Advantages**:
  - Interpretable and explainable
  - Less prone to overfitting when using regularization
  - Applicable for multi-class predictions
- **Disadvantages**:
  - Assumes linearity between inputs and outputs
  - Can overfit with small, high-dimensional data

## Tree-Based Models

### Decision Tree
- **Type**: Supervised Learning
- **Description**: Decision Tree models make decision rules on the features to produce predictions. It can be used for classification or regression.
- **Use cases**:
  - Customer churn prediction
  - Credit score modeling
  - Disease prediction
- **Advantages**:
  - Explainable and interpretable
  - Can handle missing values
- **Disadvantages**:
  - Prone to overfitting
  - Sensitive to outliers

### Random Forests
- **Type**: Supervised Learning
- **Description**: An ensemble learning method that combines the output of multiple decision trees.
- **Use cases**:
  - Credit score modeling
  - Predicting housing prices
- **Advantages**:
  - Reduces overfitting
  - Higher accuracy compared to other models
- **Disadvantages**:
  - Training complexity can be high
  - Not very interpretable

### XGBoost
- **Type**: Supervised Learning
- **Description**: Gradient Boosting algorithm that is efficient and flexible. Can be used for both classification and regression tasks.
- **Use cases**:
  - Churn prediction
  - Claims processing in insurance
- **Advantages**:
  - Provides accurate results
  - Captures non-linear relationships
- **Disadvantages**:
  - Hyperparameter tuning can be complex
  - Does not perform well on sparse datasets

### LightGBM Regressor
- **Type**: Supervised Learning
- **Description**: A gradient boosting framework that is designed to be more efficient than other implementations.
- **Use cases**:
  - Predicting flight time for airlines
  - Predicting cholesterol levels based on health data
- **Advantages**:
  - Can handle large amounts of data
  - Computationally efficient and fast training speed
  - Low memory usage
- **Disadvantages**:
  - Can overfit due to leaf-wise splitting and high sensitivity
  - Hyperparameter tuning can be complex

### Gradient Boosting Regression
- **Type**: Supervised Learning
- **Description**: Gradient Boosting Regression employs boosting to make predictive models from an ensemble of weak predictive learners.
- **Use cases**:
  - Predicting car emissions
  - Predicting ride-hailing fare amounts
- **Advantages**:
  - Better accuracy compared to other regression models
  - Can handle multicollinearity
  - Can handle non-linear relationships
- **Disadvantages**:
  - Sensitive to outliers and can therefore cause overfitting
  - Computationally expensive and has high complexity

## Clustering

### K-Means
- **Type**: Unsupervised Learning
- **Description**: K-Means is the most widely used clustering approach—it determines K clusters based on Euclidean distances.
- **Use cases**:
  - Customer segmentation
  - Recommendation systems
- **Advantages**:
  - Scales to large datasets
  - Simple to implement and interpret
  - Results in tight clusters
- **Disadvantages**:
  - Requires the expected number of clusters from the beginning
  - Has troubles with varying cluster sizes and densities

### Hierarchical Clustering
- **Type**: Unsupervised Learning
- **Description**: A "bottom-up" approach where each data point is treated as its own cluster—and then the closest two clusters are merged together iteratively.
- **Use cases**:
  - Fraud detection
  - Document clustering based on similarity
- **Advantages**:
  - No need to specify the number of clusters
  - The resulting dendrogram is informative
- **Disadvantages**:
  - Doesn’t always result in the best clustering
  - Not suitable for large datasets due to high complexity

### Gaussian Mixture Models
- **Type**: Unsupervised Learning
- **Description**: A probabilistic model for modeling normally distributed clusters within a dataset.
- **Use cases**:
  - Customer segmentation
  - Recommendation systems
- **Advantages**:
  - Computes a probability for an observation belonging to a cluster
  - Can identify overlapping clusters
  - More accurate results compared to K-means
- **Disadvantages**:
  - Requires complex tuning
  - Requires setting the number of expected mixture components or clusters

## Association

### Apriori Algorithm
- **Type**: Unsupervised Learning
- **Description**: Rule-based approach that identifies the most frequent itemset in a given dataset where prior knowledge of frequent itemset properties is used.
- **Use cases**:
  - Product placements
  - Recommendation engines
  - Promotion optimization
- **Advantages**:
  - Results are intuitive and interpretable
  - Exhaustive approach as it finds all rules based on the confidence and support
- **Disadvantages**:
  - Generates many uninteresting itemsets
  - Computationally and memory intensive
  - Results in many overlapping item sets

## Tips & Useful Links
### Tips

- **Understand Your Data**: Before choosing an algorithm, thoroughly explore and understand your dataset. Know the types of variables you have and the relationships between them.
- **Preprocessing is Key**: Proper data preprocessing (e.g., handling missing values, scaling features) can significantly improve model performance.
- **Cross-Validation**: Use cross-validation techniques to assess the generalizability of your models and prevent overfitting.
- **Hyperparameter Tuning**: Invest time in tuning the hyperparameters of your model to achieve the best performance.

### Useful Links
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html): Comprehensive guide to using one of the most popular machine learning libraries in Python.
- [Kaggle](https://www.kaggle.com/): A platform for data science competitions, datasets, and community-driven learning resources.
- [Coursera Machine Learning Course](https://www.coursera.org/learn/machine-learning): Andrew Ng’s machine learning course, a great starting point for beginners.
- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course): A free, fast-paced introduction to machine learning with TensorFlow APIs.
- [Towards Data Science](https://towardsdatascience.com/): An online publication sharing concepts, ideas, and codes related to data science.
