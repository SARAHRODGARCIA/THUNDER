# THUNDER
THUNDER is a machine learning pipeline for multi-label fraud detection in transactional data. It uses label-specific oversampling (SMOTENC) and threshold tuning to improve recall for rare frauds while maintaining precision, and supports easy feature expansion for time-dependent or rare fraud types.

THUNDER – Fraud Detection in Transactional Data

THUNDER is a machine learning pipeline designed to detect rare and time-sensitive frauds in transactional datasets. It combines advanced techniques such as label-specific oversampling (SMOTENC) and threshold tuning to improve recall for rare fraud types while maintaining reasonable precision.

Key Features:

Multi-label fraud detection: Detects multiple types of fraud in a single transaction, including chargeback_fraud, fraud_upper_fence, fraud_unusual_hour, and fraud_fast_sequence.

Label-specific oversampling: Handles class imbalance by applying SMOTENC separately to each fraud type, improving detection of rare events.

Threshold optimization: Adjusts decision thresholds for each fraud type to maximize recall without drastically reducing precision.

Flexible preprocessing: Encodes categorical features and supports numerical features like transaction amount.

Extensible: Can incorporate new features (e.g., time-based or sequence features) for improving detection of extremely rare or time-dependent frauds.

Results:

Dramatically increased recall for critical fraud types (chargeback_fraud) from 0.36 → 0.94.

Achieved high F1-scores for moderately frequent frauds (fraud_upper_fence F1 ≈ 0.93).

Identified limitations for extremely rare or temporal frauds, highlighting the need for further feature engineering.

Usage:

Load your transactional dataset.

Preprocess categorical and numerical features.

Run THUNDER pipeline to generate a balanced training dataset.

Train multi-label classifiers (e.g., Random Forest, Gradient Boosting) on the processed dataset.

Evaluate using macro/micro precision, recall, and F1-score.

💡 Summary:
THUNDER is ideal for teams working with transactional or payment data who want to detect rare frauds efficiently, understand the trade-offs between recall and precision, and improve model performance with targeted feature engineering.
