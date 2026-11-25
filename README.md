# SemProject_MLEngine

ICS 3202 Semester Project, Deliverable 3: ML engine for CharityLink.

CharityLink is a donation transparency platform for Kenya. Its ML engine flags fund allocations that look potentially misallocated, using unsupervised anomaly detection (Isolation Forest).

## Files

- `Final_ML_Engine.ipynb`: the single compiled notebook for code review. It covers data loading, cleaning and exploration, feature engineering, the Isolation Forest model, validation and results.
- `IsolationForest_Base.ipynb`: the base model.
- `Dataset_Exploration.ipynb`: early exploration of the dataset.

## Approach

- Dataset: Kiva crowdfunding data from Kaggle (about 671,000 loans). It has no fraud labels, so we used unsupervised learning.
- Model: Isolation Forest with 100 trees and contamination = 0.05, so the top 5% of loans are flagged.
- Validation: tested four contamination values, compared flags with a "funded below 90%" rule, and inspected the most anomalous loans manually.

## Running the notebook

Open `Final_ML_Engine.ipynb` in Google Colab and choose Runtime → Run all. The Kaggle dataset zip must be available in the Colab session.

## Team

Oscar Tanui, Trevor Yano, David Mungai
