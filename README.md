Interpretable Credit Risk Modeling using XGBoost, SHAP and LIME
Project purpose This project builds a credit risk classifier and provides interpretable explanations that are suitable for model validation and stakeholder reporting. The deliverables include trained model artifacts, evaluation metrics, global feature interpretation, local explanations for five representative loan applications, a comparative analysis of SHAP and LIME, and a one page executive summary.

Project files

credit_risk.csv Input dataset. The script expects a target column named id where 0 means accepted and 1 means rejected.
model.py Full reproducible script. Running this script produces all deliverables and saves them to the output folder.
output/ Generated artifacts when model.py is run:
xgb_model.joblib
tuning_results.json
cv_train_folds.json
test_metrics.json
test_classification.json
xgb_feature_importance.png
shap_summary.png
global_feature_importance.csv
case_1_shap_contributions.csv ... case_5_shap_contributions.csv
case_1_transcription.txt ... case_5_transcription.txt
case_1_lime.html ... case_5_lime.html
comparative_shap_vs_lime.txt
executive_summary.txt
deliverables_mapping.txt
Environment and installation Create a Python environment and install dependencies. Example: python -m venv venv source venv/bin/activate # on Windows use venv\Scripts\activate pip install -U pip pip install xgboost shap lime scikit-learn pandas matplotlib joblib scipy

Run the project

Place your dataset in the project folder and name it credit_risk.csv or edit model.py to change DATA_FILE.
Run: python model.py
Check the output folder for plots, JSON metrics, and local explanation files.
Reproducibility and notes

The random seed is fixed at 42 to ensure reproducible results for tuning and splits.
The script uses RandomizedSearchCV for hyperparameter tuning with a small search budget so it completes in reasonable time while improving baseline performance.
SHAP summary plot is saved as a PNG file. LIME explanations are saved as HTML files that can be opened in a browser.
How this meets the evaluator requirements

Task 1 Model development and tuning: Provided. The tuned model and tuning results are saved.
Task 2 Global feature importance visualizations: Provided. xgb_feature_importance.png and shap_summary.png and global_feature_importance.csv.
Task 3 Local explanations: Provided for five cases. Each case has SHAP contribution CSV, a SHAP force plot image when possible, a LIME HTML file, and a transcription summary text file.
Task 4 Comparative analysis of SHAP vs LIME: Provided as comparative_shap_vs_lime.txt.
Task 5 Executive summary: Provided as executive_summary.txt.
Report and submission tips

Upload the entire output folder for evaluation. Include the executive_summary.txt as the one page executive summary deliverable.
For the textual report deliverable include:
The test metrics (test_metrics.json)
The global_feature_importance.csv and shap_summary.png
The five local case transcriptions and LIME HTML files
The comparative_shap_vs_lime.txt and executive_summary.txt
Contact If you would like a Jupyter notebook version, or a PDF of the executive summary and the comparative analysis formatted for submission, ask and I will produce them.

End of README.
