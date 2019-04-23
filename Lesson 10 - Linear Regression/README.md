# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Linear Regression

> Unit 3, Lesson 1

---

## Materials We Provide

| Topic | Description | Link |
| --- | --- | --- |
| Lesson | Outlined below | [Here](linear_regression.ipynb) |
| Solution  | Solution code for blanked out lesson samples | [Here](solution-code/linear_regression-solution.ipynb) |
| Datasets | Capital Bikeshare Rider Data | [Here](./data/bikeshare.csv) |
| Practice | Kobe Shot Regularization | [Here](./practice) |
|          | Regression Review Lab    | [Here](./practice) |
|          | Simple Linear Regression | [Here](./practice) |
| Source Materials | Original files used to create this lesson | [Here](assets/slides/) |

This dataset was chosen because there it contains approximately linear relationships and is real-world data.

---

## Learning Objectives

- Define data modeling and how to apply a simple linear regression.
- Build a linear regression model using a dataset that meets the linearity assumption, using the sci-kit learn library.
- Define and identify multicollinearity in a multiple regression.

---

## Lesson Outline

TOTAL (170 min)
- Introduce the bikeshare dataset (20 min)
  - Read in the Capital Bikeshare data (15 min)
  - Visualizing the data (5 min)
- Linear regression basics (15 min)
  - Form of linear regression
- Overview of supervised learning (25 min)
  - Benefits and drawbacks of scikit-learn (5 min)
  - Requirements for working with data in scikit-learn (5 min)
  - Building a linear regression model in sklearn (5 min)
  - scikit-learn's 4-step modeling pattern (10 min)
- Build a linear regression model (10 min)
- Using the model for prediction (15 min)
  - Does the scale of the features matter?
- Work with multiple features (20 min)
  - Visualizing the data (part 2) (15 min)
  - Adding more features to the model (5 min)
- What is Multicollinearity? (10 min)
- How to select a model (25 min)
  - Feature selection (5 min)
  - Evaluation metrics for regression problems (10 min)
  - Comparing models with train/test split and RMSE (5 min)
  - Comparing testing RMSE with null RMSE (5 min)
- Feature engineering to improve performance (30 min)
  - Handling categorical features (15 min)
  - Feature engineering (15 min)
- Bonus material: Regularization
  - How does regularization work?
  - Lasso and ridge path diagrams
  - Advice for applying regularization
  - Ridge regression
- Comparing linear regression with other models


---

## Student Requirements

Before this lesson(s), students should already be able to:

- Collect data and perform basic data manipulations with Pandas
- Import libraries into Python scripts
- Create simple data visualizations using Python
- Explain basic statistical concepts including linear algebra and descriptive statistics

----

## Additional Resources

For more information on this topic, check out the following resources:

- [Ben Lorica: Six reasons why I recommend scikit-learn](http://radar.oreilly.com/2013/12/six-reasons-why-i-recommend-scikit-learn.html)
- Scikit-learn examples for [Lasso](http://scikit-learn.org/stable/auto_examples/linear_model/plot_lasso_lars.html) and [Ridge](http://scikit-learn.org/stable/auto_examples/linear_model/plot_ridge_path.html) Regression
- Scikit-learn documentation for [Lasso](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lasso.html),  [Ridge](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html), and [Elastic Net](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.ElasticNet.html) Regression
- [Analytics Vidhya's Compilation of Linear Regression Blogs](https://www.analyticsvidhya.com/blog/tag/linear-regression/)
- [Data School's "Friendly Introduction to Linear Regression" using Python](http://www.dataschool.io/linear-regression-in-python/)
