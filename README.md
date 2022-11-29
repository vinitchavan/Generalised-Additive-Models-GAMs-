# Generalised-Additive-Models-GAMs-on NBA Dataset

I've always loved basketball, and I've always wanted to combine that love with my interest for analytics. I thus built this data collection using the NBA Stats API. I sincerely hope that working with you turns out to be as exciting as it has been for me!

### Content
Every player who has ever been on the roster of an NBA franchise is represented in the data collection, which spans more than 20 years. It includes biographical information like the team played for, draught year, and round, as well as demographic factors like age, height, weight, and place of birth. It also includes fundamental box score information, such as the number of games played, average points scored per game, rebounds, assists, etc.

### Analysis:

Linear Models are considered the Swiss Army Knife of models. There are many adaptations we can make to adapt the model to perform well on a variety of conditions and data types.  Generalised Additive Models (GAMs) are an adaptation that allows us to model non-linear data while maintaining explainability.

Py Earth Model and Py Gam Model are the two models we built above. Both models employ splines and are nonlinear in nature.

PyEarth Model : The py-earth package is a Python implementation of Jerome Friedman’s Multivariate Adaptive Regression Splines algorithm, in the style of scikit-learn. For more information about Multivariate Adaptive Regression Splines.

PyGam: Generalized Additive Models (GAMs) are smooth semi-parametric models of the form:

g(E[y|X])=β0+f1(X1)+f2(X2,X3)+…+fM(XN)

where X.T = [X_1, X_2, ..., X_N] are independent variables, 

y is the dependent variable, and g() is the link function that relates our predictor variables to the expected value of the dependent variable.


only curves in the Py Earth model fit the knots. Therefore, utilising splines, relatively few machines will fit a curve. We just use 10 splines, but as they number grows, the likelihood of a curve fitting increases.

Gam Py model It duplicated the function rather than merely fitting the curve. In order to simulate iterative work, the curve will be fitted using splines and logistic regression will then be used. Each fit curve makes it into the logistic function. It fitted the curve once more and applied the logistic function on the second value.
Because of this, the Gam model's accuracy is greater than the Py earth model.
Overall, just the curve is fit by the spline model. however GAM model Utilize the curve fit in logistic modelling.
