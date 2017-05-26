## Logistic Regression
Implemented logistic regression model to predict whether a student gets admitted into a university based on scores from two exams.
### Dataset
* Features : x1, x2 (Applicant's scores on two exams).
* Target variable : y (The admissions decision).
### Plotting the data
bellow code written in [plotData.m](ex2/plotData.m#L16)
```
% Find Indices of Positive and Negative Examples
pos = find(y==1); neg = find(y == 0);

% Plot Examples
plot(X(pos, 1), X(pos, 2), 'k+','LineWidth', 2, 'MarkerSize', 7);
plot(X(neg, 1), X(neg, 2), 'ko', 'MarkerFaceColor', 'y', 'MarkerSize', 7);
```
### Sigmoid function
bellow code written in [sigmoid.m](ex2/sigmoid.m#L12)
```
g = 1.0 ./ ( 1.0 + exp(-z));
```
### Cost function & gradient
bellow code written in [costFunction.m](ex2/costFunction.m#L23)
```
h = sigmoid(X * theta);
J = (1/m) * ( (-y)' * log(h) - (1 - y)' * log(1-h)) ;
grad = (1/m) * (X' * (h - y));

```


