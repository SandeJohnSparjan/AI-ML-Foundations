# AI-ML-Foundations
This is the repository for the LinkedIn Learning course Artificial Intelligence Foundations: Machine Learning. 

## Installing
To use these exercise files, you must have the following installed:
Jupyter Notebook environment in the cloud or locally, with the necessary libraries installed
Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree.

## Library Dependencies
Before running the code, make sure to install the following dependencies in your environment.

* pandas - %pip install pandas
* matplotlib - %pip install matplotlib
* seaborn - %pip install seaborn
* scikit-learn - %pip install scikit-learn
* numpy - %pip install numpy
* xgboost - %pip install xgboost*

## scikit-learn
This project uses the `KNNImputer` from `scikit-learn` to handle missing data in our dataset. 

## What is KNNImputer?

`KNNImputer` is a part of the `scikit-learn` library that allows for imputation of missing values using the k-Nearest Neighbors approach. It estimates the missing values based on the values of the nearest neighbors, which can be very effective for filling gaps in your dataset.

### Key Features

- **Neighbor-based Imputation**: Fills in missing values based on the average (or weighted average) of the k-nearest neighbors found in the data.
- **Flexible and Adaptable**: Can handle both numerical and categorical data.
- **Scalability**: Works efficiently with large datasets.

## Installation Instructions

### If You Have `scikit-learn` Installed

Ensure your `scikit-learn` version is 0.22 or higher to use `KNNImputer`. You can check your current version with the following command:

```bash
pip show scikit-learn
```

If your version is below 0.22, you can upgrade to the latest version using:

```bash
pip install --upgrade scikit-learn
```

### If You Do Not Have `scikit-learn` Installed

You can install the latest version of `scikit-learn` using pip:

```bash
pip install scikit-learn
```

## Usage

Once you have the correct version of `scikit-learn`, you can use `KNNImputer` in your project as follows:

```python
import pandas as pd
from sklearn.impute import KNNImputer

# Sample DataFrame with missing values
data = {'A': [1, 2, None, 4], 'B': [None, 2, 3, 4], 'C': [5, None, 7, 8]}
df = pd.DataFrame(data)

# Create a KNNImputer instance
imputer = KNNImputer(n_neighbors=2)

# Impute the missing values
imputed_data = imputer.fit_transform(df)

# Convert the imputed data back to a DataFrame
imputed_df = pd.DataFrame(imputed_data, columns=df.columns)

print(imputed_df)
```

## Additional Resources

- [scikit-learn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.impute.KNNImputer.html) for more details on `KNNImputer`.
- Check the [project wiki](./wiki) for examples and advanced usage.
