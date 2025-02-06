## Covid-19 Data Analysis and Prediction
This project aims to analyze Covid-19 data, visualize key trends, and develop predictive models to estimate Covid-19 deaths based on gender, age, and location.


### Deaths involving COVID-19, pneumonia, and influenza reported to NCHS by sex, age group, and jurisdiction of occurrence.
Last Updated
September 27, 202

data was collected between 2020-01-01 and 2023-09-23
#### In this project, we will dive deep into the data related to COVID-19 deaths and try to explain and predict the most vulnerable groups of people that might be affected by this virus.

### Contributing
Data Analysis: Cleaning, processing, and analyzing Covid-19 data.
Visualization: Using plots to understand trends and relationships.
Model: Tunned XGBoost

### Technologies Used

Python
Libraries:
  * numpy (Numerical computations)
  * pandas (Data manipulation)
  * matplotlib & seaborn (Visualization)
  * sklearn (Machine learning for predictions)

Dataset
The project uses a Covid-19 dataset containing information about cases, deaths, gender, age, and location.

### Features
* data_as_of - Date of Analysis (2023-09-27)	 - Floating Timestamp 
* start_date - First date of data period - Floating Timestamp
* end_date - Last date of data period - Floating Timestamp
* group - Indicator of whether data measured by Month, by Year, or Total - Text
* year - Year in which death occurred - Number
* month - Month in which death occurred - Number
* state - Jurisdiction of occurrence - Text
* sex - Sex - Text
* age_group - Age group - Text
* covid_19_deaths - Deaths involving COVID-19 (ICD-code U07.1) - Number
* total_deaths - Deaths from all causes of death - Number
* pneumonia_deaths - Pneumonia Deaths (ICD-10 codes J12.0-J18.9) - Number
* pneumonia_and_covid_19_deaths - Deaths with Pneumonia and COVID-19 (ICD-10 codes J12.0-J18.9 and U07.1) - Number
* influenza_deaths - Influenza Deaths (ICD-10 codes J09-J11) - Number
* pneumonia_influenza_or_covid - Deaths with Pneumonia, Influenza, or COVID-19 - Number
* footnote - Suppressed counts (1-9) - Text)	footnote	Text
)	footnote	Text



### Conclusions

* Age Group Distribution: The most frequent age group in the dataset is 60 years old, while the least frequent is 50 years old.
* Outliers: The dataset contains several outliers, especially on the right side of the whisker, likely due to COVID surges, so they are considered valid and not removed.
* Gender Distribution: Male records are 3.4% higher than female records in the dataset.
* Death Patterns: COVID-19 deaths follow similar patterns to pneumonia deaths, with a notable increase in deaths as age rises, particularly for individuals aged 60 and above.
* Geographic Distribution: States like California, Texas, and Florida have the highest number of COVID deaths, while Wyoming, Vermont, Alaska, and North Dakota report the lowest.
* Model Performance: The tuned XGBoost model showed significant improvement with an R² of 0.85, offering decent performance on unseen data, outperforming previous models like Decision Trees and Linear Regression.
* Feature Importance: State-based features dominate the importance rankings, while age group, which was expected to be a significant predictor, is relatively less influential.
