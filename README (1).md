# Vaccine Prediction Project

## Overview

The goal of this project is to predict the likelihood of individuals receiving the XYZ and seasonal flu vaccines based on their demographic, behavioral, and opinion features. This is a multi-label classification problem, where the two target variables are:
- `xyz_vaccine`: Whether the respondent received the XYZ flu vaccine.
- `seasonal_vaccine`: Whether the respondent received the seasonal flu vaccine.

## Dataset

The dataset consists of 36 columns, where the first column `respondent_id` is a unique identifier, and the remaining 35 columns are features related to the respondents' demographic, behavioral, and opinion attributes.

### Features

- **xyz_concern**: Level of concern about the XYZ flu.
- **xyz_knowledge**: Level of knowledge about XYZ flu.
- **behavioral_*_**: Various behavioral features (e.g., `behavioral_avoidance`, `behavioral_face_mask`).
- **doctor_recc_*_**: Whether a doctor recommended the XYZ or seasonal flu vaccine.
- **chronic_med_condition**: Whether the respondent has a chronic medical condition.
- **child_under_6_months**: Whether the respondent has close contact with a child under six months.
- **health_worker**: Whether the respondent is a healthcare worker.
- **health_insurance**: Whether the respondent has health insurance.
- **opinion_*_**: Various opinion features (e.g., `opinion_xyz_vacc_effective`, `opinion_seas_risk`).
- **age_group**: Age group of the respondent.
- **education**: Education level of the respondent.
- **race**: Race of the respondent.
- **sex**: Sex of the respondent.
- **income_poverty**: Household annual income relative to the 2008 Census poverty thresholds.
- **marital_status**: Marital status of the respondent.
- **rent_or_own**: Housing situation of the respondent.
- **employment_status**: Employment status of the respondent.
- **hhs_geo_region**: Geographic region of residence as defined by the U.S. Dept. of Health and Human Services.
- **census_msa**: Residence within metropolitan statistical areas (MSA) as defined by the U.S. Census.
- **household_adults**: Number of other adults in the household.
- **household_children**: Number of children in the household.
- **employment_industry**: Industry of employment.
- **employment_occupation**: Occupation of the respondent.

## Model

The model used is a RandomForestClassifier wrapped in a MultiOutputClassifier to handle the multi-label classification problem. The data is preprocessed using pipelines for numerical and categorical features, including imputation and scaling/encoding.

## Files

- `training_set_features.csv`: Training data features.
- `training_set_labels.csv`: Training data labels.
- `test_set_features.csv`: Test data features.
- `vaccine_predictions.csv`: Predicted probabilities for the test set.


