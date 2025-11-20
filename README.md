# UEFA Champions League (UCL) Winner Prediction System

This project utilizes Machine Learning to predict UEFA Champions League (UCL) winners based on group stage performance statistics. It analyzes historical data to identify key performance indicators and forecasts potential champions.

# 📋 Project Overview

The UEFA Champions League Winner Prediction System leverages historical group stage data and advanced machine learning algorithms to forecast potential tournament winners. By analyzing team performance metrics from 1992 to the present, this system provides data-driven predictions for one of football's most prestigious competitions.

## 🗂️ Project Structure

```
UCL-Winner-Prediction/
│
├── UCL_Winner_Prediction.ipynb  # Main Jupyter notebook with code and analysis
├── ucl_stats.csv                # Dataset containing historical UCL statistics
├── winners-prev.png             # Image of past UCL winners
├── 2024_winner.avif             # Image of 2024 winner
├── 2023_winner.jpeg             # Image of 2023 winner
├── 2022_winner.webp             # Image of 2022 winner
├── 2021_winner.jpg              # Image of 2021 winner
└── README.md                    # Project documentation
```

## 🎯 Features

- **Data Collection & Cleaning**: Aggregation of UCL group stage data from 1992 onwards, handling missing values and inconsistencies.
- **Feature Engineering**: Creation of advanced metrics like Win_Ratio, Goal_Efficiency, and Dominance_Score to better represent team strength.
- **Exploratory Data Analysis (EDA)**: Visualizing correlations between features and the target variable (winning the championship) using heatmaps, histograms, and scatter plots.
- **Machine Learning Models**: Implementation and comparison of **Random Forest** and **XGBoost** classifiers.
- **Performance Metrics**: Evaluation of model accuracy and reliability.
- **Visualizations**: Interactive charts and graphs for data insights.
- **Imbalance Handling**: Addressing the class imbalance (few champions vs. many non-champions) using techniques like **SMOTE** and **class weighting**.
- **Prediction System**: Generating win probabilities for teams in recent seasons (2021-2024) to test model accuracy against real-world outcomes.

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required Python libraries (pandas, numpy, scikit-learn, matplotlib, seaborn, scikit-learn etc.)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Nazmul1005/UEFA-Champions-League-UCL-Winner-Prediction-System.git
cd UCL-Winner-Prediction-System
```

2. Install required dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook UCL_Winner_Prediction.ipynb
```

## 📊 Dataset

The project uses UEFA Champions League group stage statistics including:
- Team performance metrics
- Match results
- Goals scored and conceded
- Points accumulated
- Historical tournament outcomes

## 🤖 Machine Learning Approach

The prediction system employs various machine learning techniques:
- Data preprocessing and feature engineering
- Model training and validation
- Performance evaluation
- Prediction generation

## 📈 Results

Prediction results and model performance metrics can be found in the bottom of the notebook.

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Jupyter Notebook**: Interactive development environment
- **Pandas & NumPy**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms
- **Matplotlib & Seaborn**: Data visualization

### Ensemble Learning Approach

```
┌─────────────────────────────────────────────────────┐
│              INPUT: Group Stage Stats               │
│  (Wins, Draws, Losses, Goals, Points, etc.)        │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│            FEATURE ENGINEERING                      │
│  - Win Ratio          - Goal Efficiency             │
│  - Loss Ratio         - Defensive Strength          │
│  - Goals Per Match    - Dominance Score             │
│  - Points Per Match   - Clean Sheet Potential       │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│                   ENSEMBLE MODELS                   │
│            ┌──────────┐  ┌──────────┐               │
│            │ Random   │  │ XGBoost  │               │
│            │ Forest   │  │  Model   │               │
│            └────┬─────┘  └────┬─────┘               │
│                 │             │                     │
│                 └─────────────┴                     │
│                        │                            │
│                        ▼                            │
│          ┌──────────────────────┐                   │
│          │  Choosing Best MOdel │                   │
│          │                      │                   │
│          └──────────────────────┘                   │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│              OUTPUT: Win Probabilities              │
│         (Top 16 Teams Ranked by Likelihood)         │
└─────────────────────────────────────────────────────┘
```


### Test Set Validation (2021-2024)

| Season  | Predicted Winner | Actual Winner   | Rank | Probability | Result |
|---------|------------------|-----------------|------|-------------|--------|
| 2020-21 | Chelsea          | Chelsea         | 1    | 78.87%      | ✅     |
| 2021-22 | Liverpool        | Real Madrid     | 4    | 17.83%      | ❌     |
| 2022-23 | Manchester City  | Manchester City | 1    | 78.87%      | ✅     |
| 2023-24 | Atlético Madrid  | Real Madrid     | 2    | 54.29%      | ❌     |

*Overall Test Accuracy:* 50% (2/4 correct predictions)

*Average Rank of Actual Winners:* 2

---
