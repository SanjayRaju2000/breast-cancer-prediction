# Breast Cancer Prediction

## Executive Summary  

Breast cancer is one of the most common cancers worldwide and a leading cause of cancer-related deaths among women.  
According to the **World Health Organization (WHO)**, breast cancer accounts for approximately **685,000 deaths each year**. Early detection and accurate diagnosis are critical in improving survival rates and treatment outcomes.  

The central challenge lies in distinguishing between **benign** (non-cancerous) and **malignant** (cancerous) tumors based on measurable attributes of the tumor. Reliable classification can assist medical professionals in decision-making, reduce unnecessary interventions, and prioritize high-risk cases.  

**Problem Space:**  
Given numeric measurements of breast tumor samples, can we accurately classify whether a tumor is benign or malignant?  

**The Machine Learning Solution:**  
This project applies supervised machine learning models to classify tumors. By training on tumor characteristics (such as mean radius, texture, perimeter, area, and other derived features), the model predicts whether a given sample is malignant or benign. Feature importance and interpretability methods are also applied to ensure transparency in the decision-making process.  

**Commercial Opportunity:**  
Predictive models of this type could be integrated into **decision-support systems** for radiologists and oncologists, helping to:  
- Assist in early diagnosis.  
- Reduce diagnostic errors.  
- Improve patient outcomes by enabling timely intervention.  

---

## Data  

**What the data shows:**  
The dataset consists of **numeric measurements of breast tumor cells**, extracted from medical imaging. Each record corresponds to a tumor, with features describing its physical properties. The target variable is binary:  
- **0:** Benign tumor  
- **1:** Malignant tumor  

**Source:**  
The dataset used is the **Breast Cancer Wisconsin (Diagnostic) dataset**, widely available for research and educational purposes, hosted on [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data).  

---

## Methodology  

### Data Cleaning  
- Verified dataset integrity (no null values or duplicates).  
- Confirmed numerical feature consistency and ranges.  
- Standardized features for optimal model performance.  

### Exploratory Data Analysis (EDA)  
- Examined class distribution (benign vs malignant).  
- Analyzed distributions of key numerical features.  
- Explored correlations between features and the target.  
- Visualized patterns in tumor characteristics (e.g., size, texture).  

### Modeling Approach  
- **Baseline Models:** Logistic Regression, Decision Tree.  
- **Advanced Models:** Random Forest, Gradient Boosting (XGBoost), Support Vector Machines.  
- **Model Selection:** Based on ROC-AUC, F1-score, precision, and recall.  
- **Hyperparameter Tuning:** GridSearchCV for optimization.  

### Evaluation Metrics  
Given the high cost of false negatives in cancer detection (classifying malignant as benign), the following metrics are prioritized:  
- **Recall (Sensitivity)**  
- **F1-score**  
- **ROC-AUC**  
Confusion matrices are used to visualize performance.  

### Model Interpretability  
- **Feature Importance Analysis:** Identified top predictors of malignancy.  
- **SHAP Values:** Provided feature-level explanations for predictions.  
- **Ethical Considerations:** Highlighted importance of human oversight.  

---

## Results Summary  
> _(To be updated after model training)_  
- Best performing model: **[Model]**  
- ROC-AUC: **[Value]**  
- F1-score: **[Value]**  
- Top predictors of malignancy: **[Feature 1]**, **[Feature 2]**, **[Feature 3]**  

---

## Limitations  
- Dataset size and scope limit generalizability.  
- Synthetic balance in classes may not fully represent real-world scenarios.  
- For educational purposes only — **not suitable for clinical deployment**.  

---

## Future Work  
- Explore deep learning approaches (e.g., neural networks).  
- Apply survival analysis on longitudinal breast cancer datasets.  
- Validate on larger, real-world, multi-center datasets.  

---

## Acknowledgments  
- Dataset by **UCI Machine Learning Repository**, available via Kaggle.  
- WHO statistics from [https://www.who.int/news-room/fact-sheets/detail/cancer](https://www.who.int/news-room/fact-sheets/detail/cancer).  

---

## Note on Project History  
This repository originally began as a **lung cancer mortality prediction project**, which explored demographic, lifestyle, and clinical features. During exploratory data analysis, it was determined that the dataset was **synthetic and lacked predictive signal**. Those initial notebooks have been moved to the `archive/` folder for transparency but are not part of the final analysis. The project has since pivoted to focus on **breast cancer tumor classification**, which provides a stronger foundation for demonstrating machine learning workflows.  
