AI Use & Reproducibility Log

Tool / Model & Version:
ChatGPT (GPT-5, OpenAI, 2025) – used for documentation drafting, proposal writing, and code review assistance.
Python environment: scikit-learn (1.5+), pandas (2.2+), matplotlib (3.9+), seaborn (0.13+), NumPy (1.26+).

What I Asked For:

Generate clean, reproducible code for disease classification using Logistic Regression and Random Forest.

Create visualizations (confusion matrices, feature importance, distribution plots).

Write and format progress report sections and summaries in markdown and academic style.

Snippet of Prompt(s):

“Build me a well-commented, labeled Jupyter Notebook for symptom-based disease classification.”
“Add confusion matrix and feature importance visualization.”
“Rewrite proposal and draft report in a concise academic tone.”

What I Changed Before Committing:

Removed XGBoost and SHAP code (reserved for future work).

Verified that all missing-value imputation and scaling steps matched the dataset.

Added Random Seed = 42 for reproducibility.

Adjusted plot labels and feature-importance titles for clarity.

How I Verified Correctness (Tests / Sample Data):

Tested the full pipeline on the Training 2.csv dataset.

Verified shape consistency between training and test data after imputation.

Checked confusion matrices for class alignment.

Compared Logistic Regression and Random Forest accuracy / F1 scores.

Ensured reproducible results after re-running all notebook cells.
