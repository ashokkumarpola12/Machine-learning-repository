# Machine-learning-repository
Linear Regression from Scratch (Gradient Descent)

This project implements univariate linear regression from scratch using Python and NumPy.
The goal was to understand how gradient descent actually trains a model, instead of relying on machine learning libraries.

The model predicts house prices based on house size.

Rather than using frameworks like scikit-learn, everything here is implemented manually:
	•	Cost function
	•	Gradient calculation
	•	Parameter updates
	•	Training loop

This helped me understand how machine learning models actually learn parameters.
Problem

Given house sizes and their prices, learn a function:
f(x) = wx + b
where
	•	x → house size (in thousands of square feet)
	•	y → price (in thousands of dollars)
	•	w → slope (price increase per 1000 sqft)
	•	b → intercept

The objective is to find values of w and b that minimise prediction error.
How the Model Learns

Training happens using Gradient Descent.

Steps:
	1.	Start with random values for w and b
	2.	Predict house prices using the current model
	3.	Compute prediction error using the cost function
	4.	Calculate gradients
	5.	Update parameters
	6.	Repeat until the cost converges
  Cost Function

The model minimises Mean Squared Error (MSE):
Where:
	•	m = number of training examples
	•	f(x) = predicted value
	•	y = actual value

Gradient Descent Update

Parameters are updated using:
w = w - α * dJ/dw
b = b - α * dJ/db
Where:
	•	α = learning rate
	•	dJ/dw = gradient with respect to w
	•	dJ/db = gradient with respect to b

Gradients tell us how the cost changes, so the algorithm moves in the direction that reduces error.
Training Output

After training, the model converged to:
f(x) = 15.5153x + 39.4214
Interpretation:
	•	For every additional 1000 sqft, the house price increases by about $15,515.
  Key Takeaways

Implementing this from scratch helped clarify:
	•	how linear regression works
	•	how gradient descent updates parameters
	•	how cost functions measure error
	•	Why learning rate matters
	•	how models converge

Future Improvements

Possible extensions:
	•	visualise regression line
	•	plot cost vs iterations
	•	add feature scaling
	•	implement multiple linear regression
	•	compare with scikit-learn
  This project was part of my effort to understand machine learning fundamentals while studying Andrew Ng’s Machine Learning Specialisation.

Rather than treating ML as a black box, I wanted to see how the optimisation process actually works.
