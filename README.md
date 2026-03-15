# 🏃‍♂️ AthleAgent

> **Shifting Athlete Care from Reaction to Prevention.**

[![Kotlin](https://img.shields.io/badge/Kotlin-Android-blue.svg)](https://kotlinlang.org/)
[![AI](https://img.shields.io/badge/AI-Gemini_API-orange.svg)](https://deepmind.google/technologies/gemini/)
[![HealthConnect](https://img.shields.io/badge/Integration-Health_Connect-green.svg)](https://developer.android.com/health-and-fitness/guides/health-connect)

## 📖 Overview
Athlete injuries are complex, resulting from a combination of factors that are traditionally tracked in isolation.**AthleAgent** provides a single, intelligent platform to unify the four key pillars of athlete wellness.

By continuously monitoring diverse data points, AthleAgent shifts the paradigm of sports medicine from reactive treatment to proactive injury prevention, generating a daily "Risk Score" based on real-time data. 

## ✨ Core Features

AthleAgent integrates seamlessly into an athlete's daily routine:

**📊 Daily Check-ins:** Athletes fill out quick physical and psychological surveys to log subjective data such as energy levels, muscle soreness, and current stress levels. 
**🥗 AI Meal Analysis:** Utilizing a Nutrition API, athletes simply upload an image of their meal. The system automatically extracts nutritional values (Calories, Protein, Carbohydrates) and tracks them against daily targets. 
**⌚ Health Connect Sync:** Seamless integration with Google Health Connect API to pull objective wearable data automatically, such as live heart rate monitoring and sleep data. 
**📈 Actionable Insights:** The system calculates a Daily Risk Score (%) accompanied by a 7-day trend chart, alerting both athletes and coaches to potential injury risks before they happen.

## 🏗️ System Architecture & Workflow

The platform features two distinct user flows managed via **Google Authentication Service**: 

### The Athlete Application
* **Onboarding:** Register and send a "Join Team Request" to a specific coach. 
* **Data Logging:** Upload meal images, connect to Health Connect, and fill out stress level surveys. 
* **Monitoring:** View personal injury risk, recommendations, and athlete history. 

### The Coach's Toolkit
* **Team Management:** Create a team, view the athlete list, and approve athlete join requests. 
* **Risk Assessment:** Monitor the entire roster's real-time risk scores and historical data to adjust training loads accordingly. 

## 🧠 Design Philosophy

Designed specifically for the demands of professional sport, our architecture prioritizes: 

* **Usability:** A simple, intuitive interface that minimizes manual data entry. 
* **Reliability:** Robust handling of missing data and resilience to external service outages. 
* **Supportability:** A modular system architecture that allows for continuous improvement and retraining of the ML model with real-world data. [cite: 1]
* **Performance:** Optimized for speed and computational efficiency, delivering real-time insights when they matter most.

## 📱 Screenshots

| Architecture | Workflow | Screens | Athlete View | Coach View |
| :---: | :---: | :---: | :---: | :---: |
| <img src="https://github.com/yahav97/AthleAgent-App/blob/main/assets/archi.png?raw=true" width="200"/> | <img src="https://github.com/yahav97/AthleAgent-App/blob/main/assets/workflow.png?raw=true" width="200"/> | <img src="https://github.com/yahav97/AthleAgent-App/blob/main/assets/screens.png?raw=true" width="200"/> | <img src="https://github.com/yahav97/AthleAgent-App/blob/main/assets/Athlete.png?raw=true" width="200"/> | <img src="https://github.com/yahav97/AthleAgent-App/blob/main/assets/coach.png?raw=true" width="200"/> |


## 🚀 Getting Started

### Prerequisites
* Android Studio (Latest Version)
* Physical Android device (Recommended) with [Health Connect](https://play.google.com/store/apps/details?id=com.google.android.apps.healthdata) installed. 
* Google Gemini API Key (for the Nutrition Vision API features). 

### Installation
1.  Clone the repository:
    ```bash
   git clone https://github.com/yahav97/AthleAgent-App.git
    ```
2.  Open the project in Android Studio.
3.  Add your API Key to the `local.properties` file:
    ```properties
    GEMINI_API_KEY=your_api_key_here
    ```
4.  Sync the project with Gradle files and run the application.

---

