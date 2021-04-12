Key ML Terminology:
Labels: Predicted value/thing are called labels.
Features: Input Variable. Can be anything like area of the house, words in the email text etc.
Labelled Data: Contains Features as well as label values
Unlabelled Data: Contains Features but, do not contain label values.
Models: Defines relationships between features and label.
Regression Models: Predicts continuous values. E.g.: What is the value of a house in California?
Classification Models: Predicts Discrete values E.g.: Is a given email message spam or not spam?

•	When Exploring the data, plot some graphs to get some idea about the data.
Linear Relationship in data: The data does not pass through all the data points, but an approx. estimate can be drawn by drawing the nearest line.
Of the form:

y: label

m: slope of the line
x: feature
b: intercept / bias
•	To Infer/predict values for unlabelled data, just input the value of ‘x’ into this model.
•	Training a model means learning good values for all the weights and the bias from labelled examples.
•	In Supervised learning, the algorithm builds a model by examining many examples and attempting to find a model that minimizes loss, this process is called empirical risk minimization
•	Loss: Penalty for bad prediction. Indicates how bad the model’s prediction was on a single example. More the loss, worse the prediction.
Squared Loss (L2 Loss): 
 
Mean Square Error (MSE):
It is the average squared loss per example over the whole dataset. Losses for individual datapoints are averaged.
 
(x, y): example.
prediction(x): Predicted value.
D: Data set containing many labelled examples.
N: Number of examples in D.


Reducing Loss:
When we train a model, the model computes the losses using the loss function, it examines the values of the loss function and generates new values for bias(b) and slope/weights(w). This process goes on till the algorithm reaches the model parameters with the lowest possible loss. The iterations are performed until the overall loss changes extremely slowly or does not change.
Model has converged
Gradient Descent:
Regression problems yield convex loss v/s weight plots.
Gradient descent can be used to find the point of convergence in an efficient manner.
First, pick a starting value for “w1” in   

It can be set to 0 or any random value.
When there are multiple weights, the gradient is a vector of partial derivatives with respect to the weights.
Since the gradient is a vector, it has both direction and magnitude.
The gradient always points in the direction of steepest increase in the loss function.
The gradient descent algorithm takes a step in the direction of negative gradient to reduce loss as quickly as possible.
Learning Rate:
Gradient Descent algorithms multiply the gradient by a scalar known as learning rate or step size.
If the Learning rate is too big, it might overshoot the minimum.
If the learning rate is too small, it’ll take forever for the model to converge.
Learning rate is one of the hyperparameters which can be played with for tuning the algorithm.
Stochastic Gradient Descent:
Batch: Total Number of examples used to calculate the gradient in a single iteration. Till now batch has been the entire dataset.
SGD takes the idea of taking random examples and uses a single example per iteration. It works but is pretty noisy.
Mini-Batch SGD is a compromise between full-batch iteration and SGD, it takes some examples chosen at random and is more effective than both SGD and full batch.



