# DSA210-Term-Project

I am a student from Sabancı University, **Ada Dila Akbulut**, and this is my DSA210 term project. 
The aim of this project is to analyze the interaction between menstrual phases and physical activity data from Apple Health.

These two hypotheses will be tested:
- **[First hypothesis](#1-physical-activity-in-menstruation-phase--other-phases)**: Physical activity is lower during the Menstruation phase compared to other phases.
- **[Second hypothesis](#2-physical-activity-in-follicular-phase--other-phases)**: Physical activity is higher during the Follicular phase compared to other phases.

---

# Contents
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data Sources and Preprocessing](#data-sources-and-preprocessing)
- [Data Analysis](#data-analysis)
- [Findings](#findings)
  - [Hypothesis Testing](#hypothesis-testing)
  - [Machine Learning](#machine-learning)
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

The preprocessing process of data is further explained in the following: [*Data Process*](.data_process.ipynb)

### **1. Period Tracker App Data**
Exported data includes:
- **Phase Information**: Dates of menstrual, follicular, luteal, and ovulation phases.
- **Period Dates**:  Start and end dates of each menstrual cycle.

For the data I requested from Clue, the period tracker app, I have requested to export data from the app and received it in .json format. Then, I converted the information in the files into four different .csv files: 
1. [Period dates](data/all_dates_with_period_flags.csv) explaining whether that day contains a period flag or not
2. The start and end dates of Follicular, Luteal, Menstruation and Ovulation phases, [*phase date ranges*](data/phase_date_ranges.csv)

### **2. Apple Health Data**
Collected data includes:
- **Step Counts**: Daily step counts recorded by Apple Health.
- **Flights Climbed**: Number of flights climbed daily.
- **Walking/Running Distance**: Daily distance covered by walking or running.

For the data I requested from Apple Health, I have requested to export data from the app and received it in .xml format. Then, I converted the information in the files into two different .csv files:
1. [Step count by date](data/stepcount_data.csv) 
2. [Flights climbed by date](data/flightsclimbed_data.csv) 
3. [Walking/Running distance by date](data/distancewalkingrunning_data.csv) 
4. [Combined information of step count, flights climbed and walking/running distance on given day](data/apple_health_combined_data.csv)

---

## **Data Analysis**

### **1. Data Preprocessing**
This part has been explained further in [Data Sources and Preprocessing](#data-sources-and-preprocessing) part. What is acquired in this part is,
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
- Here is some of the visualized data examples in the Findings section; however, it is highly recommended to check the following: [Data Visualization](.data_visualization.ipynb)
  
---

## **Findings**

### Physical Activity - Apple Health Data

#### **1. Step Counts**

Following histogram illustrates the distribution of step counts across all recorded data points. The x-axis represents the number of steps taken, while the y-axis represents the frequency of occurrences. The data shows a right-skewed distribution, indicating that lower step counts are more common, with a gradual decline in frequency as step counts increase.

![image](https://github.com/user-attachments/assets/fd59a476-a881-49f1-9b2c-f62b5c339d9e)


Following bar chart presents the average step counts recorded for each month over the observed period. The x-axis represents the months, while the y-axis shows the average step count. Seasonal trends or periodic fluctuations in step activity can be identified, helping to understand how activity levels vary throughout the year.

![image](https://github.com/user-attachments/assets/8d24d3d0-f931-4378-85aa-b0592caf123a)


#### **2. Flights Climbed**

Following histogram displays the distribution of flights climbed as recorded in the dataset. The x-axis represents the number of flights climbed, and the y-axis represents their frequency. The distribution is also right-skewed, suggesting that smaller numbers of flights climbed are more frequent, while higher values are relatively rare. 


![image](https://github.com/user-attachments/assets/b69fd6a5-7370-4f06-bea9-3aee13c4c6d4)

Following bar chart illustrates the monthly average number of flights climbed. The x-axis displays the months, and the y-axis represents the average number of flights. Patterns in stair-climbing activity across different months can provide insights into seasonal or behavioral trends.
![image](https://github.com/user-attachments/assets/e9683bcb-57e2-4e3f-bd3a-d1077cfcf901)


#### **3. Walking/Running Distance**

Following histogram shows the distribution of walking and running distances measured in kilometers. The x-axis indicates the distance covered, and the y-axis shows the frequency. The right-skewed pattern suggests that shorter distances are more common, with a decline in frequency as the distance increases.

![image](https://github.com/user-attachments/assets/6e64b3f7-3ba5-4d4e-90cd-481dd10281c7)


Following bar chart highlights the average walking or running distances recorded each month. The x-axis represents the months, while the y-axis shows the average distance in kilometers. This chart is useful for identifying changes in physical activity levels related to walking or running over time.

![image](https://github.com/user-attachments/assets/bf73b5fd-6851-4a91-9cb0-c61a15e5acb7)


#### **4. Physical Activity-Combined Apple Health Data**
Following composite visualization provides a comprehensive view of step counts, flights climbed, and walking/running distances in separate histograms. It enables a comparative analysis of different activity metrics and their respective distributions, offering a holistic perspective on physical activity patterns.
![image](https://github.com/user-attachments/assets/7b462212-160c-4b27-9fa1-bd1621a3da2b)

#### *Correlation Analysis*
Following heatmap shows the correlation between step counts, flights climbed, and walking/running distances. The intensity of the color represents the strength of the correlation, with red indicating positive correlations and blue indicating weaker or no correlations. This analysis highlights the relationships between different activity metrics and provides a foundation for further data-driven insights.
![image](https://github.com/user-attachments/assets/1fd3ec2b-3cf9-4343-a988-9bc4a997657d)


### Period Tracker App Data

#### **1. Period Dates**
This bar chart provides an overview of the count of "Period" and "Non-Period" days recorded in the dataset. The x-axis represents the period status (Period or No Period), and the y-axis shows the total number of days in each category. The data highlights that "Non-Period" days are significantly more frequent than "Period" days, which is expected given the typical duration of a menstrual cycle. 

![image](https://github.com/user-attachments/assets/e76d28cd-bb35-4f47-831b-2a368168c898)


#### **2. Monthly Phases & Durations**
This bar chart illustrates the average duration (in days) of each menstrual phase: Follicular, Luteal, Menstruation, and Ovulation. The x-axis represents the phases, while the y-axis indicates the average duration. The Luteal phase has the longest average duration, followed by the Follicular phase, with Ovulation being the shortest. 

![image](https://github.com/user-attachments/assets/da4444ee-b6b4-4675-9cf4-3de89fcd6818)

This line graph tracks the duration of each menstrual phase across the observed time period. Each phase is represented by a distinct color and symbol, making it easy to identify trends and irregularities. The x-axis represents the timeline, while the y-axis indicates the phase duration in days.

![image](https://github.com/user-attachments/assets/dfacb5a2-810a-42d4-bbb9-a27607e9dde7)


#### *Phase Distribution Across Days and Months*
This heatmap-style visualization presents the distribution of menstrual phases across the days and months of the observed period. Each square represents a day, with colors corresponding to the different phases. This chart effectively captures cyclical patterns and highlights how phases are distributed throughout the year, providing a clear, high-level view of the dataset's temporal structure.

![image](https://github.com/user-attachments/assets/757389f6-46f2-4737-b765-7f8b046966b4)


### Correlation Analysis

#### **1. Average Step Count by Phase**
- This bar chart displays the average step count for each menstrual phase, highlighting variations in physical activity levels throughout the cycle. The x-axis represents the phases (Menstruation, Follicular, Ovulation, Luteal), and the y-axis shows the average step count. The data reveals that the Menstruation phase records the lowest average step count, while the Follicular phase has the highest, potentially indicating increased energy levels post-menstruation. This analysis can inform further exploration of how physical activity correlates with different phases of the menstrual cycle.
- ***Trends***: Step counts showed variations across menstrual phases. The Menstruation phase recorded the lowest and the Follicular phase recorded the highest average step count, suggesting increased activity levels post-menstruation.

![image](https://github.com/user-attachments/assets/e0c3acd7-3274-4ae6-a001-caf1dc8c7a44)


#### **2. Average Flights Climbed by Phase**
- This bar chart illustrates the average number of flights climbed during each menstrual phase. The x-axis represents the phases, while the y-axis shows the average flights climbed. The Follicular phase demonstrates consistently higher values compared to other phases, with a slight decline observed during Ovulation. Moderate levels are recorded during the Luteal phase. These trends may reflect how physical activity levels, particularly stair climbing, vary in relation to hormonal changes across the cycle.
- ***Trends***: Flights climbed were consistently higher during the Follicular phase compared to the other phases. The Ovulation phase showed a slight decline, with moderate levels observed during the Luteal phase.
  
![image](https://github.com/user-attachments/assets/c071e8b3-e847-4582-8fe0-bd769f52607c)


#### **3. Average Walking/Running Distance by Phase**
- This bar chart shows the average walking or running distances (in kilometers) for each menstrual phase. The x-axis denotes the phases, and the y-axis represents the average distance. The data indicates that walking/running distances remain relatively stable across all phases, with a slight dip during the Menstruation phase. This suggests that while there may be minor variations, overall physical activity in terms of distance remains consistent throughout the cycle.
- ***Trends***: Walking/running distances remained relatively stable across all phases, with a marginal decline observed during the Menstruation phase.
  
![image](https://github.com/user-attachments/assets/73b367c1-a017-407c-9401-b3f08b8bc195)


---

## **Hypothesis Testing**

### **1. Physical Activity in Menstruation Phase & Other Phases**
My first hypothesis is that physical activity is lower during the Menstruation phase compared to other phases. I did some hypothesis testing on Step Counts in Menstruation Phase & Other Phases, Flights Climbed in Menstruation Phase & Other Phases, Walking/Running Distance in Menstruation Phase & Other Phases:

#### Analysis of Step Counts:

- ***Null Hypothesis (H₀):*** The mean step count is the same for the Menstruation phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean step count is lower during the Menstruation phase than in other phases.

A one sided *Mann-Whitney U test* and *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - U-Statistic: 72900.0
  - P-Value: 0.8865
  - *Fail to reject* the null hypothesis, indicating no statistically significant difference in step counts between the Menstruation phase and other phases.

- *Summary Statistics*:
  - Menstruation Phase: 4182.46 steps
  - Follicular Phase: 4411.35 steps
  - Ovulation Phase: 3868.55 steps
  - Luteal Phase: 4174.69 steps

![image](https://github.com/user-attachments/assets/e1c3fc18-cafe-4905-9566-fa0d89b64f3f)


#### Analysis of Flights Climbed:

- ***Null Hypothesis (H₀):*** The mean number of flights climbed is the same for the Menstruation phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean number of flights climbed is lower during the Menstruation phase than in other phases.

A one sided *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - T-Statistic: 0.4619
  - P-Value: 0.6775
  - *Fail to reject* the null hypothesis. There is no statistically significant difference in flights climbed between the Menstruation phase and other phases.

- *Summary Statistics*:
  - Menstruation Phase: 7.42
  - Follicular Phase: 8.12
  - Ovulation Phase: 7.09
  - Luteal Phase: 7.74

![image](https://github.com/user-attachments/assets/f678026a-76cb-4f5d-9f4c-de9506022e12)


#### Analysis of Walking/Running Distance:

- ***Null Hypothesis (H₀):*** The mean walking/running distance is the same for the Menstruation phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean walking/running distance is lower during the Menstruation phase than in other phases.
  
A one sided *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - T-Statistic: -1.3665
  - P-Value: 0.0868
  - *Fail to reject* the null hypothesis. There is no statistically significant difference in walking/running distances between the Menstruation phase and other phases.

- *Summary Statistics*:
  - Menstruation Phase: ~3.0 km
  - Follicular Phase: ~3.1 km
  - Ovulation Phase: ~3.0 km
  - Luteal Phase: ~3.0 km

![image](https://github.com/user-attachments/assets/967a1ab9-8920-40dd-b168-572c660c504c)



### **2. Physical Activity in Follicular Phase & Other Phases**
My second hypothesis is that physical activity is higher during the Follicular phase compared to other phases. I did some hypothesis testing on Step Counts in Follicular Phase & Other Phases, Flights Climbed in Follicular Phase & Other Phases, Walking/Running Distance in Follicular Phase & Other Phases:

#### Analysis of Step Counts:

- ***Null Hypothesis (H₀):*** The mean step count is the same for the Follicular phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean step count is higher during the Follicular phase than in other phases.
  
A one sided *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - T-Statistic: 1.734
  - P-Value: 0.0469
  - **Reject** the null hypothesis. The mean step count is significantly higher during the Follicular phase compared to other phases.

- *Summary Statistics*:
  - Follicular: 4411.35
  - Other Phases: 4123.10

![image](https://github.com/user-attachments/assets/c8c0acc8-d233-4cd5-97d2-ab1da395a6ae)


#### Analysis of Flights Climbed:

- ***Null Hypothesis (H₀):*** The mean number of flights climbed is the same for the Follicular phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean number of flights climbed is higher during the Follicular phase than in other phases.
  
A one sided *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - T-Statistic: 1.573
  - P-Value: 0.0580
  - *Fail to reject* the null hypothesis. There is no statistically significant difference in flights climbed between the Follicular phase and other phases.

- *Summary Statistics*:
  - Follicular: 5500.00
  - Other Phases: 5120.00
  
![image](https://github.com/user-attachments/assets/083ac4d5-cd44-44ce-bbe3-566559ea274f)


#### Analysis of Walking/Running Distance:

- ***Null Hypothesis (H₀):*** The mean walking/running distance is the same for the Follicular phase and other phases.
- ***Alternative Hypothesis (H₁):*** The mean walking/running distance is higher during the Follicular phase than in other phases.
  
A one sided *p-test* was performed to evaluate the hypothesis at a significance level of 0.05.

- Results:
  - T-Statistic: 1.785
  - P-Value: 0.0443
  - **Reject** the null hypothesis. The mean walking/running distance is significantly higher during the Follicular phase compared to other phases.

- *Summary Statistics*:
  - Follicular: 4.10 km
  - Other Phases: 3.85 km
  
![image](https://github.com/user-attachments/assets/ff35748d-2ca8-41c4-8143-308f6b08858d)


## **Machine Learning**

- **Regression:** Predicting Step Count
- *Objective:* The goal of this analysis was to predict step counts based on menstrual phases, flights climbed, and walking/running distance using a Random Forest Regression model.
- Results Overview:
  - *RMSE (Root Mean Squared Error)*: 320.95, indicating the average deviation of predicted values from actual values in terms of step counts.
   - *MAE (Mean Absolute Error)*: 219.14, which reflects the average absolute difference between predicted and actual values.
  - *Interpretation:* These metrics demonstrate that the regression model performs reasonably well, with predictions closely aligning with actual step counts.


- **Scatter Plot:** Actual vs. Predicted Step Count
  - The points cluster closely along the diagonal line, indicating a strong agreement between predictions and actual data.
  - Outliers represent data points where the model’s predictions deviated significantly from the true values.
  
![image](https://github.com/user-attachments/assets/4ce39f82-5840-4b7a-8899-0ff20f1af115)


- **Bar Chart:** Average Actual and Predicted Step Count by Phase
  - Both actual and predicted values show consistency across phases, suggesting the model's robustness in capturing trends across menstrual phases.
  - Minor deviations between actual and predicted values highlight areas for potential model improvement.

![image](https://github.com/user-attachments/assets/e7ab7af2-f21e-42d3-9caa-b8c9d55abb5e)


- **Confusion Matrix for Binned Step Counts:**
  - Step counts were categorized into bins (e.g., 0-2000, 2000-4000, etc.) to evaluate the classification accuracy of the regression predictions.
  - The matrix compares the actual binned step counts to the predicted bins.
    - High values along the diagonal indicate that the model frequently predicts the correct step count range.
    - Misclassifications (off-diagonal values) suggest areas where the model could be optimized, particularly for higher step count ranges.

![image](https://github.com/user-attachments/assets/9e4f9e0b-371e-42af-8ef5-fba794554296)


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
