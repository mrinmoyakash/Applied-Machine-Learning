# Applied Machine Learning

A self-contained set of hands-on notebooks for learning machine learning, originally developed by
**Mrinmoy Biswas Akash** for an ML lab course and now adapted for independent, self-paced study.

Each notebook is self-contained: run it top to bottom, upload the small dataset when prompted, and
follow along. Every notebook ends with a **Practice Problems** section — try these on your own
before checking the internet for the "right" answer, since most of them don't have a single correct
one.

## Notebooks

| # | Notebook | Topics |
|---|----------|--------|
| 1 | [Data Exploration](01-data-exploration/) | pandas basics: loading, slicing, cleaning data |
| 2 | [Data Visualization](02-data-visualization/) | matplotlib & seaborn: line/bar/pie/scatter plots, heatmaps |
| 3 | [Classification I](03-classification-basics/) | Decision Trees, Logistic Regression, train/test split |
| 4 | [Classification II](04-classification-feature-extraction/) | Text classification: Bag of Words, TF-IDF, keyword features |
| 5 | [Regression](05-regression/) | Linear/Tree/Forest/SVR regression, preprocessing pipeline |
| 6 | [Feature Engineering](06-feature-engineering/) | Encoding, imputation, scaling, SMOTE, feature selection, GridSearchCV |
| 7 | [Image Classification (Conventional ML)](07-image-classification-conventional-ml/) | Hand-crafted image features + classic classifiers |
| 8 | [Neural Networks](08-neural-networks/) | A first ANN with Keras: binning, scaling, one-hot encoding, dropout |
| 9 | [Image Classification (CNN)](09-image-classification-cnn/) | Convolutional Neural Networks and transfer learning (VGG16) |
| 10 | [Clustering](10-clustering/) | DBSCAN, HDBSCAN, unsupervised grouping |
| 11 | [Hyperparameter Tuning & Transfer Learning](11-hyperparameter-tuning-transfer-learning/) | ResNet50 feature extraction + Optuna tuning |

Suggested order: follow the numbering above — later notebooks assume familiarity with concepts
(train/test splits, scikit-learn's fit/predict pattern, etc.) introduced earlier.

## How to Run

These notebooks are written for **Google Colab** (they use `google.colab.files.upload()` to load
data), which needs no local setup:

1. Open a notebook in Colab (e.g. via the "Open in Colab" badge if you're browsing on GitHub, or
   File → Upload notebook from the [Colab website](https://colab.research.google.com/)).
2. Run cells from top to bottom. When a cell asks you to upload a file, use the CSV/XLSX file
   sitting alongside that notebook in this repo (download it to your computer first if you haven't
   already).
3. For the two CNN/transfer-learning notebooks (9 and 11), switch to a GPU runtime first
   (Runtime → Change runtime type → T4 GPU) — they're very slow on CPU — and you'll need a free
   [Kaggle account](https://www.kaggle.com/) and API token (instructions are in the notebook).

### Running locally instead

You can also run these with a local Jupyter install. `files.upload()` is Colab-specific, so replace
those cells with a plain `pd.read_csv('the_file.csv')` (or `pd.read_excel(...)`) pointing at the
data file already sitting in the notebook's folder.

```bash
pip install -r requirements.txt
jupyter notebook
```

## Requirements

See [requirements.txt](requirements.txt). Notebooks 8, 9, and 11 additionally need TensorFlow
(and a GPU is strongly recommended for 9 and 11).

## Notes on the Data

Datasets are small, publicly available, and included directly in each notebook's folder — except
for the chess pieces image dataset (notebooks 9 and 11), which is downloaded on the fly from
Kaggle since it's too large to include here.

## Author

Designed by **Mrinmoy Biswas Akash**.

## License / Usage

Anyone is welcome to use these notebooks in their own class or for self-learning — feel free to
use, adapt, and share them. If you do, I'd be really grateful if you credit the original designer
(Mrinmoy Biswas Akash) somewhere in your materials or repo.
