
# AthleAgent 


## 📖 Overview
AthleAgent is a comprehensive mobile platform designed to bridge the gap between athletes and their coaches. The application tracks daily health metrics, wearable data, dietary intake, and psychological check-ins to monitor athlete well-being and generate a daily "Risk Score" for injury prevention. 

The system provides two distinct user interfaces:
* **Athlete App:** Allows athletes to sync wearable data, complete daily stress surveys, and analyze their meals using AI.
* **Coach Dashboard:** Allows coaches to manage their team, approve join requests, and monitor the real-time health and risk scores of their athletes.

## 🏗️ Repository Context & Architecture
**Please Note:** This repository is dedicated to my individual submission for the project. It contains:
1.  **The Android Client App** (Kotlin)
2.  **The Backend Server** (Python)

The full Machine Learning (ML) model used for advanced risk prediction was developed collaboratively and is maintained in a separate repository. For the purpose of this individual evaluation, the Python backend in this repository utilizes a **custom calculation algorithm (Mock API)**. This algorithm processes the real parameters sent from the Android app to generate and return the Risk Score, demonstrating the complete end-to-end functionality and system architecture.

## 🛠️ Tech Stack
* **Frontend:** Android, Kotlin, XML
* **Backend:** Python (Flask/FastAPI)
* **Database & Auth:** Firebase Firestore, Firebase Authentication
* **Device Integrations:** Google Health Connect API (for wearable sensor data like sleep, heart rate, and steps)
* **AI Integration:** Google Gemini API (Generative AI for nutritional meal analysis)
* **UI/Data Visualization:** MPAndroidChart, Material Design

## 🚀 Getting Started & Setup Instructions

To run this project locally, please follow these steps carefully, as sensitive API keys have been secured and excluded from version control.

### 1. Clone the Repository

bash
git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)



### 2. Gemini API Key Configuration (Action Required)

For security reasons, the Gemini API key used for the "AI Meal Analysis" feature is **not** included in this repository. To run the app and test the AI features, you must provide your own API key.

1. Generate a free API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Open the Android project in **Android Studio**.
3. Locate the `local.properties` file in the root directory of the project. (If it does not exist, create a new file named `local.properties` in the root folder).
4. Add the following line to the bottom of the file, replacing `YOUR_API_KEY` with your actual key (**without quotes**):

properties
GEMINI_API_KEY=YOUR_API_KEY



5. Click **Sync Project with Gradle Files** (the elephant icon). Android Studio will automatically generate the required `BuildConfig.GEMINI_API_KEY` to be used safely within the code.

### 3. Firebase Configuration

The project is connected to Firebase. Ensure that the `google-services.json` file is present in the `app/` directory. If you are a grader and require access to the Firebase testing environment, please contact me.

### 4. Running the App

* **Device:** It is highly recommended to test the app on a physical Android device rather than an emulator to fully experience the Health Connect API sync and the Camera features for meal analysis.
* **Health Connect:** Ensure the [Health Connect](https://play.google.com/store/apps/details?id=com.google.android.apps.healthdata) app is installed on the testing device. (If using an emulator, you can use the Health Connect Toolbox APK to mock wearable data).
* Build and run the project via Android Studio.



