## 📁 Project Structure

EDA_MiniProject_Group1_2025/
│
├── EDA_miniProject_Group1_2025ipynb                                   # Main Jupyter notebook
├── districtwise-missing-persons-2021-onwards.csv                      # Your selected dataset
├── README.md                                                          # Overview and instructions
└── Missing_Persons_EDA_Project_Presentation.pptx                      # Summary presentation

# 📊 EDA Project: District-wise Missing Persons in India (2021 - 2022)

## 🗂️ Dataset Overview
This project involves exploratory data analysis on a dataset detailing missing persons cases reported across various districts in India from the year 2021 to 2022. The data is disaggregated by state, district, gender, and age group.

- **Total Records**: 1841 rows
- **Total Features**: 22 columns
- **Source**: [data.gov.in](https://data.gov.in) – Government of India Open Data Platform
- **File Format**: CSV

### 👁️‍🗨️ Key Features:
- `year`: Year of reporting (from 2021 to 2022)
- `state_name`, `district_name`: Geographic identification
- Gender- and age-specific columns:
  - Children and adults separated into age buckets:  
    - Below 12 years, 12–16, 16–18, and 18+  
    - For **male**, **female**, and **transgender** persons
- `registration_circles`: The circle or jurisdiction where the report was filed

---

## 🎯 Project Objective

The aim is to:
- Understand the geographic and demographic distribution of missing persons
- Explore patterns and trends across age groups and genders
- Use statistical and visual methods to uncover insights for decision-making or further study

---

## 🧪 Steps Performed

### 1. Data Import and Cleaning
- Imported using `pandas`
- Verified data types and column names
- Checked for and confirmed **no missing** or **duplicate** values
- Converted applicable fields (e.g., dates, categories) if needed
- Replaced NaN's with 0

### 2. Descriptive Statistics
- Generated summary statistics for each numeric feature
- Aggregated total counts across age groups and gender

### 3. Visual Exploration
- **Histograms** and **density plots** for age/gender distributions
- **Bar charts** to compare district/state-wise counts
- **Box plots** to identify spread and outliers
- **Scatter plots** and **heatmaps** to explore correlation between variables

### 4. Group-Level Analysis on Data set
- Grouped by `state_name` and `year` to analyze yearly trends
- Analyzed `district_name` to identify high-concern regions

### 5. Advanced Python Techniques
- Used **lambda functions** for categorization (e.g., low/medium/high cases)
- Defined **user functions** to aggregate and visualize region-wise stats
- Employed **list comprehensions** to extract feature-based metadata

### 6. Insights and Conclusions

#### ✅ Key Findings from the EDA:

- The dataset captures detailed demographic breakdowns of missing persons (males, females, transgender individuals) across Indian districts and states from 2021 onwards.
- New columns were created to better interpret data:
  - **`missing_severity`** classified cases into Low/Medium/High based on total missing persons.
  - **`high_female_missing`** flagged districts with >100 female cases.
  - **`male_missing_class`** grouped districts by male missing counts into Low/Medium/High.
  - **`gender_summary`** provided a readable summary of total male, female, and transgender counts.
  - **`district_flag`** marked "Severe" districts with more than 200 total missing persons
- **Majority of cases** are concentrated in a few districts with high population density.
- **Female children (12–18 years)** are disproportionately reported missing.
- **Transgender** cases are rare but not absent — highlight for awareness.
- Several states show an **upward trend** in reports post-2021 — possibly due to improved reporting mechanisms.

#### 📊 Patterns and Relationships:

- **Gender Distribution:**
  - Female missing cases were notably high in several districts—some even surpassing male counts.
  - Transgender missing cases are reported, but in significantly lower numbers.

- **Correlation Analysis:**
  - The **correlation matrix** and **heatmap** revealed strong correlations between total gender-specific missing values and overall missing counts.
  - Correlation also exists between age-specific categories, indicating that patterns in one demographic group may predict trends in another.

- **State-wise and Year-wise Trends:**
  - **Pivot tables** showed how missing person counts fluctuate by state and year, suggesting systemic or regional influences.

#### 🚨 Anomalies and Notable Flags:

- Certain districts were flagged "Severe" for having over 200 missing cases, possibly indicating hotspots for deeper policy or security investigation.
- Numerical anomalies were observed where some values (e.g., counts >1000) stood out in otherwise moderate datasets—potential data quality or reporting spikes.

#### 🔍 Further Analysis Opportunities:

- **Temporal Analysis**:
  - With multiple years of data, time-series analysis could uncover increasing or seasonal trends in missing person cases.

- **Geo-Spatial Mapping**:
  - Mapping districts/states by severity could provide powerful visual insights for policy makers.

- **Predictive Modeling**:
  - Given the structured data, it would be viable to train models (like Random Forest or XGBoost) to predict high-risk districts using demographic inputs.

- **Sociological Exploration**:
  - Merging with external datasets (e.g., literacy, crime rate, economic indicators) may help uncover root causes behind the missing person trends.


