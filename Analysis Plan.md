# 2. Analysis Plan

The objective of this project is to develop a Logistic Regression model from scratch to predict whether a book will become a bestseller using features from the Goodreads Books Dataset. A structured plan ensures that the analysis is comprehensive, reproducible, and interpretable.

---

## 2.1 Exploratory Data Analysis (EDA)

The first step is to understand and clean the dataset. The key steps include:

1. **Data Inspection**

   * Examine the dataset’s structure, including the number of entries, features, data types, and basic summary statistics.
   * Identify and remove duplicates to ensure no book is counted more than once.

2. **Missing Values and Data Cleaning**

   * Identify missing or null values in critical features such as `average_rating`, `ratings_count`, `text_reviews_count`, and `num_pages`.
   * Decide whether to remove, impute, or adjust missing entries to ensure numeric features required for Logistic Regression are complete.

3. **Distribution Analysis**

   * Create histograms, boxplots, and kernel density estimates (KDE) for numeric features to visualise distributions, identify skewness, and detect potential outliers.
   * For instance, `ratings_count` and `text_reviews_count` may exhibit long-tailed distributions.

4. **Correlation and Relationships**

   * Generate a correlation heatmap to examine relationships between numeric variables.
   * Use scatterplots to understand how `average_rating` or `num_pages` relates to reader engagement metrics.
   * Investigate possible non-linear relationships that may enhance feature engineering.

5. **Outlier Detection**

   * Identify extreme values that could disproportionately influence the Logistic Regression model.
   * Plan to apply normalisation or scaling techniques to reduce the impact of outliers.

---

## 2.2 Feature Selection and Engineering

Effective feature selection is crucial for model performance:

1. **Primary Features**

   * Include numeric predictors: `average_rating`, `ratings_count`, `text_reviews_count`, `num_pages`.

2. **Feature Engineering**

   * Create new features:

     * `reviews_per_rating` = `text_reviews_count` / (`ratings_count` + 1)
     * `pages_per_rating` = `num_pages` / (`ratings_count` + 1)
   * These engineered features provide additional insights into reader engagement and book length relative to popularity.

3. **Handling Multicollinearity**

   * Assess correlations among features; remove or combine highly correlated predictors to avoid redundancy and overfitting.

4. **Target Variable Definition**

   * Define `bestseller` as a binary target based on a threshold of `ratings_count` (e.g., >50,000 ratings = 1, otherwise 0).

5. **Feature Selection Techniques**

   * Apply backward elimination or forward selection using p-values to identify statistically significant features.

---

## 2.3 Model Training

This stage involves preparing the data and training the Logistic Regression model:

1. **Data Preparation**

   * Normalise or standardise numeric features to ensure equal weighting.
   * Split the dataset into training (80%) and test (20%) sets to evaluate generalisation performance.

2. **Logistic Regression Implementation**

   * Train the model from scratch using gradient descent.
   * Include a bias term and apply the sigmoid activation function.

3. **Hyperparameter Tuning**

   * Test different learning rates (`0.01, 0.05, 0.1`) and epochs (`500, 1000, 2000`) to optimise model performance.
   * Monitor iterative training and loss curves to ensure convergence.

---

## 2.4 Model Interpretation and Evaluation

After training, assess the model’s effectiveness using multiple metrics:

1. **Performance Metrics**

   * Evaluate Accuracy, Precision, Recall, F1-score, and Confusion Matrix.
   * Use the ROC-AUC curve to assess discriminative ability.

2. **Threshold Tuning**

   * Adjust decision thresholds (e.g., 0.4, 0.5, 0.6) to balance sensitivity and specificity.

3. **Feature Importance**

   * Analyse model coefficients to determine which features significantly impact bestseller prediction.

4. **Retraining and Refinement**

   * Retrain the model if necessary based on performance outcomes.
   * Address class imbalance if non-bestsellers dominate, using resampling or weighted loss functions.

---

## 2.5 Reporting

The final stage involves compiling the analysis and results:

* Present all EDA visualisations with corresponding interpretations.
* Document feature selection, engineering, and preprocessing methods.
* Detail model training procedures, including hyperparameters and loss curves.
* Report performance metrics and provide clear explanations of results.
* Discuss limitations, potential improvements, and actionable insights regarding factors influencing bestseller status.
