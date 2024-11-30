# DSA210-Term-Project

I am a student from Sabancı University, **Ada Dila Akbulut**, and this is my DSA210 term project. 
The aim of this project is to analyze the interaction between my phases' patterns recorded in my FLO period tracker app and my music listening habits from Spotify. 

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
Music has a significant impact on emotions, and emotional changes may be tied to biological rhythms. By studying the data I acquired from FLO and Spotify, I hope to:
- Understand the relationship between my music preferences (genre, tempo, energy, sound, etc.) and my monthly phases.
- Identify trends that could help in creating personalized playlists to support emotional well-being during different phases.
- Gain actionable insights into how monthly phases influences music preference.

---

## **Project Goal**
The goal of this project is to uncover how different phases in my FLO period tracker correlate with my Spotify listening habits, including genres, tempos, and other audio attributes. By analyzing these interactions, I aim to generate actionable insights and potentially develop a playlist recommendation system based on my emotional and biological rhythms.

---

## **Data Source**
To protect privacy, raw data will not be shared in the repository. Instead, all analysis scripts and processed, anonymized data will be provided. A `.gitignore` file will be used to ensure sensitive or unnecessary files are excluded.

### **1. FLO Period Tracker App**
Exported data includes:
- **Phase Information**: Menstrual, follicular, luteal, and ovulation phases.
- **Mood Tags**: Emotional states (e.g., happy, anxious, energized).
- **Symptom Data**: Physical or emotional symptoms associated with each phase.

### **2. Spotify API**
Collected data includes:
- **Listening History**: Songs, timestamps, listening frequency and sound.
- **Track Attributes**: Tempo, energy, valence, and danceability.
- **Genres and Artists**: Categorization of songs by genre and artist metadata.

---

## **Data Analysis**

### **1. Data Preprocessing**
- Exported and cleaned datasets from FLO and Spotify.
- Extracted features like total listening time, genre distribution, audio attributes (tempo, energy, valence), and FLO mood phases.
  
### **2. Exploratory Data Analysis (EDA)**
- Analyzed data distributions and visualized trends in phases and music preferences.
- Identified correlations between Spotify attributes and FLO phases/moods.

### **3. Correlation Analysis**
- Examine relationships between monthly phases and Spotify features.
- Determined if certain phases align with specific music listening preferences.
- Investigated the impact of sound levels (volume) and specific audio features on mood shifts.

### **4. Visualization**
   - Visualizations to represent trends and correlations.
   - Histograms, boxplots, heatmaps, bar charts, line charts, scatter plots, violin plots may be used.

---

## **Findings**
This section will be completed after the analysis is conducted.

---

## **Limitations and Future Work**
This section will be completed after the analysis is conducted. However, the expected limitations are:
- Limited to personal data, which may not generalize to larger populations.
- Limited features exported by FLO and Spotify, other factors that may influence emotional well-being and music preferences are not considered.
- The frequency of data entries to FLO period tracker app may differ from month to month.
