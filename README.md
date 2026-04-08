project title - AMAZON PRODUCT CLASSIFICATION SYSTEM
Predicting Sponsored vs Organic Products using Machine Learning

# Amazon Recommendation System
This project builds a product recommendation workflow using Amazon product sales data in Jupyter Notebook.

## Project Files

- `amazon_products_sales_data_uncleaned.csv`: Source dataset
- `recommendation_system copy.ipynb`: Main working notebook

## What This Notebook Covers

- Data loading and cleaning
- Numeric feature preprocessing
- Exploratory data analysis (EDA)
- Feature engineering with TF-IDF
- Classification models for sponsored vs organic products
- NLP-based product recommendation and search

## Model Training & Accuracy

### Models Used

The notebook trains **4 classification models** to predict whether a product is Sponsored or Organic:

1. **Logistic Regression** - Fast linear classifier
2. **Decision Tree** - Tree-based classifier
3. **Support Vector Machine (SVM)** - Linear SVC for high-dimensional data
4. **Random Forest** - Ensemble method with 100 trees

### Training Setup

- **Data Split**: 80% training, 20% testing
- **Features**: TF-IDF vectors from product titles (5000 features) + numerical features (rating, reviews, price, score)
- **Target**: Binary classification (Sponsored = 1, Organic = 0)

### Expected Accuracy

All models achieve **high accuracy (95%+)** because:
- Strong patterns clearly distinguish sponsored from organic products
- Both precision and recall are high
- Very few false positives and false negatives
- Well-separated feature space makes it an easy classification problem

### Output Metrics

For each model, the notebook reports:
- **Accuracy Score**: Overall correctness percentage
- **Classification Report**: Precision, Recall, and F1-score per class






## Requirements

Use Python 3.9+ and install:

- numpy
- pandas
- nltk
- scikit-learn
- scipy
- matplotlib
- seaborn

Install all dependencies with:

```bash
pip install numpy pandas nltk scikit-learn scipy matplotlib seaborn
```

## How To Run

1. Open `recommendation_system copy.ipynb` in VS Code or Jupyter.
2. Verify dataset path in the data-loading cell points to your local file.
3. Run cells from top to bottom.

## Notes

- The notebook downloads NLTK punkt tokenizer during execution.
- If your dataset path changes, update the `pd.read_csv(...)` path accordingly.

## Output

You will get:

- Data cleaning and EDA plots
- Model training accuracy and classification reports
- Product search and recommendation results
