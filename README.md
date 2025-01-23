# Daily Nurse Staffing Analysis

## Project Overview

This project involves an in-depth analysis of the CMS Payroll Based Journal (PBJ) Daily Nurse Staffing dataset for Q1 2024. The focus is on examining contractor usage across various states and facilities, particularly looking into contractor-to-employee staffing ratios and role-specific contractor utilization including Registered Nurses (RN), Licensed Practical Nurses (LPN), Certified Nursing Assistants (CNA), and Med Aides.

## Objective

The main objective is to identify trends and provide data-driven recommendations to help Clipboard Health optimize their sales efforts by targeting regions, facilities, and specific roles where the demand for contractor staffing is highest.

## Key Features

- **Data Analysis**: Detailed examination of contractor and employee staffing patterns.
- **Visualization**: Graphical representation of data to illustrate key insights and trends.
- **Recommendations**: Strategic insights provided for targeted sales initiatives.

## Technologies Used

- Python
- Pandas for data manipulation
- Matplotlib for data visualization
- Google Colab for executing Python notebooks

## Installation

To set up the project environment, ensure you have Python installed and proceed to install the required packages:

```bash
pip install pandas matplotlib
Usage
Data Loading and Cleaning
Load the data using Pandas, handle mixed data types issues, and clean missing values:

python
Copy
import pandas as pd

df = pd.read_csv('PBJ_Nursingstaffing.csv', encoding='ISO-8859-1', low_memory=False)
Data Analysis
Analyze staffing ratios and calculate contractor usage:

python
Copy
# Calculate contractor-to-employee ratio
df['contractor_ratio'] = df['Total_Contractor_Hours'] / df['Total_Employee_Hours']

# Group and analyze data by state
state_analysis = df.groupby('STATE')['contractor_ratio'].mean()
Visualization
Visualize the results to identify trends:

python
Copy
import matplotlib.pyplot as plt

plt.bar(state_analysis.index, state_analysis.values)
plt.title('Average Contractor Ratio by State')
plt.xlabel('State')
plt.ylabel('Contractor Ratio')
plt.xticks(rotation=90)
plt.show()
Results
The analysis reveals significant variability in contractor usage across states and roles, with some states showing a higher reliance on contractors than others. Detailed findings and state-specific data are available in the repository.

Recommendations
Based on the analysis, targeted recommendations are provided for Clipboard Health to focus on states and facilities with the highest usage of contractors, optimizing their sales and marketing strategies.

Contributing
Contributions to this project are welcome! Please fork the repository and submit a pull request with your improvements.

License
Distributed under the MIT License. See LICENSE for more information.

Contact
Your Name – your-email@example.com

Project Link: https://github.com/yourgithubusername/daily-nurse-staffing

vbnet
Copy

This README is designed to guide users through setting up, using, and contributing to your project. It includes sections on the project's purpose, how to set up the environment, detailed instructions on how to run the analysis, and how to visualize the results.
