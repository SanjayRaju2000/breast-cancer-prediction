# Lung Cancer Mortality Prediction

---

## Executive Summary

Lung cancer is one of the most aggressive and deadly forms of cancer, with a high mortality rate worldwide.  
According to the **World Health Organization (WHO)**, lung cancer is responsible for approximately **1.8 million deaths every year**, making it the leading cause of cancer-related deaths globally.  

Identifying factors that influence lung cancer mortality is critical in healthcare — not only for early intervention, but also for tailoring treatment plans to improve patient survival outcomes. Understanding which clinical, demographic, and lifestyle features are most strongly associated with mortality can help medical professionals make better-informed decisions.

**Problem Space:**  
Patients diagnosed with lung cancer face varying prognoses. While some recover fully, others succumb despite treatment. The challenge lies in predicting patient outcomes based on available data at diagnosis and during treatment. This enables better risk stratification, targeted interventions, and improved allocation of healthcare resources.

**The Machine Learning Solution:**  
This project uses supervised machine learning models to predict whether a lung cancer patient is likely to recover or die, based on their demographic, lifestyle, and clinical features. The model outputs both predictions and interpretable feature importance, allowing for transparency in decision-making.

**Commercial Opportunity:**  
Such predictive tools could be integrated into hospital decision-support systems, enabling:
- Faster triage of high-risk patients.
- Prioritization of follow-up testing and imaging.
- Tailored patient monitoring programs.  
This could potentially improve survival rates while reducing treatment costs through better resource allocation.

---

## Data

**What the data shows:**  
The dataset contains records of patients diagnosed with lung cancer, including whether they recovered or died. Features include demographic details (age, gender), lifestyle factors (smoking history, alcohol consumption), environmental exposure (air pollution, dust allergy), and clinical indicators. The target variable is binary:  
- **0:** Patient recovered  
- **1:** Patient died  

**Source:**  
The dataset was obtained from **[Dataset Author’s Name]** and is hosted on **[Kaggle link or data repository]**. All data is anonymized and provided for research and educational purposes only.

---

## Methodology

### Data Cleaning
- Checked for and handled missing values (imputation for numerical features, mode replacement for categorical).
- Encoded categorical variables using label encoding and one-hot encoding where appropriate.
- Standardized or normalized numerical features to improve model convergence.
- Removed duplicates and verified data consistency.

### Exploratory Data Analysis (EDA)
- Summary statistics for all features.
- Class distribution analysis to check for imbalance in survival outcomes.
- Correlation analysis to identify relationships between features and the target variable.
- Visualization of key patterns:
  - Age distribution across recovery/death outcomes.
  - Mortality rates across smoking history categories.
  - Impact of environmental factors on survival.

---

### Modeling Approach
- **Baseline Model:** Logistic Regression to establish a performance benchmark. Decision Tree for any improvement. 
- **Advanced Models:** Random Forest, Gradient Boosting (XGBoost), and Support Vector Machines for performance improvement.
- **Model Selection:** Based on ROC-AUC, F1-score, recall, and precision.
- **Hyperparameter Tuning:** GridSearchCV for optimal performance.

---

### Evaluation Metrics
Given the high cost of false negatives in healthcare (predicting survival when death is likely), priority was given to:
- **Recall (Sensitivity)**
- **F1-score**
- **ROC-AUC**  
Confusion matrices were used to visualize classification performance.

---

### Model Interpretability
- **Feature Importance Analysis:** Identified top predictors of mortality.
- **SHAP Values:** Provided feature-level explanations for individual predictions.
- **Ethical Considerations:** Discussed potential biases in model predictions and the importance of human oversight in clinical use.

---

## Results Summary
> _(To be updated after model training)_  
- Best performing model: **XGBoost Classifier**
- ROC-AUC: **[Value]**
- F1-score: **[Value]**
- Top predictors of mortality: **[Feature 1]**, **[Feature 2]**, **[Feature 3]**

---

## Limitations
- Dataset size limits generalizability.
- Potential biases due to demographic or regional sampling.
- Model not suitable for direct clinical use — for research and educational purposes only.

---

## Future Work
- Incorporate time-to-event data for survival analysis.
- Test on larger, multi-center datasets.
- Integrate with external datasets (air quality, socio-economic indicators) for improved predictions.

---

## Acknowledgments
- Dataset by **[Author]**, sourced from **[Link]**.
- WHO statistics from [https://www.who.int/news-room/fact-sheets/detail/cancer](https://www.who.int/news-room/fact-sheets/detail/cancer).
