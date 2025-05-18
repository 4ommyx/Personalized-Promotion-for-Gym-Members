
# Gym Member Analytics & Segmentation

This project analyzes a dataset of **973 gym members** with the goal of building a classification model to predict fitness experience levels and performing customer segmentation to suggest personalized promotions and strategies.

## Dataset Overview

The dataset includes :
- **Demographics :** Age, Gender, Height, Weight  
- **Workout Info :** Duration, Calories, Type, Frequency  
- **Biometric Data :** Heart Rate, Fat Percentage, Water Intake  
- **Target Variable :** `Experience_Level` (1: Beginner → 3: Expert)

## Project Objectives

- Perform **EDA and Feature Engineering**  
- Create new insightful metrics
- **Predict** member **Experience_Level** using classification models  
- Segment customers using clustering(K-mean)  
- Design actionable marketing strategies based on segments

## Experience Level Prediction (Classification Model)

Models tested
- **KNN**
- **Decision Tree**
- **Random Forest**
- **SVM**

> 📈 **Best Accuracy: 92.31% (Random Forest with GridSearchCV)**

## Feature Engineering (Segmentation)

New features created to enhance analysis

| Feature | Description |
|--------|-------------|
| `Intensity_Score` | Calories_Burned / Session_Duration (cal/hours) |
| `Fat_Percentage_to_Water_Ratio` | Fat_Percentage / Water_Intake (%/L) |
| `Consistency_Score` | Session_Duration × Workout_Frequency (hours/week) |


## Customer Segmentation

Segmentation was done using KMeans based on:
- `Intensity_Score`
- `Fat_Percentage_to_Water_Ratio`
- `Consistency_Score`

**Optimal number of clusters : 4 (based on Elbow + Silhouette Score)**  
Generated interactive **3D scatter plot** for segment visualization.


## Segment Profiles & Actions

| Segment | Profile | Strategy |
|---------|---------|----------|
| **0** | Fit & Consistent | Loyalty rewards, VIP class upsell |
| **1** | Low motivation | Restart challenges, Buddy workouts |
| **2** | Intense but inconsistent | Coaching plan, habit-building tools |
| **3** | At-risk group | Health recovery programs, beginner support |

## Visualization Highlights

- 📊 Radar Chart comparing segment behavior  
- 🎥 3D Animated Cluster Visualization  
- 📉 Elbow + Silhouette Score for optimal clustering
