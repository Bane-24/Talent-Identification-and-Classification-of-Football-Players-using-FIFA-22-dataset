# Talent Identification and Playing Position Classification of Football Players

---

## Project Overview

This project aims to classify football players into their best-suited playing positions using machine learning models based on FIFA 22 player data. 
The key motivation is to identify young football talent and optimize their performance by aligning their skills with the appropriate playing positions.

---

## Business Problem

The project addresses two critical challenges in football talent management:  
1. **Player Development**: Identifying players whose skillsets need to be developed for their current positions.  
2. **Role Realignment**: Identifying players who are playing in positions misaligned with their skillsets and suggesting better-suited positions.

---

## Stakeholders

- **Footballers**: Benefit from improved guidance in their careers.  
- **Football Clubs**: Enhance team performance by optimizing player roles.  
- **Talent Scouts**: Augment scouting decisions with data-driven insights.

---

## Machine Learning Goal

1. **4-Class Classification**:
   - Classify players into Attacker, Midfielder, Defender, or Goalkeeper categories.  
2. **27-Class Classification**:
   - Fine-grained classification into specific positions like Striker (ST), Central Midfielder (CM), Right Back (RB), etc.

---

## Methodology

### Dataset Description

- **Source**: Kaggle  
- **Name**: FIFA 22 Complete Player Dataset  
- **Size**: 19,239 rows and 110 columns  
- **Attributes**: Player ratings, attributes, positions, wages, and more.

### Feature Engineering

1. **Dropped Features**: Removed 52 irrelevant features (e.g., weblinks, photos, etc.).
2. **Created Features**:  
   - **Main Position**: Grouped into 4 classes (Attacker, Midfielder, Defender, Goalkeeper).  
   - **Club Position**: Expanded into 27 specific positions.  
3. **Missing Values**:  
   - Deleted features with >70% missing values (e.g., Goal Keeping Speed).  
   - Imputed missing values for skill attributes using median values of similar players.  
4. **Encoded Features**:  
   - Binary encoding for `preferred_foot`.  
   - Multi-class encoding for positions.

### Exploratory Data Analysis (EDA)

- **Correlation Heatmap**: Highlighted relationships between attributes.  
- **Insights**:
  - Players with higher overall ratings tend to have higher wages.  
  - No clear relationship between age and overall rating.  
- **Visualization**: Used pair plots to explore data distributions.

### Models Used

1. Logistic Regression  
2. Support Vector Machine (SVM)  
3. Decision Tree  
4. Random Forest  
5. Neural Network  
6. XGBoost  

- **Train-Test Split**: 80/20 split, stratified by position.  
- **Hyperparameter Tuning**: Conducted for XGBoost to improve performance.

---

## Results

### 4-Class Classification (Attacker, Midfielder, Defender, Goalkeeper)
- **Best Model**: XGBoost (after tuning).  
- **Accuracy**: 0.91 (XGBoost), 0.90 (SVM).

### 27-Class Classification (Fine-Grained Positions)
- **Best Model**: Logistic Regression.  
- **Accuracy**: 0.59.

---

## Key Achievements

1. Developed robust classification models for both 4-class and 27-class position categories.
2. Achieved high accuracy (91%) for broad position classification using XGBoost.  
3. Provided actionable insights for talent identification and role optimization.

---

## Limitations

1. **Incomplete Hyperparameter Tuning**: Due to computational constraints, full tuning wasn't possible.  
2. **Data Scope**: Models rely on FIFA skill scores, not real-world performance metrics (e.g., speed, strength).  
3. **Data Imbalance**: Some positions had fewer samples, potentially affecting accuracy.  

---

## Future Work

1. Extend the model to include real-world performance metrics such as running speed, passes, and strength.  
2. Focus on young, emerging players at grassroots levels for better talent scouting.  
3. Improve model accuracy with advanced imbalanced data techniques.

---

## Ethical Implications

1. Data is publicly available from Kaggle; no privacy concerns.  
2. Player identities could be anonymized to enhance ethical compliance.  
3. Models are designed to assist talent scouts and coaches, not replace them.

---

## Conclusion

This project successfully developed machine learning models to classify football players into optimal positions, providing valuable tools for clubs, players, and scouts. Future enhancements will focus on incorporating real-world performance data and improving accuracy for finer position classifications.

