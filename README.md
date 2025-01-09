# DSA210-Term-Project

I am a student from Sabancı University, **Ada Dila Akbulut**, and this is my DSA210 term project. 
The aim of this project is to analyze the interaction between menstrual phases and physical activity data from Apple Health.

**Hypothesis** 

**First hypothesis**: Physical activity is lower during the Menstruation phase compared to other phases.
**Second hypothesis**: Physical activity is higher during the Follicular phase compared to other phases.

---

# Contents
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data Sources and Preprocessing](#data-sources-and-preprocessing)
- [Data Analysis](#data-analysis)
- [Findings](#findings)
- [Limitations and Future Work](#limitations-and-future-work)

---

## **Motivation**
Menstrual phases can significantly influence physical activity and overall well-being. Understanding how different phases correlate with physical activity patterns may help in better managing health and fitness goals. By studying the data I acquired from a period tracker app and Apple Health, I hope to:
- Understand the relationship between menstrual phases (e.g., follicular, luteal, ovulation, and menstruation) and my step counts, flights climbed, and walking/running distances.
- Identify trends in physical activity levels across different menstrual phases.
- Gain actionable insights into how physical activity varies with menstrual cycles and vice versa.

---

## **Project Goal**
The goal of this project is to uncover patterns in physical activity across menstrual phases by correlating data from a period tracker app and Apple Health. This project aims to provide insights into how menstrual phases influence physical activity levels and may suggest personalized recommendations for optimizing activity during different phases.

---

## **Data Sources and Preprocessing**
To protect privacy, raw data will not be shared in the repository. Instead, all analysis scripts and processed, anonymized data will be provided. A `.gitignore` file will be used to ensure sensitive or unnecessary files are excluded.

### **1. Period Tracker App Data**
Exported data includes:
- **Phase Information**: Dates of menstrual, follicular, luteal, and ovulation phases.
- **Period Dates**:  Start and end dates of each menstrual cycle.

For the data I requested from Clue, the period tracker app, I have requested to export data from the app and received it in .json format. Then, I converted the information in the files into four different .csv files: 
1. Period dates explaining whether that day contains a period flag or not (all_dates_with_period_flags.csv)
2. The start and end dates of Follicular, Luteal, Menstruation and Ovulation phases. (phase_date_ranges.csv)

### **2. Apple Health Data**
Collected data includes:
- **Step Counts**: Daily step counts recorded by Apple Health.
- **Flights Climbed**: Number of flights climbed daily.
- **Walking/Running Distance**: Daily distance covered by walking or running.

For the data I requested from Apple Health, I have requested to export data from the app and received it in .xml format. Then, I converted the information in the files into two different .csv files:
1. Step count by date (stepcount_data.csv)
2. Flights climbed by date (flightsclimbed_data.csv)
3. Walking/Running distance by date (distancewalkingrunning_data.csv)
4. Combined information of step count, flights climbed and walking/running distance on given day (apple_health_combined_data.csv)

---

## **Data Analysis**

### **1. Data Preprocessing**
This part is explained further in [Data Sources and Preprocessing](#data-source-and-preprocessing) part.
- Cleaned and structured datasets from the period tracker app and Apple Health.
- Merged datasets by date to align menstrual phases with physical activity metrics.
  
### **2. Exploratory Data Analysis (EDA)**
- Analyzed distributions of step counts, flights climbed, and walking/running distances across menstrual phases.
- Visualized trends in physical activity metrics during different phases.
  
### **3. Correlation Analysis**
- Examined relationships between menstrual phases and physical activity metrics.
- Investigated if certain phases align with increased or decreased physical activity levels.

### **4. Visualization**
- Visualizations to represent trends and correlations.
- Histograms, boxplots, heatmaps, bar charts, line charts, scatter plots are used.


**Step Count:**
![image](https://github.com/user-attachments/assets/fd59a476-a881-49f1-9b2c-f62b5c339d9e)
![image](https://github.com/user-attachments/assets/03fcdb35-4d95-4374-b928-c02bf7c4e332)

*Average Step Count:*
![image](https://github.com/user-attachments/assets/62beb2d2-7e71-479d-82f4-4c8e1f4af164)
![image](https://github.com/user-attachments/assets/8d24d3d0-f931-4378-85aa-b0592caf123a)


**Flights Climbed:**
![image](https://github.com/user-attachments/assets/b69fd6a5-7370-4f06-bea9-3aee13c4c6d4)
![image](https://github.com/user-attachments/assets/c9faa3d1-4cce-45a7-a02f-be1cc49d1e8f)

*Flights Climbed:*
![image](https://github.com/user-attachments/assets/d5b36f4c-20d3-427b-a29f-6d81f62680eb)
![image](https://github.com/user-attachments/assets/e9683bcb-57e2-4e3f-bd3a-d1077cfcf901)


**Walking/Running Distance:**
![image](https://github.com/user-attachments/assets/6e64b3f7-3ba5-4d4e-90cd-481dd10281c7)
![image](https://github.com/user-attachments/assets/71b30704-9137-4d4d-afd7-543940382e66)

*Walking/Running Distance:*
![image](https://github.com/user-attachments/assets/c0c78e91-8455-449c-bfd5-560c012e2c6a)
![image](https://github.com/user-attachments/assets/bf73b5fd-6851-4a91-9cb0-c61a15e5acb7)

---

## **Findings**
### **1. Step Counts**
- Trends: Step counts showed slight variations across menstrual phases. The Follicular phase recorded the highest average step count, suggesting increased activity levels post-menstruation.
**Statistical Test Results:**
- A Mann-Whitney U test revealed no significant difference between step counts during the Menstruation and Ovulation phases (p-value = 0.9584).
**Visual Insights:**
- Boxplots indicated a wider variation in step counts during the Menstruation phase, potentially reflecting day-to-day fluctuations in activity levels.
  
### **2. Flights Climbed**
- Trends: Flights climbed were consistently higher during the Follicular phase compared to the Ovulation phase, with average values dropping slightly during the Luteal phase.
**Statistical Test Results:**
- A two-tailed t-test comparing flights climbed during the Ovulation phase and other phases yielded no significant differences (p-value = 0.2099).
**Visual Insights:**
- Bar charts highlighted that while average flights climbed were higher during the Follicular phase, the differences were not statistically significant across phases.
  
### **3. Walking/Running Distance**
- Trends: Walking/running distances remained stable across all phases, with a marginal decline during the Menstruation phase.
**Statistical Test Results:**
- A two-tailed t-test comparing walking/running distances during the Menstruation phase and other phases confirmed no significant differences (p-value = 0.8926).
**Visual Insights:**
- Distance distributions were narrow across phases, indicating consistent daily activity regardless of menstrual phase.

### **Observations**
- No statistically significant differences were observed in physical activity metrics across menstrual phases.
- Marginally higher activity levels (step counts and flights climbed) were noted during the Follicular phase, aligning with anecdotal evidence of increased energy levels during this phase.
- The Menstruation phase showed a slight reduction in walking/running distances, potentially due to discomfort or fatigue.

---

## **Limitations and Future Work**
### **Limitations**
- The analysis is based on personal data, limiting its generalizability to larger populations.
- Period tracker data is restricted to phase information and period dates, while Apple Health data is limited to step counts, flights climbed, and walking/running distances.
- Data accuracy depends on the frequency and precision of entries in Apple Health and the period tracker app.
- External factors such as weather, mood, or daily activities that could influence physical activity are not accounted for.

### **Future Work**
- Extend the analysis to a broader dataset from diverse individuals to generalize findings.
- Incorporate additional metrics like heart rate variability, sleep patterns, or calorie expenditure for a more comprehensive analysis.
- Explore machine learning techniques to predict physical activity levels based on menstrual phases.
- Collaborate with researchers to validate findings and contribute to the growing body of menstrual health studies.
