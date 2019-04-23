# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) More-Statistics-and-Visualizations

> Unit 2, Lesson 2

---

## Materials We Provide

| Topic | Description | Link |
| --- | --- | --- |
| Lesson | More Statistics and Visualizations | [Here](./More-Statistic-and-Visualization.ipynb)|
| Extra Materials | French Fry Study | [Here](https://git.generalassemb.ly/data-part-time/More-Statistics-and-Visualizations/blob/master/assets/french-fry.pdf) |
| Solutions | Lesson Solution Material | [Here](./solution-code/More-Statistics-and-Visualizations-solutions.ipynb)|

In this lesson, we use an online CSV file of advertising data from the book "An Introduction to Statistical Learning". This dataset is easy to understand. It allows the student to easily compare sales data across three advertising mediums.

You will likely need to spend time on explaining covariance and correlation, perhaps doing examples on the board to make the equations as clear as possible. Make sure time is left for the scenario at the end where students have time to practice the lesson material.

---

## Learning Objectives

- Explain the difference between causation and correlation
- Determine causality and sampling bias using Directed Acyclic Graphs
- Identify what missing data is and how to handle it
- Test a hypothesis using a sample case study

---

## Lesson Outline

TOTAL (170 min)
- Data Source (10 min)
	- What are the features/covariates/predictors?
	- What is the outcome/response?
	- What do you think each row in the dataset represents?
- Math review (40 min)
	- Covariance (15 min)
	- Correlation (10 min)
	- The variance-covariance matrix (15 min)
- Causation and Correlation (10 min)
	- Structure of causal claims
	- Why do we care?
	- How do we determine if something is causal?
- Pearlean Causal DAG model (15 min)
	- What is a DAG?
	- It's possible that X causes Y.
	- Y causes X.
	- The correlation between X and Y is not statistically significant.
	- X or Y may cause one or the other indirectly through another variable.
	- There is a third common factor that causes both X and Y.
	- Both X and Y cause a third variable and the dataset does not represent that third variable evenly.
	- Controlled Experiments
	- When is it OK to rely on association?
	- How does association relate to causation?
- Sampling bias (15 min)
	- Forms of sampling bias
	- Problems from sampling bias
	- Recovering from sampling bias
    	- Stratified random sampling
- Missing data (20 min)
	- Types of missing data
	- De minimis
	- Class imbalance
    	- Relation to machine learning
- Introduction to Hypothesis Testing (20 min)
	- Validate your findings
	- Confidence intervals
	- Error types
- Scenario (40 min)
	- Exercises
	- Statistical Tests
	- Interpret your results

---

## Student Requirements

Before this lesson(s), students should already be able to:
- Perform basic data analysis in Pandas
- Have a basic understanding of bias, variance, and correlation
- Create basic visualizations in Seaborn
- Have some exposure to major considerations within experimental design

----

## Additional Resources

For more information on this topic, check out the following resources:
- [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/)
- [The more advanced book: Elements of Statistical Learning](http://web.stanford.edu/~hastie/ElemStatLearn/)
- [Spurious Correlations](http://www.tylervigen.com/spurious-correlations)
- Wikipedia pages on [ANOVA](https://en.wikipedia.org/wiki/Analysis_of_variance), [Welch's t-test](https://en.wikipedia.org/wiki/Welch's_t-test), [Mann-Whitney test](https://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test)
