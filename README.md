#### English Version | [Kaggle competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

# House Prices - Advanced Regression Techniques

### Competition Description

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence. With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

### Goal
It is your job to predict the sales price for each house. For each Id in the test set, you must predict the value of the SalePrice variable.

### Approach

This project uses machine learning to predict house prices. The following steps were taken:

1. **Data exploration:**
   -  The training and testing datasets were loaded and thoroughly examined to understand the characteristics and other distributions. 
   -  By conducting correlation analysis, we identified key features that influence the sale price. These features were then visualized using histograms and scatter plots, providing a clearer picture of their impact.

2. **Feature Engineering:**
   - New features were developed to improve the model's prediction accuracy, including combining existing features and creating binary indicators for specific characteristics.

3. **Data Preprocessing:**
   - Missing values were handled by imputing them with appropriate strategies, such as filling with "None" for categorical features and 0 for numerical features.
   - Categorical features were encoded using One-Hot Encoding to transform them into numerical representations suitable for machine learning algorithms.

4. **Model Selection and Training:**
   - XGBRegressor and Ridge Regression were selected as the base models based on their performance and characteristics.
   - A Stacking Regressor model was chosen for its ability to combine the strengths of multiple base models.

5. **Model Evaluation:**
   - The trained model was evaluated using the Root Mean Squared Error (RMSE) and R-squared (R2) metrics.
   - A balance graph and a probability plot were generated to assess the model's residuals and ensure they followed a normal distribution.

6. **Prediction and Submission:**
   - The trained model was used to predict the SalePrice for the houses in the test dataset.
   - The predictions were then converted back to their original scale by applying the inverse of the logarithmic transformation.
   - The final predictions were saved into a submission file in the required format for submission to the Kaggle competition.

### Results

The developed model achieved a Kaggle score of **0.11996**, placing it within the **top 5%** of the leaderboard. RMSE:0.0577, R²: 0.979

### Files

- `House_Prices.ipynb`: Jupyter Notebook containing the complete code and analysis.
- `train.csv`: Training dataset.
- `test.csv`: Testing dataset.
- `data_description.txt`: Description of the features in the dataset.
- `submission.csv`: File containing the predictions for the test dataset.
- `png`: All graphs in the project.

### Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn 
- xgboost
- scipy

### Acknowledgements

This project was completed as part of a Kaggle competition. Thanks to Kaggle and the competition organizers for providing the dataset and platform.
