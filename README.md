# Heart-Disease-Dataset-UCI
Logistic Regression + Outlier Removal + Variance Inflation Factor 

### Methodology:

1. **Loading the Dataset**:
   We began by loading the Heart Disease UCI dataset into a Pandas DataFrame. We explored the data, identified 14 columns with both numerical and categorical features, and checked for missing values. No missing data was found.

   - **Key features**: `age`, `cholesterol`, `resting_blood_pressure`, `thalassemia`, etc.
   - **Target**: Binary variable (`0` for no heart disease, `1` for heart disease).

2. **Initial Data Analysis**:
   Using `df.describe()`, we explored basic statistics like mean, standard deviation, and min/max values for numerical columns. We also reviewed categorical values using `df.unique()` to understand the distribution across these features.

   - **Example**: The mean age of patients was approximately 54, and cholesterol levels had a wide range, from 126 to 564 mg/dl.

3. **Correlation and Outlier Detection**:
   We calculated the correlation matrix to explore relationships between features. Variables like `Max_heart_rate` and `oldpeak` showed relatively strong correlations with the `target` (heart disease).

   We also performed outlier detection, identifying and removing 72 outliers across several columns (e.g., `cholesterol`, `resting_blood_pressure`).

   - **Result**: Outliers removed; dataset reduced to 946 rows.

4. **Label Encoding and Feature Scaling**:
   Categorical features such as `sex`, `chest_pain_type`, and `thalassemia` were label-encoded to convert them into numerical values. Non-categorical features were normalized to ensure all values were on a similar scale, essential for model training.

5. **Model Selection**: 
   We used **Logistic Regression** for this binary classification task, aiming to predict whether a patient had heart disease (target = 1) based on the features. The dataset was split into training and test sets (80/20 split).

6. **Model Training and Evaluation**:
   The logistic regression model was trained, and we evaluated it on the test set. 

   - **Accuracy**: **84.7%**
   - **Precision, Recall, F1-Score**: 
     - For **Class 0** (no heart disease):
       - Precision: **88%**
       - Recall: **81%**
       - F1-Score: **84%**
     - For **Class 1** (heart disease):
       - Precision: **82%**
       - Recall: **88%**
       - F1-Score: **85%**

   - **Confusion Matrix**: 
     - **Class 0 (No Heart Disease)**: 79 true negatives, 18 false positives.
     - **Class 1 (Heart Disease)**: 82 true positives, 11 false negatives.

7. **Decision Boundary**: 
   To visualize the model’s decision-making process, we plotted a decision boundary between two key features: `age` and `cholesterol`. This gave us insight into how the model classifies patients based on these features.

   - **Visual Result**: ![Alt text](relative/path/to/2.png)

  

