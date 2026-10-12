# Wine Dataset Analysis and Classification Using Gaussian Naive Bayes

## 📌 Project Overview

This project explores the Wine Dataset through **Exploratory Data Analysis (EDA)** and applies the **Gaussian Naive Bayes** algorithm to classify wines into three distinct classes.

The project demonstrates a complete introductory machine learning workflow, including data exploration, statistical analysis, visualization, model training, prediction, and performance evaluation.

## 🎯 Objectives

- Understand the structure and characteristics of the Wine Dataset.
- Perform Exploratory Data Analysis to identify patterns and relationships.
- Visualize feature distributions, potential outliers, and correlations.
- Train a Gaussian Naive Bayes classification model.
- Evaluate the model using accuracy, a classification report, and a confusion matrix.

## 📊 Dataset Description

The project uses a CSV version of the Wine Dataset containing chemical measurements of wines belonging to three classes.

| Dataset Property | Description |
|---|---|
| Total Samples | 178 |
| Total Columns | 14 |
| Input Features | 13 |
| Target Variable | `Wine` |
| Number of Classes | 3 |
| Problem Type | Multiclass Classification |

### Features

The dataset includes the following chemical measurements:

- Alcohol
- Malic Acid
- Ash
- Alcalinity of Ash (`Acl`)
- Magnesium (`Mg`)
- Total Phenols
- Flavanoids
- Nonflavanoid Phenols
- Proanthocyanins (`Proanth`)
- Color Intensity (`Color.int`)
- Hue
- OD280/OD315 of Diluted Wines (`OD`)
- Proline

The `Wine` column represents the target class, with labels 1, 2, and 3.

### Class Distribution

| Wine Class | Number of Samples |
|---|---:|
| Class 1 | 59 |
| Class 2 | 71 |
| Class 3 | 48 |
| **Total** | **178** |

## 🔍 Exploratory Data Analysis (EDA)

The following EDA techniques were performed:

1. **Dataset Inspection:** Examined the first and last records, dimensions, column names, and data types.
2. **Statistical Summary:** Analyzed descriptive statistics, including mean, standard deviation, minimum, maximum, and quartiles.
3. **Class Distribution:** Examined the number of samples in each wine class using a count plot.
4. **Feature Distributions:** Used histograms to understand the distribution of numerical features.
5. **Outlier Analysis:** Used box plots to identify potential outliers.
6. **Feature Comparison:** Compared alcohol measurements across wine classes.
7. **Relationship Analysis:** Created a scatter plot to examine alcohol content against color intensity.
8. **Correlation Analysis:** Used a correlation matrix and heatmap to investigate relationships among numerical features.
9. **Data Quality Checks:** Checked for missing values and duplicate rows.
10. **Class-wise Statistics:** Compared selected feature averages across the three wine classes.

## 🤖 Machine Learning Model

### Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem. It assumes that the numerical features follow Gaussian (normal) distributions within each class and treats the features as conditionally independent given the class.

It is suitable for this project because the dataset contains continuous numerical measurements and three target classes.

### Model Workflow

1. Separated the dataset into input features (`X`) and target labels (`y`).
2. Split the data into training and testing sets.
3. Used 80% of the data for training and 20% for testing.
4. Applied stratified splitting to preserve class proportions.
5. Trained the Gaussian Naive Bayes model on the training data.
6. Predicted wine classes for the test data.
7. Evaluated performance using multiple classification metrics.

### Train-Test Split

| Subset | Samples |
|---|---:|
| Training Set | 142 |
| Testing Set | 36 |
| **Total** | **178** |

The random state was set to `42` to make the split reproducible.

## 📈 Model Evaluation

The model was evaluated using the following metrics:

- **Accuracy:** Measures the proportion of correct predictions.
- **Precision:** Measures how often predictions for a class are correct.
- **Recall:** Measures how many actual samples of a class are correctly identified.
- **F1-Score:** Combines precision and recall into a single metric.
- **Confusion Matrix:** Shows correct predictions and misclassifications for each class.

### Results

The Gaussian Naive Bayes model achieved the following results on the test set:

| Metric | Result |
|---|---:|
| Correct Predictions | 35 |
| Incorrect Predictions | 1 |
| Total Test Samples | 36 |
| **Test Accuracy** | **97.22%** |

### Confusion Matrix

The confusion matrix obtained from the test set was:

```text
[[12  0  0]
 [ 1 13  0]
 [ 0  0 10]]
```

**Interpretation:**

- **Class 1:** All 12 test samples were classified correctly.
- **Class 2:** 13 out of 14 test samples were classified correctly; one was misclassified as Class 1.
- **Class 3:** All 10 test samples were classified correctly.

The model correctly classified 35 out of 36 test samples, resulting in an accuracy of approximately 97.22%.

*Note: These results represent one train-test split. They do not guarantee the same performance on unseen datasets.*

## 🛠️ Technologies and Libraries

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical computing
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Scikit-learn** — Machine learning and model evaluation
- **Jupyter Notebook** — Interactive development environment

## 📁 Project Structure

```text
wine-dataset-classification/
│
├── wine-dataset-eda-naive-bayes.ipynb
├── wine.csv
└── README.md
```

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Ensure Python and Jupyter Notebook are installed.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. Place `wine.csv` in the expected location or update the CSV file path in the notebook.
5. Open the notebook:

   ```bash
   jupyter notebook wine-dataset-eda-naive-bayes.ipynb
   ```

6. Run the notebook cells sequentially to perform EDA, train the model, and evaluate its predictions.

## 📚 Key Learnings

Through this project, I practiced:

- Loading and inspecting a real-world dataset.
- Performing EDA and interpreting statistical summaries.
- Visualizing distributions, outliers, and feature correlations.
- Preparing data for supervised machine learning.
- Training and evaluating a multiclass classification model.
- Interpreting accuracy, precision, recall, F1-score, and confusion matrices.

## 🚀 Future Improvements

- Apply stratified k-fold cross-validation for more robust evaluation.
- Compare Gaussian Naive Bayes with other classification algorithms.
- Analyze feature importance and class-wise distributions in greater depth.
- Investigate model performance using additional evaluation metrics.

## 👩‍💻 Author

**Aqsa Batool**

Computer Science Student | Data Science and Machine Learning Enthusiast

---

*This project was developed for learning and practicing Exploratory Data Analysis and supervised machine learning using Python.*
