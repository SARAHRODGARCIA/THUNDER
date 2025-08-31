# THUNDER ⚡
THUNDER is a machine learning pipeline designed to detect rare and time-sensitive frauds in transactional datasets. It combines advanced techniques such as label-specific oversampling (SMOTENC) and threshold tuning to improve recall for rare fraud types while maintaining reasonable precision.

Key Features:

Multi-label fraud detection: Detects multiple types of fraud in a single transaction, including chargeback_fraud, fraud_upper_fence, fraud_unusual_hour, and fraud_fast_sequence.

Label-specific oversampling: Handles class imbalance by applying SMOTENC separately to each fraud type, improving detection of rare events.

Threshold optimization: Adjusts decision thresholds for each fraud type to maximize recall without drastically reducing precision.

Flexible preprocessing: Encodes categorical features and supports numerical features like transaction amount.

Extensible: Can incorporate new features (e.g., time-based or sequence features) to improve detection of extremely rare or time-dependent frauds.

Results with XGBoost:

Chargeback fraud: Recall dramatically increased from 0.36 → 0.94.

Fraud upper fence: Achieved F1 ≈ 0.93, demonstrating high precision and recall for moderately frequent frauds.

Fraud unusual hour & fast sequence: Improved detection with threshold tuning, though extremely rare or temporal frauds remain challenging.

Identified limitations for extremely rare or temporal frauds, highlighting the need for further feature engineering.

Usage:

Load your transactional dataset.

Preprocess categorical and numerical features.

Run the THUNDER pipeline to generate a balanced training dataset.

Train multi-label classifiers (e.g., Random Forest, XGBoost) on the processed dataset.

Evaluate using macro/micro precision, recall, and F1-score.

💡 Summary: THUNDER is ideal for teams working with transactional or payment data who want to efficiently detect rare frauds, understand the trade-offs between recall and precision, and improve model performance with targeted feature engineering.
