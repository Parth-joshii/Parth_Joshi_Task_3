# Housing Price Prediction using Linear Regression

## Project Overview
This project demonstrates a complete machine learning workflow for predicting housing prices based on various features. It uses a **multiple linear regression model** to analyze the relationship between house attributes (like area, number of bedrooms, and location) and their market price.

The entire analysis is contained within a single Python script designed to be run in a **Google Colab** environment.

---

## Dataset
The project uses the `Housing.csv` dataset, which contains **545 entries** with **13 different attributes** for each house, including:

- **price** (Target Variable)  
- area  
- bedrooms  
- bathrooms  
- stories  
- mainroad  
- guestroom  
- basement  
- hotwaterheating  
- airconditioning  
- parking  
- prefarea  
- furnishingstatus  

---

## Methodology
The project follows these key steps:

1. **Data Loading**: The `Housing.csv` file is uploaded and loaded into a pandas DataFrame.  

2. **Data Preprocessing**:  
   - Categorical features with 'yes'/'no' values are converted into a binary format (`1/0`).  
   - The `furnishingstatus` column is converted into numerical data using **one-hot encoding**.  

3. **Train-Test Split**: The dataset is split into **training (80%)** and **testing (20%)** sets to ensure the model can be evaluated on unseen data.  

4. **Model Training**: A **LinearRegression** model from the `scikit-learn` library is trained on the training data.  

5. **Model Evaluation**: The model's performance is assessed on the test set using three standard metrics:  
   - **Mean Absolute Error (MAE)**  
   - **Mean Squared Error (MSE)**  
   - **R-squared (R²)**  

---

## Results and Interpretation
The model achieved the following performance on the test data:

- **R-squared (R²): 0.65**  
  - This indicates that **65% of the variance** in house prices can be explained by the features included in the model.  

- **Feature Insights**:  
  - **Positive Impact**: Features like the number of bathrooms, airconditioning, and being in a preferred area (`prefarea`) have the strongest positive effects on price.  
  - **Negative Impact**: An unfurnished status is associated with the largest decrease in price compared to a furnished house.  

A regression plot is also generated to visually compare the **actual prices** against the **model's predictions**.

---

## Dependencies
This project requires the following Python libraries:

- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- google.colab (for file uploading in Colab environment)
