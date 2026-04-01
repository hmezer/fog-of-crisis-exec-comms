# The Fog of Crisis: Asymmetric Linguistic Shocks in Executive Communication

[cite_start]**Author:** Huseyin Mert Ezer [cite: 3]
[cite_start]**Institution:** TU Dortmund [cite: 4]
[cite_start]**Course:** Financial Econometrics WiSe25/26 [cite: 6]

## 📌 Project Overview
[cite_start]This repository contains the presentation and underlying Python notebook for a research project that investigates the impact of the March 2020 global economic shock on executive communication[cite: 30, 404]. [cite_start]Using Natural Language Processing (NLP) and econometric models on earnings calls from 2012 to 2024, the analysis explores a central question: Did the COVID-19 shock force executives into a uniform retreat behind complex language, or did it fracture communication styles along economic lines? [cite: 2, 31]

[cite_start]The linguistic complexity is measured using the **Gunning Fog Index**, which proxies the years of formal education required to understand a text[cite: 32].

## 🧪 Competing Hypotheses
The research tests two primary theories:
* [cite_start]**H1: Strategic Obfuscation:** Managers use complex language to hide bad news, predicting a massive spike in complexity among vulnerable sectors (e.g., Energy, Real Estate)[cite: 34, 35, 36, 38].
* [cite_start]**H2: Rational Complexity:** Linguistic complexity reflects a genuinely complex new operating environment, predicting a spike in resilient sectors (e.g., Tech, Finance) as they explain new paradigms[cite: 39, 40, 41, 42].

## 🛠️ Methodology
The analysis employs a multi-layered approach to quantify and explain the linguistic shock:

1. [cite_start]**Interrupted Time Series (ITS):** Treats the onset of COVID-19 as an exogenous interruption to isolate the crisis's impact from long-term natural language evolution[cite: 51, 52]. [cite_start]The core econometric model is: $Y_{t}=\beta_{0}+\beta_{1}T+\beta_{2}D_{t}+\beta_{3}P_{t}+\epsilon_{t}$[cite: 55].
2. [cite_start]**Unsupervised Structural Break Detection:** A piecewise linear regression algorithm iterates through every quarter to autonomously identify the optimal break date without a priori assumptions[cite: 96, 98, 99]. [cite_start]The algorithm minimizes the total error using: $t^{*}=arg~min_{t}(\sum_{i=1}^{t}(y_{i}-\hat{y}_{i})^{2}+\sum_{j=t+1}^{n}(y_{j}-\hat{y}_{j})^{2})$[cite: 105].
3. **Counterfactual Simulation (ARIMA):** Trains a model on pre-pandemic history (2012-2019) to simulate a "Business as Usual" scenario, testing if the 2020 spike was a statistically significant anomaly outside a 95% confidence interval[cite: 303, 305, 308].
4. **Machine Learning & NLP:** A Random Forest model evaluates the drivers of complexity, utilizing FinBERT for sentiment analysis[cite: 341, 345].

## 📊 Key Findings
* [cite_start]**Sentiment Drives Complexity:** Negative sentiment (identified via FinBERT) is the number one predictor of linguistic complexity at 17.6% importance, far outweighing market volatility[cite: 341, 342, 347].
* [cite_start]**Rejection of H1 (Obfuscation):** Struggling firms in vulnerable sectors did not use the pandemic to hide behind complex language, showing no structural break in 2020[cite: 391, 393, 394].
* [cite_start]**Support for H2 (Rationality):** The 2020 structural break was exclusive to resilient sectors (the Digital Economy) articulating new operating paradigms[cite: 396, 398, 399].
* [cite_start]**Precautionary Complexity:** Residual analysis revealed systematic underestimation in the resilient sectors[cite: 400]. [cite_start]Executives used complex language not to deceive, but to buy flexibility and hedge against future uncertainty while rewriting post-pandemic market rules[cite: 402, 403].

## 📂 Repository Structure
* `notebooks/` - Contains the Python Jupyter Notebook with the data processing, NLP extraction, ITS, ARIMA, and Random Forest implementations.
* `presentation/` - Contains the final slide deck summarizing the findings (`ezer-huseyin_mert-finecon2526.pdf`).
* `README.md` - Project overview and conclusions.
