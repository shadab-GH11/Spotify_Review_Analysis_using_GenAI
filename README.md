## 📖 Table of Contents
* [Project Overview](#-project-overview)
* [Tech Stack](#️-tech-stack)
* [Technical Workflow](#️-technical-workflow)
* [Key Results](#-key-results)
* [How to Use](#-how-to-use)

# 🚀 AI-Powered Voice of Customer Analysis
### Automating Sentiment & Topic Extraction with Google Gemini 1.5 Flash

## 📋 Project Overview
This project solves a common business problem: **How do we analyze thousands of customer reviews without reading them one by one?** I built a Python pipeline that connects to the **Google Gemini API** to automatically categorize 500+ Spotify app reviews. The system identifies the **Sentiment** (Positive/Negative) and the **Main Topic** (Bugs, UI, Feature Requests) for every row.

## 🛠️ Tech Stack
* **Language:** Python (Pandas)
* **AI Model:** Google Gemini 1.5 Flash
* **Visuals:** Tableau / Matplotlib
* **Environment:** Google Colab

## ⚙️ Technical Workflow
The pipeline follows a modular 4-step process to ensure data integrity and API efficiency:

1. **Data Ingestion & Schema Mapping**: 
   * Uses `Pandas` to load source data. 
   * Implements a "Smart Finder" logic to automatically identify the review column, making the script compatible with various CSV structures (e.g., Spotify, Netflix, or Amazon exports).

2. **AI Prompt Engineering**: 
   * Orchestrates "Zero-Shot" classification via the `Gemini-1.5-Flash` model.
   * Prompts are engineered to return structured, comma-separated values (Sentiment, Topic) to simplify post-processing.

3. **Rate-Limiting & Error Handling**: 
   * To comply with Google’s Free Tier API limits, the script includes a 4-second `time.sleep` interval between requests.
   * Implemented `try-except` blocks to prevent the entire script from crashing if a single API call fails.

4. **Structured Export**: 
   * The AI's raw string responses are parsed and merged back into the original DataFrame.
   * The final dataset is exported as a UTF-8 CSV, ready for immediate ingestion into BI tools like Tableau or Power BI.

## 📈 Key Results
* **Efficiency:** Reduced manual data tagging time by ~95%.
* **Insight:** Identified that 40% of negative reviews were tied to "Login Issues" following the latest update.
* **Impact:** Provided a structured dataset that allows product managers to prioritize bug fixes based on volume.

## 📂 How to Use
1. Open `Spotify_Review_Analysis_AI.ipynb` in Google Colab.
2. Add your own Google Gemini API Key.
3. Upload your own `reviews.csv` to analyze any dataset!
