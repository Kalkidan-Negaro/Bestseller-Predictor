# Bestseller-Predictor

## Overview
**BookSense** is a predictive analytics project that uses Logistic Regression to determine whether a book is likely to become a bestseller. The project leverages the Goodreads Books dataset and incorporates Exploratory Data Analysis (EDA), feature engineering, model training from scratch, hyperparameter tuning, and performance evaluation.

## Dataset
The project uses the [Goodreads Books Dataset](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks), which contains information about book ratings, reviews, pages, and other metadata. This dataset was chosen for its quality, size, and relevance to predicting book popularity.

## Features
- **average_rating**: The average rating of the book.  
- **ratings_count**: Total number of ratings.  
- **text_reviews_count**: Number of textual reviews.  
- **num_pages**: Total pages in the book.  
- **reviews_per_rating**: New feature representing reviews per rating.  
- **pages_per_rating**: New feature representing pages per rating.

## Target Variable
- **bestseller**: Binary indicator (1 if the book has ratings above a certain threshold, 0 otherwise).

## Methods
1. **Exploratory Data Analysis (EDA)**: Cleaning, checking missing values, visualizing distributions, correlations, and patterns.  
2. **Feature Engineering**: Creating additional features to enhance model performance.  
3. **Model Training**: Logistic Regression implemented from scratch with gradient descent.  
4. **Hyperparameter Tuning**: Testing different learning rates and epochs for optimal performance.  
5. **Evaluation**: Confusion matrix, classification report, ROC-AUC, and threshold tuning.  

## How to Run

1. Clone the repository:  
   ```bash
   git clone <repo_url>
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook `BookSense_Logistic_Regression.ipynb` or the Python scripts in `src/`.

## Results

* Achieved high accuracy in predicting bestseller books.
* Identified key features influencing bestseller status.
* ROC-AUC and confusion matrices demonstrate the model's discriminative ability.

## References

* Kaggle, 2025. Goodreads Books Dataset. [Dataset] Available at: [https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks) [Accessed 22 October 2025].
* Stack Abuse, 2021. Logistic Regression From Scratch in Python. [Online] Available at: [https://stackabuse.com/logistic-regression-from-scratch-in-python/](https://stackabuse.com/logistic-regression-from-scratch-in-python/) [Accessed 24 October 2025].
* Analytics Vidhya, 2020. Logistic Regression: Understanding Gradient Descent. [Online] Available at: [https://www.analyticsvidhya.com/blog/2020/10/logistic-regression-understanding-gradient-descent/](https://www.analyticsvidhya.com/blog/2020/10/logistic-regression-understanding-gradient-descent/) [Accessed 21 October 2025].
* Scikit-learn, n.d. Metrics and scoring: classification metrics. [Online] Available at: [https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics) [Accessed 27 October 2025].
* Scikit-learn, n.d. Preprocessing data. [Online] Available at: [https://scikit-learn.org/stable/modules/preprocessing.html](https://scikit-learn.org/stable/modules/preprocessing.html) [Accessed 23 October 2025].
* Seaborn, n.d. Seaborn: statistical data visualization. [Software] Available at: [https://seaborn.pydata.org/](https://seaborn.pydata.org/) [Accessed 28 October 2025].

