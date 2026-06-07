# IoT-Based-Edge-Ensemble-Model-for-Zoonotic-Disease-Prediction
## About the Project
Zoonotic diseases — 
infectious diseases that spread from animals to humans (e.g., Rabies, SARS, Ebola, Zika, Monkeypox, Nipah, Dengue) — pose a severe health risk, particularly in rural areas with limited healthcare infrastructure. Traditional monitoring systems are costly, slow, and inefficient.
This project proposes a low-cost, IoT-based edge computing system that collects real-time health and environmental data, and uses an ensemble machine learning model (XGBoost + STL Decomposition) to predict zoonotic disease outbreaks at an early stage.

## Methodology

1. Data Collection — Multiple real-world datasets covering COVID-19, Dengue, Monkeypox, Nipah, Ebola, and livestock disease records across India.
2. Preprocessing — Merging all CSV/Excel files, handling missing values (median/mode imputation), dropping duplicate rows, one-hot encoding, and removing columns with >50% missing data.
3. STL Decomposition — Time-series decomposition into trend, seasonal, and residual components to improve feature quality.
4. Feature Engineering — Lag features (lag1, lag2, lag3) and rolling mean (window=3) added to capture temporal patterns.
5. Model Training — XGBoost Regressor trained with StandardScaler normalization (90/10 train-test split).
6. Evaluation — Model assessed using R² Score.

# Start → Data Collection → Preprocessing → Build & Train Model → Evaluate & Compare → End

## Datasets Used
The datasets.zip contains multiple real-world disease datasets including:

1. COVID-19 case data (India — state-wise, district-wise, day-wise)
2. Dengue cases in India
3. Monkeypox daily confirmed cases
4. Nipah virus data (Bangladesh 2026)
5. Ebola outbreak records
6. Livestock disease incidence data (India)
7. COVID-liver, vaccine efficacy, and more

## How to Run

1. Download ClgProject2026.ipynb and open it in Google Colab.
2. Run all cells in order.
3. When prompted, upload datasets.zip.
4. Wait for the program to complete — the output (model accuracy) will be displayed at the end.
