# Data-Engineering-Supplement-Experiments_Pipleine
# Experiments Data ETL Pipeline

This repository contains an ETL (Extract, Transform, Load) pipeline for the 1001-Experiments project. The pipeline merges data from four different CSV files into a single, clean DataFrame providing a comprehensive view of each user's health metrics, supplement usage, and demographic profile.

## 📁 Input Datasets

The pipeline uses the following four datasets:

| File Name               | Description |
|------------------------|-------------|
| `user_health_data.csv` | Daily health metrics and data from wearables (per user per day). |
| `supplement_usage.csv` | Records of supplement intake per user per day. |
| `experiments.csv`      | Metadata about experiments and treatments. |
| `user_profiles.csv`    | Demographic and contact information for each user. |

## 🛠️ Features

- Cleans and normalizes all input data.
- Converts dosage to grams uniformly.
- Categorizes users into age groups.
- Formats date fields to `YYYY-MM-DD`.
- Merges all datasets using proper foreign keys.
- Returns a final DataFrame suitable for analysis or export.

## 🚀 How to Use

Use the following function to run the full ETL pipeline:

```python
from your_module_name import merge_all_data

df = merge_all_data('user_health_data.csv', 'supplement_usage.csv', 'experiments.csv', 'user_profiles.csv')
