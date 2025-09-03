# Login Anomaly Detection

This project demonstrates an **unsupervised anomaly detection pipeline** for simulated user login activity, inspired by real-world fraud and abuse detection scenarios in cloud security.

## Project Overview
- Simulated realistic login data for 500 users across multiple regions.
- Injected “fraud-like” anomalies:
  - Impossible travel (unrealistic geo-hops).
  - Sudden new device usage.
  - Brute-force failed login bursts.
  - Odd-hour access outside normal behavior.
- Engineered security-focused features (distance, hop speed, device novelty, failed attempts, login hour).
- Applied **IsolationForest** to detect anomalies without labels.
- Evaluated results with precision, recall, F1 score, confusion matrix, and daily anomaly trends.

## Results
- Precision/Recall metrics reported for anomaly detection.
- Top anomalous users and events flagged.
- Timeline visualization showing actual vs. flagged anomalies.
- Feature importance analysis via permutation tests.

## Why It Matters
Fraud and abuse often appear as **deviations from normal behavior**.  
This demo shows how unsupervised learning can uncover suspicious logins at scale — the same principles that underpin large-scale fraud detection systems in enterprise cloud environments.

## Tech Stack
- Python, Pandas, NumPy
- scikit-learn (IsolationForest, evaluation metrics)
- Matplotlib (visualizations)
- Google Colab (notebook execution)

## How to Run
1. Open the notebook in Google Colab.  
2. Run cells in order to generate the dataset, inject anomalies, engineer features, and train/evaluate the model.  
3. (Optional) Experiment with other anomaly detection models such as One-Class SVM or Autoencoders.

## Next Steps
- Add streaming inference endpoint (FastAPI) for real-time scoring.  
- Monitor concept drift and update models dynamically.  
- Enrich with IP intelligence, device fingerprinting, and network metadata for more robust fraud detection.  

---

