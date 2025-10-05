# Insight_Navigators
United Airlines Flight Difficulty Score
1. Project Objective
The goal of this project is to develop a data-driven Flight Difficulty Score to systematically quantify the relative operational complexity of each flight departing from Chicago O'Hare International Airport (ORD). This score replaces manual, experience-based assessments with a consistent, scalable, and predictive system to enable proactive resource planning.

2. Prerequisites & Setup
This project is written in Python 3. Before running the scripts, you must install the necessary libraries.

Open your terminal or command prompt and run the following command:

Bash

pip install pandas matplotlib seaborn lightgbm xgboost catboost scikit-learn
3. How to Run the Project
To generate all the results from start to finish, place all the Python scripts and the five raw data CSV files (Flight Level Data.csv, PNR+Flight+Level+Data.csv, etc.) in the same folder.

Then, run the scripts in the following numerical order:

1_merge_and_clean.py: This script merges the 5 raw data files, performs essential cleaning (like fixing impossible ground times), and creates the master dataset for analysis.

2_exploratory_data_analysis.py: This script loads the cleaned data, calculates the answers to the 5 key EDA questions, and generates several summary plots.

3_build_difficulty_score.py: This is the main modeling script. It engineers features, trains all 4 machine learning models, generates the difficulty scores and daily ranks, and creates the final submission CSV.

4_post_analysis_insights.py: This script loads the final scored results and generates the analysis needed for the operational recommendations (e.g., top difficult destinations, common drivers).

4. File Descriptions
Python Scripts (.py)
1_merge_and_clean.py: Input: 5 raw CSV files. Output: master_flight_data_cleaned.csv.

2_exploratory_data_analysis.py: Input: master_flight_data_cleaned.csv. Output: Printed EDA summary and visual *.png files.

3_build_difficulty_score.py: Input: master_flight_data_cleaned.csv. Output: test_<your_name>.csv.

4_post_analysis_insights.py: Input: test_<your_name>.csv. Output: Printed insights and visual_difficulty_drivers.png.

Key Data Files (.csv)
master_flight_data_cleaned.csv: The clean, unified dataset that serves as the foundation for all analysis and modeling.

test_<your_name>.csv: The final submission file containing flight details, engineered features, and the difficulty scores/ranks from all models.

Visual Outputs (.png)
The scripts will generate several visual_*.png files. These are the charts and graphs intended for use in the final presentation.
