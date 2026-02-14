Author: Zeyad Mohamed Arafat
Contact: zeyadarafat833@gmail.com

Linear Regression — Insurance Charges
=====================================

Overview
--------
This repository contains a Jupyter Notebook that implements a simple linear regression model (from scratch)
+to predict normalized insurance charges using the provided `insurance.csv` dataset.

Files
-----
- linear-regression.ipynb — Notebook with the full workflow: data loading, preprocessing, model training (gradient descent), prediction, and final evaluation.
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
2. Create binary columns for `sex` (`is_male`, `is_female`) and drop the original column.
3. Map `smoker` to `is_smoker` (1=yes, 0=no) and drop the original column.
4. One-hot encode `region` into separate region columns and drop the original column.
5. Normalize `age`, `bmi`, `children`, and `charges` by dividing by their mean.
6. Split dataframe into features (X) and target (`charges`), add a bias column, and initialize `weights` to zeros.
7. Train weights using batch gradient descent:
   - learning rate used in the notebook: 5e-7
   - iterations: 10,000
8. Compute predictions, report mean squared error (MSE), and inspect results.

Notes
-------------------
- The notebook uses a manual gradient descent implementation and simple mean normalization; consider standard scaling or a train/test split for more robust evaluation.
- You can experiment with learning rate, number of iterations, or alternative feature scaling.
- Compare the from-scratch implementation with `sklearn.linear_model.LinearRegression` for reference.

How to run
----------
1. Open `linear-regression.ipynb` in Jupyter or VS Code and run the cells sequentially.
2. Ensure `insurance.csv` is in the same folder as the notebook.
3. Install dependencies as shown above.