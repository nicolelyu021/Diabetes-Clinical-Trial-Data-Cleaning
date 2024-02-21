# Diabetes Clinical Trial Data Cleaning Project

## Project Overview

This project aimed to clean a GPT-generated dataset of diabetes clinical trials to ensure data quality and integrity for further analysis. The dataset contained various details about the trials, including participant demographics, trial groups, smoking status, and outcomes.

## Dataset Description

The dataset included entries on clinical trials related to diabetes, with features such as sex, trial group, smoking status, and other trial-specific metrics. This GPT-generated dataset required thorough cleaning to address inconsistencies, missing values, and to standardize its format.

## Objectives

- Correct inconsistencies in categorical data.
- Implement feature engineering for better data representation.
- Handle missing data effectively to maintain dataset integrity.

## Tools and Technologies Used

- Python programming language for scripting the data cleaning process.
- Pandas library for data manipulation and analysis.

## Data Cleaning Steps

### Standardize Categorical Data

#### Handle Inconsistencies

1. **Standardization of Sex Column**: The 'Sex' column contained values 'Female' and 'Male', which were standardized to 'F' and 'M', respectively, to maintain consistency.
2. **Removal of Condition Column**: The 'Condition' column was deemed unnecessary for the analysis and was removed from the dataset.

#### Feature Engineering

- **Methodology Choice**: Discussed the appropriateness of Label Encoding, One-Hot Encoding, and Frequency Encoding for different types of data within the dataset. One-Hot Encoding was applied to the 'Sex', 'Trial Group', and 'Smoking Status' columns, with the first dummy variable dropped for each to avoid multicollinearity.

### Deal with Missing Data

- Missing data was quantified both as counts and percentages to identify the extent of missingness in each column. This step was crucial for deciding on further actions, such as imputation or removal, depending on the significance of the missing data to the overall analysis.

## Challenges and Solutions

- **Challenge: Handling Missing Data**: The primary challenge involved missing biomarker data and outliers in drug doses. Addressing these issues was critical due to their significance in clinical trial analysis.
- **Solution**: Performed an initial assessment to quantify missingness. Applying domain knowledge, outliers in durg doses were replaced with NaN. Then imputed with median (considering a skewed distribution). KNN was used to fill in the small number of missing biomarkers. 

## Key Findings and Results

- The cleaning process standardized the dataset, making it more suitable for analysis and modeling.
- Identified the need for further detailed strategies to handle missing data, which will enhance the dataset's reliability and utility.

## Future Work

- Explore and implement imputation methods for missing data based on the nature of each column.
- Further analysis to uncover insights specifically related to diabetes clinical trials.
- Use the cleaned dataset to build predictive models regarding trial outcomes.

## Conclusion

The data cleaning process applied to the GPT-generated diabetes clinical trial dataset has significantly improved its quality, making it a valuable resource for future research and analysis. This project underscored the importance of meticulous data cleaning and preparation in the data science workflow.
