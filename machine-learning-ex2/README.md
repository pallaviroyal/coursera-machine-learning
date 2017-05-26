# Logistic Regression
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


