# Exploring-Auto-sklearn-with-Imbalanced-Class

This project utilizes **auto-sklearn**, an automated machine learning toolkit based on **scikit-learn**, to classify cast parts as **"Good"** or **"Bad"** based on temperature readings from multiple sensors during the casting process. The implementation tackles **class imbalance**, applies **feature engineering techniques**, and leverages **automated model selection and hyperparameter optimization** provided by auto-sklearn.

---

## 📌 Project Highlights

### 🔹 Data Preprocessing

#### Handling Missing Values and Outliers:
- Missing values were addressed using appropriate imputation techniques.
- Outliers in temperature readings were identified and handled using robust statistical methods such as **z-scores** and **Interquartile Range (IQR)**.

#### Exploratory Data Analysis (EDA):

##### Visualization and Outlier Detection:
- Outliers in temperature readings were visualized using **box plots** to understand their distribution and impact on the dataset.
- **Class label imbalance** was examined, and strategies like **Synthetic Minority Oversampling Technique (SMOTE)** were explored to mitigate imbalance.

---

### 🔹 Feature Engineering

#### Statistical Feature Extraction:
- Aggregated **statistical features** (e.g., `max`, `min`, `std`) were computed over sliding windows for temperature sensor data.
- This resulted in the generation of multiple **engineered features** to enrich the dataset.

#### Dimensionality Reduction:

##### Principal Component Analysis (PCA):
- **PCA** was employed to reduce the dimensionality of the dataset while retaining **99%** of the variance.
- This step helped in simplifying the model without losing critical information from the original features.

---

### 🔹 Model Training & Evaluation

#### Auto-sklearn Integration:
- **Automated model selection** and **hyperparameter tuning** were performed using **auto-sklearn** to optimize the classification pipeline.
- Model performance was evaluated using **robust cross-validation techniques**, focusing on metrics such as **F1-score** to account for class imbalance.

---

## 📊 Results

### Performance Metrics:
- The **initial base model performance** was benchmarked.
- Through iterative experimentation and **auto-sklearn's capabilities**, significant improvements in **F1-score** were achieved, demonstrating the effectiveness of the approach.

---


## Requirements

The project relies on the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy`
- `imblearn`
- `scikit-learn`
- `scikit-learn-intelex` (for Intel optimizations)
- `auto-sklearn`

To install all requirements, run:
```bash
pip install -r requirements.txt
```

---

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Exploring-Auto-sklearn-with-Imbalanced-Class.git
    cd Exploring-Auto-sklearn-with-Imbalanced-Class
    ```

2. Open Notebook `Classifying casting parts in detail.ipynb` and execute the cells
    

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contribution
Feel free to contribute by submitting pull requests or reporting issues. For questions or suggestions, contact the repository maintainer.
