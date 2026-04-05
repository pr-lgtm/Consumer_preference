
# Consumer_preference
A Research Work conducted in collaboration with PANACEA, The Statistics Society of Ram Lal Anand College (University of Delhi). The Research is conducted to study the user(consumer's) preference in between the Local Shops and the Quick Commerce Apps considering the various key factors and to analyze the consumer behavior in terms of frequency,time.

# Retail Choice Predictor

## Overview

**Retail Choice Predictor** is an interactive Python program that predicts whether a user is more likely to choose **Quick Commerce apps** (like Blinkit, Zepto) or **local retail/kirana shops** for daily purchases.  

The prediction is based on **survey data collected by Panacea**, and the program also provides an explanation showing which factors influenced the decision.

The program uses **logistic regression** — a statistical model — to learn patterns from the survey and generate interpretable predictions. This approach ensures that predictions are **grounded in actual consumer behavior**, not just arbitrary guesses.

---

## Features

1. **Interactive survey input:**  
   Users answer questions about age, occupation, shopping habits, convenience, trust, cost, and delivery preferences.

2. **Statistical prediction:**  
   Logistic Regression with **class balancing** ensures that predictions are not biased toward the majority class (e.g., Local Shops) in the survey.

3. **Explanation of prediction:**  
   Each predicted outcome is accompanied by a **reason**, showing which factors contributed most to the decision. This is calculated using **coefficients of the trained logistic regression model** applied to the user’s input.

4. **Probability output:**  
   Displays the **likelihood (%) of choosing Quick Commerce vs Local Shop**.

5. **CSV-driven model:**  
   The model learns from **survey data (`responses of March.csv`)**, making predictions **statistically grounded** and research-based.

---

## Statistical Concepts Used

- **Logistic Regression:**  
  A statistical method for modeling the probability of a binary outcome. Here, it predicts the probability of choosing Quick Commerce (`1`) vs Local Shop (`0`).

- **Class Weight Balancing:**  
  The survey may have more respondents preferring Local Shops. Setting `class_weight="balanced"` ensures that the model **gives equal importance to both classes** during training.

- **One-hot Encoding:**  
  Categorical survey responses (like “Yes, frequently” or “Student”) are converted into numerical features suitable for logistic regression.

- **Feature Contribution for Explanation:**  
  Each user input feature is multiplied by its logistic regression coefficient to quantify **how strongly it influenced the prediction**. This provides a transparent explanation for the output.

- **Probability Estimation:**  
  The logistic regression model outputs probabilities using the sigmoid function, showing **confidence in the prediction**.

---

## Usage

1. Place the survey CSV file `responses of March.csv` in the same folder as the program.  
2. Run the program:

```bash
python logistic_statistical_reason.py
