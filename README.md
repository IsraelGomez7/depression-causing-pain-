# Depression Analysis using Actigraphy Data


## Project Overview

This project analyzes patterns in sleep and daily motor activity to understand the differences between individuals with depression and non-depressed individuals. Using actigraphy data from the [Depression Dataset on Kaggle](
https://www.kaggle.com/datasets/arashnic/the-depression-dataset), the analysis aims to identify significant variations in motor activity levels and sleep durations associated with different depressive states.

The main objectives of this project are:
1. **Sleep Pattern Analysis**: Compare sleep duration and activity levels between individuals with depressive symptoms and healthy controls.
2. **Machine Learning Classification**: Develop and evaluate models to predict depressive states using activity metrics.
3. **Feature Engineering**: Extract meaningful features from timestamped actigraphy data to enhance model accuracy.

## Dataset Description

The dataset comprises two main folders:
- **Control Group**: CSV files for non-depressed individuals.
- **Condition Group**: CSV files for individuals diagnosed with depression.

Each file contains actigraphy data collected at one-minute intervals, featuring the following columns:
- **Timestamp**: Time of the activity measurement.
- **Date**: Date of the recording.
- **Activity**: Actigraph watch activity measurements.

Additionally, the `scores.csv` file contains information on each participant's MADRS (Montgomery-Åsberg Depression Rating Scale) score, as well as demographic and clinical data such as:
- **Age Group**, **Gender**, **Education Level**
- **Depression Type** (e.g., Unipolar Depressive, Bipolar I or II)
- **MADRS Scores** at the beginning and end of the measurement period.

## Analysis and Results

### Data Preprocessing
- **Cleaning**: Removed duplicates and converted timestamps to datetime format.
- **Aggregation**: Daily total activity and average activity levels were calculated per participant to facilitate analysis.
  
### Exploratory Data Analysis (EDA)
1. **Daily Activity Patterns**: Examined total daily activity across groups to detect differences.
2. **Sleep Duration Comparison**: Measured and compared total sleep duration between participants with and without depressive symptoms.
3. **Statistical Testing**: Used statistical methods to validate observed differences between the control and condition groups.

### Machine Learning Classification
- **Random Forest Classifier**: Used to classify participants based on their average daily activity levels and demographic data.
- **Results**: The classifier achieved an accuracy of 82% with a precision of 80% for the control group, indicating potential predictive capability.

## Key Findings

- **Reduced Activity in Depressed Individuals**: Depressed participants showed lower average daily activity levels than controls, especially among those with Unipolar Depression.
- **Variation in Sleep Patterns**: Depressed individuals exhibited increased sleep duration variability compared to non-depressed participants.

## Tools and Libraries Used

- **Programming Language**: Python
- **Data Analysis and Visualization**: Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn, Random Forest Classifier
- **Platform**: Kaggle Notebooks

## Future Work

1. **Feature Engineering**: Explore additional features, such as sleep onset and wake time consistency.
2. **Model Improvement**: Experiment with deep learning models, like Convolutional and Recurrent Neural Networks, for time-series classification.
3. **Enhanced Sleep Analysis**: Examine correlations between sleep patterns and specific depressive symptoms.
