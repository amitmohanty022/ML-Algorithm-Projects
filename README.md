# ML Algorithm Projects

Hands-on Jupyter notebooks covering core machine learning algorithms with **scikit-learn**.

| Notebook | Topic | Data |
|---|---|---|
| `Scikit_Learn_Day_1.ipynb` | Basics: linear regression, KNN, scaling, encoding, imputation | Iris + Titanic (downloaded automatically) |
| `Scikit_Learn_Day_2.ipynb` | Linear regression on a built-in dataset | Built into scikit-learn |
| `Scikit_Learn_Day_3_Logistic_Regression.ipynb` | Logistic regression on Titanic | Downloaded automatically |
| `Scikit_Learn_Day_4_Dession_Tree.ipynb` | Decision tree drug classification | `drug200.csv`* |
| `Scikit_Learn_Random_Forest.ipynb` | Random forest on car evaluation | `car.data.csv`* (or the UCI download in the notebook) |
| `Classification_KNN_and_Naive_bayes_.ipynb` | KNN and Naive Bayes on breast cancer data | `cancer_data.csv`* |
| `First_ML_Project_LinearReg.ipynb` | Predicting Olympic medals with linear regression | `teams.csv`* |
| `Stock_Sentiment_Analysis.ipynb` | Stock movement from news headlines (bag of words + random forest) | `Data.csv`* |

\* These data files are not included in the repository. See [Datasets](#datasets).

## How to run (step by step)

You need **Python 3.10 or newer** ([download](https://www.python.org/downloads/)). No API key is needed.

**1. Download the project**

```bash
git clone https://github.com/amitmohanty022/ML-Algorithm-Projects.git
cd ML-Algorithm-Projects
```

**2. Create a virtual environment and activate it**

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

**3. Install the requirements**

```bash
pip install -r requirements.txt
```

**4. Add the data files** that the notebook you want needs (see [Datasets](#datasets)). Put them in this folder, next to the notebooks.

**5. Start Jupyter**

```bash
jupyter notebook
```

Open a notebook and choose **Run → Run All Cells**.

> `Scikit_Learn_Day_1.ipynb` intentionally calls `predict()` before `fit()` once, to show the `NotFittedError`. That error is expected.

### Running in Google Colab instead

Open https://colab.research.google.com → **File → Upload notebook**. Then upload the data file with the 📁 **Files** panel on the left and run all cells.

## Datasets

| File | Where to get it |
|---|---|
| `drug200.csv` | Kaggle: search "Drug Classification drug200" |
| `car.data.csv` | UCI Car Evaluation dataset: https://archive.ics.uci.edu/dataset/19/car+evaluation (save `car.data` as `car.data.csv`) |
| `cancer_data.csv` | Kaggle: "Breast Cancer Wisconsin (Diagnostic) Data Set" |
| `teams.csv` | Olympic teams/medals dataset used in the linear regression tutorial |
| `Data.csv` | Kaggle: "Stock Sentiment Analysis using News Headlines" (25 top headlines per day + label) |

## Updates (2026)
- `sns.distplot` was removed from seaborn, so it is replaced with `sns.histplot(kde=True)`.
- `fetch_openml("titanic")` now uses `parser="liac-arff"`, which avoids a pandas 3 parsing error.
- Fixed a `SimpleImputer` shape error in Day 1.
