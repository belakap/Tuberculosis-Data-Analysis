**Assessing the Impact of Climate Change on Tuberculosis Incidence: A Global Perspective**


This study explores climate and Tuberculosis (TB) data to assess the impact of climate change on Tuberculosis incidence. 

The goal of this study is to analyze the impact of climate change on Tuberculosis incidence, using quantitative data, and present findings to inform public health strategies.

**Objectives**

Assess the impact of multiple climate indicators (average temperature, rainfall, CO₂ emissions, extreme weather events) on TB incidence trends across 7 countries.

Use available global TB and climate datasets covering at least 20 years (2000 – 2023) for consistent cross-country comparison.

Identify whether climate factors have a significant direct or indirect influence on TB burden, to inform public health planning and integrated climate-health policy.

**Steps**

1. Define the study question: "Assessing the Impact of Climate Change on Tuberculosis Incidence: A Global Perspective"

2. Determine the primary goal and objectives.

3. Research the datasets needed for analysis.

4. Save datasets as CSV files.

5. Perform preliminary analysis of raw data to understand and guide the cleaning process.

6. Clean data.

7. Perform in-depth analysis and visualization.

**Analysis criteria**

The following criteria have been met.

1. Export two datasets from Kaggle.com: 

       https://www.kaggle.com/datasets/khushikyad001/tuberculosis-trends-global-and-regional-insights

       https://www.kaggle.com/datasets/bhadramohit/climate-change-dataset

2. Identify the required packages

3. Load datasets and save them as CSV files. Rename and read them in Python using pandas.

- Climate Change Trends.csv

- Tuberculosis Trends.csv

4. Clean and merge data

 Datasets were cleaned using pandas. 
                         
Climate dataset was cleaned as follow:

- Drop columns that are not relevant to the analysis
  
- Sort the DataFrame by the 'Year' column in ascending order

- Average duplicates for each country and year to have each country appear once a year.

TB dataset cleaning steps:

- Filter the DataFrame to keep only the columns relevant to the analysis.
- Sort the DataFrame by the 'Year' column in ascending order
- Average duplicates for each country and year to have each country appear once a year.

After the initial cleaning, both datasets were filtered to include only the countries that appear in both the climate and TB data. However, these two “common” datasets were still mismatched, the number of years available for each country in the climate dataset did not always match the number of years in the TB dataset for the same country and time period.

To ensure an accurate merge and avoid bias in the analysis, both datasets were filtered to keep only the rows where the years fully matched. Specifically, we:
1.	Grouped each dataset by country and collected the unique years available for each country.
2.	Identified the years that are common to every country within each dataset.
3.	Found the final set of years that overlap in both datasets for all countries.
4.	Filtered the climate and TB datasets to keep only rows where the year is in the final common set.

This helps to ensure that the final datasets were perfectly aligned, containing only the same countries and the same years. This approach allows for a consistent merge and increases the accuracy of the analysis.

5. Present and visualize data

heatmap, lineplot, and scatterplot with a Lowess (locally weighted scatterplot smoothing) trend line were used.

6. Use the virtual environment.
 
8. Build a data dictionary. 

9. Interpret and document.

**Summery of findings**

This analysis explored the complex relationship between climate indicators and tuberculosis (TB) incidence across 7 countries, 

combining visual trends, statistical testing, and country-level rankings.

Visual analysis suggested some nonlinear patterns, such as:

A U-shaped relationship between TB incidence and both average temperature and rainfall, where moderate levels were associated with lower TB rates.

A mild negative trend with extreme weather events.

Almost no visual relationship between CO₂ emissions and TB.

However, the statistical analysis revealed no significant correlations between TB incidence and any climate variables. 

The only variable close to significance was rainfall (p = 0.087), indicating a weak, non-conclusive link. Overall, 

the model explained very little variation, emphasizing that non-climatic factors such as poverty, healthcare access, population density, 

HIV burden, and nutrition are likely the main drivers of TB globally.

At the country level:

India bears the highest TB incidence (271.94) and a large number of cases (476,178), reflecting a substantial disease burden.

South Africa has the highest TB mortality (Avg Mortality = 26.13; Deaths = 92,505), indicating more severe outcomes.

China consistently shows low TB burden and has the best Rank_Score (9.0), suggesting better health control and possibly stronger infrastructure.

Countries like Russia, India, and South Africa have higher Rank_Scores, reflecting greater TB impact or weaker performance across the combined indicators.

The USA shows a mid-level Rank_Score (13.0 in one table, 13.0 in another), indicating a relatively low TB incidence and mortality compared to high-burden 

countries like India or South Africa. The USA’s TB rates are much lower thanks to stronger public health systems, better access to diagnosis and treatment, and 

more resources for TB control.

Summary

Although climate factors may have indirect effects on TB through social disruption, malnutrition, or population movement, this analysis finds no strong or direct climate influence on TB patterns. Other relevant social, economic, and health system indicators should be analyzed to better understand and address the true drivers of TB incidence and outcomes.

**Recommendation**

Before giving the final recommendations, we will include additional non-climate indicators such as socioeconomic status, healthcare access, HIV prevalence, and urbanization in analyses to build a clearer understanding of TB’s causes.

**Project layout**


|File                                |Description                                                                            | 	
|------------------------------------|---------------------------------------------------------------------------------------|
|README.md                           |General information about the project                                                  |
|RAW DATA                            |raw data files                                                                         |
|CLEAN DATA                          |clean data files                                                                     |
|Dictionary                          |Dictionary for the raw data                                                                |
|01a-raw-climate-basic-analysis.ipynb|Jupyter notebook showing simple data analysis to understand the raw datasets               | 
|01b-raw-TB-basic-analysis.ipynb     |and guide the cleaning process.                                                        |

|02a-clean-climate-data.ipynb        |Jupyter notebook showing the cleaning performed                                    |
|02b-clean-TB-data                   |
|Commons-and-merges.ipynb            |Jupyter notebook with merged dataset.                                               |
|Data-Analysis.ipynb                 |Jupyter notebook with analysis.                                                     |


**Requirements to run the project**

*Git*: if not yet installed, you can download at https://git-scm.com/downloads

*Python*: this project uses python 3.12. If not yet, you can install or update python at https://www.python.org/downloads/

*Jupyter notebook* or *vs code*

*virtual environment(venv)*: 
           Installation: as you will use python 3, the venv is already installed.
           Create venv: python3 -m venv venv or python -m venv venv.
           Activate venv: source/Scripts/activate(for Windows users) or source venv/bin/activate(for Mac and Linux users).

*Package*: pip install requirements.txt. 

**Getting Started**

Clone this repo.

Create a virtual environment and install the packages listed in the requirements.txt file.

Open RAW DATA file to view the raw data.

Run 02a-clean-climate-data.ipynb and |02b-clean-TB-data.ipynb to clean the raw data.

Run Data-Analysis.ipynb file to view the analysis and visualizations.