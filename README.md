

# Fraud Detection in Mobile Money Transactions

## Project Overview

This project delves into the analysis and exploration of a synthetic dataset generated by the PaySim simulator, simulating mobile money transactions. The primary focus is to understand normal transaction patterns and effectively detect fraudulent behavior within the dataset.

### Project Statement

To address the scarcity of public datasets in the financial services domain, specifically in mobile money transactions, this project presents a synthetic dataset created using PaySim. The dataset emulates real financial transactions, including both normal operations and injected malicious behavior for evaluating fraud detection methods.

## Dataset Details

### Overview

The dataset originates from aggregated data taken from a month of financial logs of a mobile money service in an African country. This scaled-down version (1/4 of the original) was exclusively designed for Kaggle. Notably, transactions marked as fraud are canceled, rendering certain columns irrelevant for fraud detection (oldbalanceOrg, newbalanceOrig, oldbalanceDest, newbalanceDest).

### Key Features

- **Step:** Represents real-world time units where 1 step equals 1 hour, spanning 744 steps (30 days).
- **Type:** Transaction type - CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER.
- **Amount:** Transaction amount in local currency.
- **NameOrig:** Initiating customer of the transaction.
- **OldbalanceOrg & NewbalanceOrig:** Initial and new balances of the originating customer.
- **NameDest:** Recipient of the transaction.
- **OldbalanceDest & NewbalanceDest:** Initial and new balances of the recipient (excluding merchant accounts starting with M).
- **isFraud:** Flags transactions carried out by fraudulent agents attempting to deplete funds.
- **isFlaggedFraud:** Flags illegal attempts detecting transfers exceeding 200,000 in a single transaction.

## Objectives

This project aims to achieve the following:

- Analyze and comprehend normal mobile money transaction patterns.
- Implement and evaluate fraud detection methods on the synthetic dataset.
- Explore the impact of malicious behavior injection on fraud detection techniques.
- Investigate the effectiveness of flagged illegal attempts within the business model.

## Methodologies and Findings

Our meticulous exploration of the dataset involved comprehensive feature review and strategic metric selection. While initial attempts with Logistic Regression (LR) and Linear Discriminant Analysis (LDA) encountered challenges due to severe class imbalance and non-linear separability, ensemble methods, especially CatBoost, emerged as effective solutions.

Additionally, our outlier detection efforts revealed a mix of precision and recall challenges among various methodologies employed. Ensemble techniques effectively addressed class imbalance issues, while neural network models showcased promising potential.

The application of pre-trained models, like BERT, for fraud detection demonstrated promising results, emphasizing the potential of leveraging sophisticated pre-existing models.

These findings underscore the significance of fraud detection and highlight the critical role diverse methodologies play in addressing fraudulent activities within complex and imbalanced datasets.

