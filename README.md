
# NLP Disaster Tweets - Kaggle Mini Project

This repository contains my work for the **Week 4 Peer-Graded Assignment** of the Coursera NLP course, based on the [Kaggle competition: Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started).

## Project Overview
The goal is to classify tweets as describing a real disaster (1) or not (0), using both traditional ML and deep learning approaches.

## Project Steps
1. **Data loading and inspection** – Import dataset and check structure.
2. **EDA and preprocessing** – Clean text, remove noise, normalize features.
3. **Feature extraction** – Apply TF-IDF and GloVe word embeddings.
4. **Model building and training** – Implement TF-IDF + Logistic Regression, BiLSTM, TextCNN, and a simple blend.
5. **Evaluation and tuning** – Measure performance with accuracy, F1, precision, recall, and Kaggle leaderboard.
6. **Submission** – Generate `submission.csv` and upload to Kaggle.

## Key Results
| Model | Public LB Score |
|-------|-----------------|
| BiLSTM + GloVe | **0.79803** |
| TF-IDF + LR | 0.79650 |
| Blend (BiLSTM+TextCNN+LR) | 0.79528 |

BiLSTM outperformed other models in Kaggle public leaderboard, while TF-IDF + LR remained competitive with lower computational cost.

## Error Case Examples
| Tweet | True | Pred | Likely Reason |
|-------|------|------|---------------|
| "Storm is coming! Can’t wait for the game tonight!" | 0 | 1 | “storm” keyword misinterpreted as disaster. |
| "Evacuating now with the kids" | 1 | 0 | Short text without explicit keywords. |

## Conclusion
- **Best Model:** BiLSTM + GloVe for deployment.
- **Baseline:** TF-IDF + LR offers stable, efficient performance.
- **Future Work:** Try transformer-based models (BERT, RoBERTa), domain-specific embeddings, and advanced ensemble methods.

## Repository Contents
- `week4_NLP_disaster_tweets_classification.ipynb` – Full workflow.
- `submission.csv` – Final Kaggle submission.
- `week4_kaggle_public_score_disaster_tweets.png` – Leaderboard screenshot.
- `README.md` – Project summary.
