Author: Zeyad Mohamed Arafat
Contact: zeyadarafat833@gmail.com

Linear Regression — Insurance Charges
=====================================

Overview
--------
This repository contains a Jupyter Notebook that implements a simple linear regression model (from scratch)
to predict insurance `charges` using the provided `insurance.csv` dataset. For training the notebook applies
z-score standardization (mean centering and scaling by standard deviation) to numeric features and the target.

Files
-----
- linear-regression.ipynb — Notebook with the full workflow: data loading, preprocessing, model training (gradient descent), prediction, and a final scatter plot of predicted vs actual charges.
- insurance.csv — Dataset used by the notebook.

Dependencies
------------
- Python 3.8+ recommended
- numpy
- pandas
- matplotlib

Install dependencies:

```powershell
pip install numpy pandas matplotlib
```

Notebook workflow (high level)
------------------------------
1. Load `insurance.csv` with pandas and inspect the data.
2. Map `sex` to a numeric `gender` column (`male`=1, `female`=0) and map `smoker` to `is_smoker` (1=yes, 0=no); drop the original columns.
3. One-hot encode `region` into separate region columns and drop the original `region` column.
4. Standardize (z-score) the numeric columns: `age`, `bmi`, `children`, and also standardize `charges` (target) for training.
5. Split the DataFrame into features (X) and target (`charges`).
6. Add a bias column to X and initialize `weights` to zeros.
7. Train weights using a manual batch gradient descent implementation:
   - learning rate used in the notebook: 1e-4 (0.0001)
   - iterations: 10,000
   - note: the notebook's update uses the summed gradient (`gradient.sum()`) per weight (no explicit averaging by N).
8. Compute predictions, report mean squared error (MSE) on the (standardized) target, and plot predicted vs actual charges.

Notes
-------------------
- The notebook applies z-score standardization (mean subtraction, division by std) for `age`, `bmi`, `children`, and `charges`.
- Add a train/test split to assess generalization performance.

How to run
----------
1. Open `linear-regression.ipynb` in Jupyter or VS Code and run the cells sequentially.
2. Ensure `insurance.csv` is in the same folder as the notebook.
3. Install dependencies as shown above.