#  Wellness Center Analytics Dashboard  
### Python & Power BI Data Analysis Project

---

##  Project Overview
This project focuses on analyzing wellness center data to understand healthcare availability, doctor distribution, and category-wise services across different cities.

Using **Python for data cleaning and analysis** and **Power BI for visualization**, the project transforms raw data into meaningful insights through an interactive dashboard.

---

##  Objectives
- Analyze doctor distribution across cities  
- Identify areas with low healthcare coverage  
- Compare different healthcare categories  
- Build an interactive dashboard for insights  

---

##  Tools & Technologies
- Python (Pandas, NumPy)  
- Power BI  

---

## Workflow

###  Data Cleaning (Python)
- Handle missing values  
- Remove duplicates  
- Fix data types  
- Clean text data  

```python
import pandas as pd

df = pd.read_csv("data.csv")

df['WellnessCentreName'] = df['WellnessCentreName'].fillna("Unknown")
df['Category'] = df['Category'].fillna("Unknown")

df.drop_duplicates(inplace=True)

df['DoctorCount'] = pd.to_numeric(df['DoctorCount'], errors='coerce')

###  Data Analysis (Python)
Group data by city and category
Calculate totals and averages
city_summary = df.groupby('CityName')['DoctorCount'].sum()
category_summary = df.groupby('Category')['DoctorCount'].sum()

##  Data Visualization (Power BI)
KPI Cards (Total Doctors, Total Centers, Average Doctors)
Map Visualization (Latitude & Longitude)
Bar Chart (City-wise comparison)
Donut Chart (Category distribution)
Slicers (City, Category)
Insights Panel (DAX-based)

### Key Insights
Healthcare is concentrated in major cities
Allopathy category dominates doctor availability
Uneven distribution across regions
Some cities have low healthcare coverage

### Dashboard Features
Interactive filtering
Map-based visualization
Category comparison
Clean and professional UI
Dynamic insights panel
### Dashboard Preview

(Add your Power BI dashboard screenshot here)

### Conclusion

This project highlights patterns in healthcare distribution and helps identify areas that require improvement.

### Future Improvements
Add population-based analysis
Include time-based trends
Build predictive models
## Author

Shamsiya kp
