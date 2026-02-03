**Sarcasm Detection in German Dialects**


This repository contains a fine-tuned DistilBERT model specialized in identifying irony and sarcasm across the D-A-CH region (Germany, Austria, and Switzerland). By leveraging a perspectivist approach, we analyze how regional linguistic markers—such as Austrian "ur" or Swiss "merci"—influence automated sentiment analysis and contribute to model bias.



The code output, along with the model and complete repository, is available at: https://ucloud.univie.ac.at/index.php/s/9xZPwqzH2jcTcPS

*01. Project Overview*


Objective: Fine-tune a Transformer architecture to detect figurative language while quantifying regional dialect bias.


Core Problem: Most German NLP models are trained on "Hochdeutsch" (Standard German), leading to a "Dialect Gap" where regional enthusiasm is frequently misinterpreted as sarcasm.


Frameworks: Built using transformers, PyTorch, and SHAP for model interpretability.

*02. Data Source: MultiPICo*


We utilize the Multilingual Perspectivist Irony Corpus (MultiPICo).

Content: 18,778 conversation pairs from Twitter and Reddit.

Perspectivism: Includes disaggregated demographic metadata (age, gender, nationality) of annotators.

Labels: Supports both Hard Labels (majority agreement) and Soft Labels (probability distributions) to reflect human disagreement.

*03. Technical Workflow*


Data Categorization: Partitioning datasets by regional variety (DE, AT, CH).

Optimized Training: Fine-tuning with a Weighted Loss Trainer to handle class imbalance.

Performance Checkpoint: Selection of the best model state (e.g., Step 700) based on F1-score optimization.


Interpretability: Using SHAP Waterfall plots to visualize feature importance and identify linguistic triggers like "ja" or "ur"
