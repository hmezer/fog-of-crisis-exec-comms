# The Fog of Crisis: Asymmetric Linguistic Shocks in Executive Communication

**Author:** Huseyin Mert Ezer 
**Institution:** TU Dortmund 
**Course:** Financial Econometrics WiSe25/26 

## 📌 Project Overview
This repository contains the presentation and underlying Python notebook for a research project that investigates the impact of the March 2020 global economic shock on executive communication. Using Natural Language Processing (NLP) and econometric models on earnings calls from 2012 to 2024, the analysis explores a central question: Did the COVID-19 shock force executives into a uniform retreat behind complex language, or did it fracture communication styles along economic lines? 

The linguistic complexity is measured using the **Gunning Fog Index**, which proxies the years of formal education required to understand a text.

## 🧪 Competing Hypotheses
The research tests two primary theories:
* **H1: Strategic Obfuscation:** Managers use complex language to hide bad news, predicting a massive spike in complexity among vulnerable sectors (e.g., Energy, Real Estate).
* **H2: Rational Complexity:** Linguistic complexity reflects a genuinely complex new operating environment, predicting a spike in resilient sectors (e.g., Tech, Finance) as they explain new paradigms.

## 🛠️ Methodology
The analysis employs a multi-layered approach to quantify and explain the linguistic shock:

1. **Interrupted Time Series (ITS):** Treats the onset of COVID-19 as an exogenous interruption to isolate the crisis's impact from long-term natural language evolution. The core econometric model is: $Y_{t}=\beta_{0}+\beta_{1}T+\beta_{2}D_{t}+\beta_{3}P_{t}+\epsilon_{t}$
2. **Unsupervised Structural Break Detection:** A piecewise linear regression algorithm iterates through every quarter to autonomously identify the optimal break date without a priori assumptions. The algorithm minimizes the total error using:

$$t^{*}=arg~min_{t}(\sum_{i=1}^{t}(y_{i}-\hat{y}_{i})^{2}+\sum_{j=t+1}^{n}(y_{j}-\hat{y}_{j})^{2})$$

3. **Counterfactual Simulation (ARIMA):** Trains a model on pre-pandemic history (2012-2019) to simulate a "Business as Usual" scenario, testing if the 2020 spike was a statistically significant anomaly outside a 95% confidence interval.
4. **Machine Learning & NLP:** A Random Forest model evaluates the drivers of complexity, utilizing FinBERT for sentiment analysis.

## 📊 Key Findings
* **Sentiment Drives Complexity:** Negative sentiment (identified via FinBERT) is the number one predictor of linguistic complexity at 17.6% importance, far outweighing market volatility.
* **Rejection of H1 (Obfuscation):** Struggling firms in vulnerable sectors did not use the pandemic to hide behind complex language, showing no structural break in 2020.
* **Support for H2 (Rationality):** The 2020 structural break was exclusive to resilient sectors (the Digital Economy) articulating new operating paradigms.
* **Precautionary Complexity:** Residual analysis revealed systematic underestimation in the resilient sectors. Executives used complex language not to deceive, but to buy flexibility and hedge against future uncertainty while rewriting post-pandemic market rules.

## 📂 Repository Structure
* `notebooks/` - Contains the Python Jupyter Notebook with the data processing, NLP extraction, ITS, ARIMA, and Random Forest implementations.
* `presentation/` - Contains the final slide deck summarizing the findings (`ezer-huseyin_mert-finecon2526.pdf`).
* `README.md` - Project overview and conclusions.
