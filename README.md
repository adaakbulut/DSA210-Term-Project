# DSA210-Term-Project

I am a student from Sabancı University, **Ada Dila Akbulut**, and this is my DSA210 term project. 
The aim of this project is to analyze the interaction between menstrual phases and physical activity data from Apple Health.

---

# Contents
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data Source](#data-source)
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

## **Data Source**
To protect privacy, raw data will not be shared in the repository. Instead, all analysis scripts and processed, anonymized data will be provided. A `.gitignore` file will be used to ensure sensitive or unnecessary files are excluded.

### **1. Period Tracker App Data**
Exported data includes:
- **Phase Information**: Menstrual, follicular, luteal, and ovulation phases.
- **Period Dates**:  Start and end dates of each menstrual cycle.

### **2. Apple Health Data**
Collected data includes:
- **Step Counts**: Daily step counts recorded by Apple Health.
- **Flights Climbed**: Number of flights climbed daily.
- **Walking/Running Distance**: Daily distance covered by walking or running.
  
---

## **Data Analysis**

### **1. Data Preprocessing**
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
- Histograms, boxplots, heatmaps, bar charts, line charts, scatter plots, violin plots may be used.

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
