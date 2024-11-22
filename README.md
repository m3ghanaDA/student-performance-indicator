# Predicting Student Performance Using Machine Learning

## 1. Problem Definition

### Objective
The primary aim of this project was to analyze and predict student performance based on demographic and socioeconomic factors. Specifically, the study addressed:

- How demographic factors (e.g., gender, ethnicity) and socioeconomic indicators (e.g., parental education, lunch type) influence student test scores.
- The impact of participation in a test preparation course on performance.
- Using machine learning models to predict student scores based on these factors.

### Dataset
The dataset was sourced from Kaggle and includes 1,000 records with eight attributes related to student demographics and test scores.

---

## 2. Data Collection

### Features
- **Categorical Variables**: Gender, Ethnicity, Parental Level of Education, Lunch Type, Test Preparation Course.
- **Numerical Variables**: Math Score, Reading Score, Writing Score.

### Tools
Data manipulation and visualization were performed using:
- **Python Libraries**: Pandas, NumPy, Matplotlib, Seaborn.

---

## 3. Data Preprocessing and Cleaning

### Steps
1. **Data Validation**: Ensured no missing or duplicate entries.
2. **Data Type Verification**: Verified correct data types for numerical and categorical features.
3. **Feature Engineering**: Added:
   - **Total Score**: Sum of Math, Reading, and Writing scores.
   - **Average Score**: Mean of Math, Reading, and Writing scores for overall academic performance.

---

## 4. Exploratory Data Analysis (EDA)

### Insights
- **Gender**: Female students scored higher in reading and writing; male students excelled in math.
- **Parental Education**: Higher parental education levels correlated with better scores.
- **Lunch Type**: Students with standard lunches outperformed those with free/reduced lunch.
- **Test Preparation**: Completing a test preparation course improved scores across all subjects.

### Visualizations
- Distribution plots for scores across subjects.
- Box plots and scatter plots to analyze relationships between features.

---

## 5. Feature Engineering and Data Transformation

### Processing Steps
- **Encoding**: One-Hot Encoding for categorical features.
- **Standardization**: Applied StandardScaler to normalize numerical features.
- **Data Splitting**: Divided data into training (80%) and testing (20%) sets.

---

## 6. Model Selection and Training

### Models Evaluated
- **Linear Regression**
- **Ridge and Lasso Regression**
- **K-Neighbors Regressor**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **CatBoost Regressor**
- **AdaBoost Regressor**

Each model was trained and evaluated using metrics such as:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

---

## 7. Model Evaluation and Comparison

### Findings
- **Top Performers**: Ridge Regression and Linear Regression achieved an R² score of 88%.
- **Ensemble Models**: Random Forest and CatBoost performed well but required higher computational resources.
- **Residual Analysis**: Scatter plots showed minimal deviations for the Linear Regression model, confirming its reliability.

---

## 8. Insights and Conclusions

### Key Takeaways
- **Socioeconomic Factors**: Parental education and lunch type significantly impacted scores.
- **Gender Trends**: Female students excelled in reading and writing; male students in math.
- **Test Preparation**: Courses positively influenced performance across all subjects.

This study demonstrated the efficacy of machine learning in predicting student scores based on demographic and socioeconomic factors.

---

## 9. Future Improvements and Applications

### Next Steps
- **Hyperparameter Tuning**: Fine-tune top models for better accuracy.
- **Feature Expansion**: Include factors like study hours or school quality.
- **Broader Applications**: Adapt the model to identify at-risk students or tailor educational interventions.

---

## 10. Code Structure and Management

### Modular Design
- **Components**:
  - `data_ingestion.py`: Handles data loading and preprocessing.
  - `data_transformation.py`: Performs feature engineering and transformations.
  - `model_trainer.py`: Trains and evaluates models.

- **Pipelines**:
  - `train_pipeline.py`: Orchestrates training workflows.
  - `predict_pipeline.py`: Manages predictions on new data.

### Dependency Management
- `setup.py`: Defines the project as an installable package.
- `requirements.txt`: Lists all dependencies for easy setup.

### Logging and Exception Handling
- `logger.py`: Tracks execution for debugging.
- `exception.py`: Manages custom exceptions for robustness.

---

## 11. Deployment

### Deployment Steps
- **Flask Web Application**: Built a web app for user interaction and model predictions.
- **AWS Deployment**: Hosted on AWS Elastic Beanstalk with CI/CD pipelines.
- **Dockerization**: Created a Docker image encapsulating the app and dependencies.

---

## 12. CI/CD Pipeline Configuration

A Continuous Integration and Deployment pipeline was established using:
- **GitHub Actions**: For version control and integration.
- **AWS CodePipeline**: For seamless deployments.

---

## Conclusion
This project showcases the potential of machine learning in educational analytics, offering actionable insights into student performance and its influencing factors. With further refinements, this approach can serve as a valuable tool for educators and policymakers.
