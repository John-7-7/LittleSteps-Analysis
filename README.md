# LittleSteps-Analysis
This project analyses nurse scheduling and patient visit efficiency for LittleSteps, an at-home healthcare startup. The analysis focuses on understanding patterns in patient visit duration and identifying areas for improvement. This project was approached by using python libraries like numpy for data generation, pandas for data cleaning and visualisation. The process goes by first generating a CSV(visits.csv) file with 600 entries in accordance with the requirement. Next, the visits.csv is then cleaned to give visits_cleaned.csv. Finally, using matplotlib tools, I extract key insights by visualising the data in various representations. 

\## Repository Structure

Littlesteps-Analysis/
│── data/ # Raw and cleaned data files
│   ├── visits.csv
│   ├── visits_cleaned.csv
│
│── notebooks/ # Jupyter notebooks for data generation, cleaning and analysis
│   ├── 01_data_generation.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_analysis_visualisation.ipynb
│
│── requirements.txt
│── README.md # Project documentation

\## Setup Instructions
git clone https://github.com/yourusername/LittleSteps-Analysis.git
cd LittleSteps-Analysis

bash

pip install -r requirements.txt

bash
\# Generate dataset (Run this notebook first)
jupyter notebook notebooks/data_generation.ipynb

\# Cleaning the dataset (Run this notebook next)
jupyter notebook notebooks/data_cleaning.ipynb

\# Run analysis and generate visualisations (Run this notebook last)
jupyter notebook notebooks/analysis_visualisation.ipynb

1\. Visit Duration Patterns

Average visit duration: ~3439 minutes

Significant variation across service types

The service type with the longest average duration is Wound Care with average duration of 4950 minutes (3s.f.) while the service with shortest duration is Physical Therapy with average duration of 1560 minutes (3s.f.).

2\. Geographical Variations

Visit durations show some variation across locations

Statistical testing reveals significant differences

3\. Nurse Performance

The top three nurses that have the shortest visit_duration are N14, N05, N13 with average duration of 78.2, 94.8 and 96.1 minutes (3s.f.) respectively. The top three nurses that have the longest visit_duration are N01, N03, N17 with average duration of 7270, 7420 and 7790 minutes (3s.f.), respectively.


Data Cleaning Approach:

Handling Missing Values

Formatted the time and sorted by start time

Inconsistent datetime formats standardised

Removed duplicate records

Nurse notes: Filled with "Nil" and replaced those with "lorem ipsum" to "Nil"

Justification: Preserves data volume while maintaining integrity

Categorical variables cleaned and standardised

Text data processed for keyword extraction

Created a new CSV file named "visits_cleaned.csv"


Visualisations:

The analysis includes comprehensive visualisations:

Distribution of visit durations in full

Distribution of visit durations (0 - 1000 minutes)

Distribution of visit durations by Service Type

Distribution of visit durations by Location Zone

Boxplot of Visit Duration by Location (0 - 1000 minutes)

Boxplot of Visit Duration by Service Type

Nurse performance metrics

Distribution of Service Type (Pie)


Assumptions and Limitations:

Assumptions

Synthetic data realistically simulates real-world patterns

5-minute minimum visit duration is reasonable

Nurse notes keywords provide meaningful insights

Limitations

Synthetic data may not capture all real-world complexities

Visit duration outliers could have legitimate explanations

Text analysis is basic; NLP could provide deeper insights


Recommendations:

Resource Optimisation for certain zones, such as East, since there is a higher average visit durations

Allocate more time for Physical Therapy visits

Share best practices from top-performing nurses

Investigate reasons for longer durations in specific locations

Implement better data collection practices

Develop standardised note-taking templates to ensure consistency

Regular review of visit duration patterns

Develop predictive models for visit duration

Real-time monitoring and alerting system


Challenges:

Capturing all the possible cases of errors for standardisation

Identifying the right range of outliers for removal

Resizing and fitting all the plots in the diagram


Contact:

For questions about this analysis, please contact me.








