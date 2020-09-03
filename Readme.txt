We have created a function that can do Bivariate analysis at a click and generate pair-wise graph for each predictor with Target Variable automatically.

Name of Function: "Bi"

There are 2 cases:
1) When Target Variable is Numerical
	Function will generate Scatter plot for Numerical(target)-Numerical(predictor).
	Function will generate side-by-side boxplot for Numrerical(target)-Categorical(predictor) variable.
	

2) When Target is Categorical
	Function will generate side-by-side boxplot for categorical(target)-Numerical(predictor) variable.
	Function will generate side-by-side barplot for categorical(target)-Categorical(predictor) variable.

Assumption:
1) User must know his Target variable(Categorical/Numerical).
2) If a variable has count of Unique values =< 10, we assume that it must be categorical variable, hence function will automacially convert it into categorical variable.

Input Required:
Bi(data, var, target)
data-> dataframe for which Bivariate Analysis need to be done
var -> sequence of variable need for Bivariate Analysis,  (default, var = c(seq(1,ncol(data))) = all variable)
target -> Target Variable for which B. Analysis need to be done.

How to Run:
For cars dataset we can give following Input.

source("..\\Bi.R") -- To source the file from any location(local machine, github)

setwd("Required location where graph need to be stored")
Bi(cars, target= "MPG")
Bi(cars, target= "Origin")