# Parkinson's Disease Detection Using Machine Learning

## Overview
An educational supervised machine-learning project that explores classification using biomedical voice measurements from the [UCI Parkinson's Disease dataset](https://archive.ics.uci.edu/dataset/174/parkinsons).

The notebook compares four classifiers: Support Vector Machine (SVM), K-Nearest Neighbours (KNN), Decision Tree, and Random Forest.

## Dataset
- Source: UCI Machine Learning Repository — Parkinson's Disease
- Records: 195
- Input features: 22 biomedical voice measurements
- Target: `status` (`1` = Parkinson's group in this dataset; `0` = control group)

The notebook downloads `parkinsons.data` directly from the UCI repository, so an internet connection is required when running the data-loading cell.

## Methods
1. Load and inspect the dataset.
2. Separate the input features and target label; remove the participant/file identifier.
3. Split the data into training and test sets using a stratified 75:25 split.
4. Train and compare SVM, KNN, Decision Tree, and Random Forest classifiers.
5. Evaluate the models using accuracy, precision, recall, F1-score, confusion matrices, and ROC-AUC.
6. Review Random Forest feature importance.
7. Demonstrate interactive and manual sample prediction.

Scaling is applied in the SVM and KNN pipelines. The notebook selects the top model by test-set F1-score.

## Results
The saved notebook output reports:
- Test-set accuracy for the selected Random Forest model: approximately **92%**.
- Random Forest ROC-AUC: **0.966**.
- Random Forest was the top model by test-set F1-score in the recorded run.

Results depend on the train/test split and model settings. See the notebook for the full classification report and comparison.

## Technologies
Python, Jupyter Notebook, Pandas, NumPy, Matplotlib, scikit-learn, and ipywidgets.

## Run locally
```bash
git clone https://github.com/USERNAME/parkinsons-disease-prediction-ml.git
cd parkinsons-disease-prediction-ml
python -m pip install -r requirements.txt
jupyter notebook
```
Open `Parkinsons_Disease_ML_Project.ipynb` and run the cells. The interactive controls require a Jupyter environment that supports ipywidgets.

## Repository contents
- `Parkinsons_Disease_ML_Project.ipynb` — complete workflow, evaluation, plots, and prediction demo.
- `requirements.txt` — Python dependencies.
- `.gitignore` — common generated/local files excluded from version control.

## Limitations and responsible use
This is an academic demonstration using a relatively small dataset. Test-set performance does not establish clinical validity or guarantee generalization to other populations, devices, or recording conditions. The model must not be used to diagnose, screen, or make treatment decisions for any person. Seek qualified medical care for health concerns.

## Author
**Sneha Theertha A D**  
M.Tech Computer Science and Information Systems

## License
No license is currently specified. All rights in the notebook remain with their respective authors unless a license is added.
