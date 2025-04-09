 Milk Quality Prediction using Decision Tree Classifier

This project implements a machine learning model using a Decision Tree Classifier to predict the quality grade of milk based on various physicochemical attributes. It includes preprocessing, outlier detection, model training, evaluation, and result visualization.

 Project Objective

To build an interpretable and accurate machine learning model that classifies milk samples into categories like **Low**, **Medium**, and **High** quality using features such as pH, temperature, fat content, and more.

 Dataset Description

The dataset contains several key indicators of milk quality. After cleaning and outlier treatment, it was used to train and evaluate the classification model.

 Features:

| Feature      | Description                        |
|--------------|------------------------------------|
| pH           | Acidity level of milk              |
| Temperature  | Temperature of milk                |
| Taste        | Taste evaluation score             |
| Odor         | Odor evaluation score              |
| Fat          | Fat content                        |
| Turbidity    | Milk turbidity level               |
| Colour       | Visual assessment of color         |
| Grade        | Target variable (Low, Medium, High)|

---

 Data Preprocessing

- **Outlier Detection:** IQR method
- **Outlier Handling:**
  - `pH`, `Temperature`: Replaced outliers with **median**
  - `Colour`: Replaced outliers with **mode**
- **Encoding:** Label Encoding used to convert `Grade` into numerical values
   Model Overview

- **Algorithm:** Decision Tree Classifier
- **Library Used:** `scikit-learn`
- **Data Split:** 80% training, 20% testing

 Model Steps:
1. Load and clean data
2. Handle outliers
3. Encode target labels
4. Train Decision Tree model
5. Predict and evaluate test data

 Evaluation Metrics

- **Accuracy Score**
- **Classification Report** (Precision, Recall, F1-Score)
- **Confusion Matrix**
- **Sample Test Results** (as a DataFrame)



 Visualizations

- Bar chart of `Grade` distribution
- Confusion matrix heatmap
- Optional: Decision tree plot
 Output Files

| File                            | Description                                |
|---------------------------------|--------------------------------------------|
| `milk_cleaned.csv`              | Dataset after outlier handling             |
| `milk_encoded_test_results.csv` | Predicted vs Actual test results           |
| `confusion_matrix.png`          | Visualization of prediction results        |
| `project.ipynb`                 | Full notebook with all implementation steps|

 Requirements

```bash
pip install pandas scikit-learn matplotlib seaborn

### folder structure
milk-quality-classifier/
│
├── milk_cleaned.csv
├── milk_encoded_test_results.csv
├── confusion_matrix.png
├── project.ipynb
└── README.md
