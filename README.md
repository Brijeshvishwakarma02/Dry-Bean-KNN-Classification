# Dry Bean Classification Using K-Nearest Neighbors (KNN)

## Project Overview
This project uses machine learning to classify dry beans into seven varieties based on numerical measurements of their shape and size. It includes exploratory data analysis (EDA), data preparation, feature scaling, and a K-Nearest Neighbors (KNN) classification model.

## Dataset
- **Dataset:** Dry Bean Dataset
- **Records:** 13,611
- **Input features:** 16 numerical measurements
- **Target column:** `Class`
- **Bean classes:** BARBUNYA, BOMBAY, CALI, DERMASON, HOROZ, SEKER, SIRA

The measurements include Area, Perimeter, MajorAxisLength, MinorAxisLength, Eccentricity, ConvexArea, Solidity, Compactness, and other shape-related features.

## Project Workflow
1. Load the Excel dataset using Pandas.
2. Inspect the data structure, data types, missing values, and duplicate records.
3. Remove duplicate rows.
4. Explore feature distributions and relationships using visualizations.
5. Separate the input features (`X`) and target (`y`).
6. Apply Min-Max Scaling to the numerical features.
7. Split the data into training and testing sets.
8. Train a KNN classifier.
9. Evaluate the model using a classification report.

## Exploratory Data Analysis
The notebook contains visualizations such as:
- Count plots for bean classes
- Histograms and density plots
- Box plots and violin plots
- Scatter plots and pair plots
- Correlation heatmap
- Feature comparisons across bean classes

## Machine Learning Model
**Algorithm:** K-Nearest Neighbors (KNN) Classifier

KNN predicts the class of a new observation by looking at the classes of its nearest data points.

The notebook tests the default KNN configuration and a model with `n_neighbors=1`.

## Model Result
The saved classification report for the default KNN model shows:
- **Accuracy:** approximately **92%**
- **Weighted F1-score:** approximately **0.92**

These are the results recorded in the current notebook. Results can vary if the data split, preprocessing, or model settings are changed.

## Tools and Libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- openpyxl

## Repository Structure
```text
Dry-Bean-KNN-Classification/
│
├── KNN_BEAN_PROJECT.ipynb
├── Dry_Bean_Dataset.xlsx
└── README.md
```

## How to Run This Project
1. Download or clone this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
   ```
3. Keep `KNN_BEAN_PROJECT.ipynb` and `Dry_Bean_Dataset.xlsx` in the same folder.
4. In the notebook, update the dataset-loading line to:
   ```python
   df = pd.read_excel("Dry_Bean_Dataset.xlsx")
   ```
5. Open Jupyter Notebook and run the cells from top to bottom.

## Dataset Reference
Koklu, M. and Ozkan, I.A. (2020). “Multiclass Classification of Dry Beans Using Computer Vision and Machine Learning Techniques.” *Computers and Electronics in Agriculture*, 174, 105507.

https://doi.org/10.1016/j.compag.2020.105507

## Note
This repository is an educational machine learning project. The reported score is the result stored in the notebook and is not a guarantee of performance on new or unseen data.
