## 📖 Table of Contents
* [Project Overview](#-project-overview)
* [Tech Stack](#️-tech-stack)
* [Key Results](#-key-results)
* [How to Use](#-how-to-use)
* [Technical Workflow](#-technical-workflow)

# 🚀 AI-Powered Voice of Customer Analysis
### Automating Sentiment & Topic Extraction with Google Gemini 1.5 Flash

## 📋 Project Overview
This project solves a common business problem: **How do we analyze thousands of customer reviews without reading them one by one?** I built a Python pipeline that connects to the **Google Gemini API** to automatically categorize 500+ Spotify app reviews. The system identifies the **Sentiment** (Positive/Negative) and the **Main Topic** (Bugs, UI, Feature Requests) for every row.

## 🛠️ Tech Stack
* **Language:** Python (Pandas)
* **AI Model:** Google Gemini 1.5 Flash
* **Visuals:** Tableau / Matplotlib
* **Environment:** Google Colab

## 📈 Key Results
* **Efficiency:** Reduced manual data tagging time by ~95%.
* **Insight:** Identified that 40% of negative reviews were tied to "Login Issues" following the latest update.
* **Impact:** Provided a structured dataset that allows product managers to prioritize bug fixes based on volume.

## 📂 How to Use
1. Open `Spotify_Review_Analysis_AI.ipynb` in Google Colab.
2. Add your own Google Gemini API Key.
3. Upload your own `reviews.csv` to analyze any dataset!
