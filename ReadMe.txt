Author: Zeyad Mohamed Arafat
Contact: zeyadarafat833@gmail.com

Linear Regression — Insurance Charges

Overview:
This notebook implements a simple linear regression model (from-scratch gradient descent)
to predict normalized insurance charges using the `insurance.csv` dataset.

Files:
- linear-regression.ipynb — main notebook containing data prep, model training, and evaluation
- insurance.csv — dataset (should be in the same folder)

Purpose:
Explore preprocessing (binary mapping and one-hot encoding), feature scaling, and
manual gradient descent for linear regression. The notebook shows the mean squared error
after training.

Key preprocessing steps (as implemented in the notebook):
- Convert `sex` into `is_male` and `is_female` binary columns and drop the original column.
- Map `smoker` to `is_smoker` (1 for yes, 0 for no) and drop the original column.
- One-hot encode `region` into separate region columns and drop the original column.
- Normalize `age`, `bmi`, `children`, and `charges` by dividing by their mean.

Model details:
- Linear regression with bias term appended to features.
- Weights initialized to zeros and updated via gradient descent.
- Default learning rate and iterations are set inside the notebook (see the cell with
  `learning_rate` and the training loop).

Dependencies:
- Python 3.8+
- numpy, pandas, matplotlib

How to run:
1. Open [linear-regression.ipynb] in Jupyter or VS Code.
2. Ensure `insurance.csv` is in the same folder as the notebook.
3. Install dependencies: `pip install pandas numpy matplotlib` (or create a `requirements.txt`).
4. Run cells sequentially (top-to-bottom). The final cell prints the MSE for the trained model.

Notes & suggestions:
- You can experiment with learning rate, number of iterations, or alternative scaling.
