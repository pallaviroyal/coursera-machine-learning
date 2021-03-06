# Linear Regression
## Linear regression with one variable

Implemented linear regression with one variable to predict profit for a food truck and we have data for profits and populations from the cities.
Have to use this data to select which city to expand to next.

### Dataset
* Feature : x (Citi population)
* Targetvariable : y (Profit)
* Dataset size : 97 datapoints (x,y)

### Plotting the data
Below code written in [ex1.m](ex1/ex1.m#L40)
```
data = load('ex1data1.txt');
X = data(:, 1); y = data(:, 2);
m = length(y);
```
Code written in [plotData.m](ex1/plotData.m#L19)
```
plot(x, y, 'rx', 'MarkerSize', 10);
ylabel('Profit in $10,000s');
xlabel('Population of City in 10,000s');

```
<img src="ex1/results/data_visualization.png" alt="ex1/results/data_visualization.png"></img>
### Gradient Descent 
Code written in [computeCost.m](ex1/computeCost.m#L16)
```
predictions = X * theta; % predictions on all examples
squeredError = (predictions-y) .^2; % squared errors
J = 1/(2*m) * sum(squeredError); % cost function
```
Code written in [gradientDescent.m](ex1/gradientDescent.m#L21)
```
delta = (1/m) * (X' * ((X * theta) - y));
theta = theta - alpha * delta;
```

<img src="ex1/results/cost_function.jpg" alt="ex1/results/cost_function.jpg" weight="300px" height="300px"></img>
<img src="ex1/results/cost_function_1.jpg" alt="ex1/results/cost_function_1.jpg" weight="300px" height="300px"></img>

### Linear regression line on the data
<img src="ex1/results/linear_regression_line.jpg" alt="ex1/results/linear_regression_line.jpg" weight="300px" height="300px"></img>

