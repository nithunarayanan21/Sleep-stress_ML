# Sleep-stress_ML
# Sleep, Health & Lifestyle: Predicting Stress Levels with ML

This project analyzes the [Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset) to explore how sleep quality, sleep duration, physical activity, BMI, heart rate, and other lifestyle factors relate to stress levels, and builds machine learning models to predict stress level from these indicators.

## Authors
- Nithyasree N
- Sujith Ram V

## Contents
- `Sleep__Health_and_lifestyle.ipynb` — full analysis notebook (EDA, preprocessing, model training, evaluation)
- `Analyzing_the_Impact_of_Sleep_and_Lifestyle_Factors.pdf` — written report with visualizations and findings
- `Sleep_health_and_lifestyle_dataset.csv` — dataset (place here before running; see note below)

## Project Overview
- **Dataset:** 374 records, 13 attributes (demographics, sleep metrics, physical activity, cardiovascular indicators, stress level)
- **Target variable:** Stress Level
- **Approach:** Exploratory data analysis → preprocessing (label encoding, train/test split) → model training → comparison

## Models & Results

| Model | Accuracy |
|---|---|
| Logistic Regression | 86.67% |
| Decision Tree | 97.33% |
| Random Forest | 100.00% |

**Note:** The Random Forest's 100% accuracy is likely a result of the dataset being small (374 rows) and synthetic/clean rather than a signal the model generalizes perfectly to real-world data — see Limitations below and in the full report.

## Key Findings
- Sleep Duration and Quality of Sleep were the strongest predictors of stress level.
- Heart Rate showed a meaningful positive correlation with stress.
- Physical activity level and daily steps had only a weak direct relationship with stress in this dataset.

## Running the Notebook

### Option 1: Google Colab (easiest)
1. Open the notebook in Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<your-username>/sleep-stress-ml/blob/main/Sleep__Health_and_lifestyle.ipynb)
2. Run the cells top to bottom. The first cell (`files.upload()`) will prompt you to upload `Sleep_health_and_lifestyle_dataset.csv` from your computer — select it and continue.
   - Alternatively, since the CSV is already in this repo, you can skip the upload cell and instead run:
```python
     import pandas as pd
     df = pd.read_csv("Sleep_health_and_lifestyle_dataset.csv")
```
     after cloning the repo into your Colab environment.

### Option 2: Run Locally with Jupyter
1. Clone the repo (the CSV is already included, so no separate download needed).
2. Skip or delete the first cell (`files.upload()`), since that's Colab-specific.
3. Install dependencies:
```bash
   pip install -r requirements.txt
```
4. Launch Jupyter:
```bash
   jupyter notebook "Sleep__Health_and_lifestyle.ipynb"
```

## Limitations
- Small dataset (374 records) limits generalizability.
- Dataset may be synthetic and not fully representative of real-world populations.
- Stress is influenced by many factors (psychological, social, environmental) not captured here.

## Future Work
- Test on larger, real-world healthcare datasets
- Add cross-validation and additional evaluation metrics (precision/recall per class)
- Incorporate wearable sensor / mental health survey data
- Explore deep learning approaches

## References
- Dataset: [Kaggle - Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset)
