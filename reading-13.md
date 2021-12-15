# Linear Regression

## [ How to rn Linear regression in Python](https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/)
### Scikit-learn
- module of machine learning
  - contains function for:
    - regression
    - classification
    - clustering
    - model selection
    - dimensionality redution

- Informaton gathering about data set
  - .keys()
    - if data is a dictionary it grabs all the keys
  - .feature_names
    - an attribute on the boston data set

- Scikit Learn
  - once data is placed in a dataframe where a linear relationship can be described
  - y = boston housing price
  - x = all the ofther features
  - `from sklearn.linear_model import LinearRegression` is the module
  - `lm = LinearRegression()`

- Functions of the module
  - `lm.fit()` => fits a linear model
  - `lm.score()` => returns the coefficient of dtermination

- Fitting a Linear Model
  - `lm.fit(x, bos.Price)` X is the rest of the dataframe and bos.Price is going to be the y axis

- Prdicting values
  - `plt.scatter(bos.PRICE, lm.predict(x))` creates prices vs predicted prices


- Training and validation data sets
- `sklearn.model_selection import train_test_split`
  - helps test data

### Additional Resources:
- [Real Python on regression](https://realpython.com/linear-regression-in-python/)
- [Toward Data Science Regression](https://towardsdatascience.com/train-test-split-and-cross-validation-in-python-80b61beca4b6)

[Return Home](README.md)