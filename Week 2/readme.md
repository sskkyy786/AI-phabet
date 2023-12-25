# Week 2

Welcome to Week 2! This week we start exploring one of the most fundamental algorithms and concepts of Machine Learning.- 

* Linear Regression
* Logistic Regression

First we shall go into Machine Learning models for estimation of values. This is termed as regression. There are other models as well however linear regression is the simplest.  

First we want you to go through the videos of first 3 weeks of 
**[this](https://www.coursera.org/learn/machine-learning-course?utm_source=mobile&utm_source=wa&utm_medium=page_share&utm_content=lih&utm_campaign=card_button)**
Coursera course

This is some additional theory to help/revise the concepts learnt.
## Linear Regression

Linear Regression is one of the most fundamental models in Machine Learning. It assumes a linear relationship between target variable *(y)* and predictors (input variables) *(x)*. Formally stating, *(y)* can be estimated assuming a linear combination of the input variables *(x)*. 

When we have a single predictor as the input, the model is called as **Simple Linear Regression** and when we have multiple predictors, the model is called **Multiple Linear Regression**.  
The input variable *(x)* is a vector of the features of our dataset, for eg. when we are predicting housing prices from a dataset, the features of the dataset will be Area of the house, Locality, etc. and the output variable *(y)* in this case will be the housing price. The general representation of a Simple Linear Regression Model is -
                                                
                                                y = θ(0) + θ(1)*x

where *θ(0)* is known as the **bias term**, and *θ* in general is called as the **weight vector**, there are the parameters of the linear regression model. For multiple linear regression, the equation modifies to - 

                                                y = transpose(Θ)*(X) 

where *X* is a vector containing all the features and *Θ* is a vector containing all the corresponding weights (bias and weights both) i.e. the parameters of the linear model. Also note that *X* here has an additonal feature - the constant term 1 which accounts for the intercept of the linear fit.

We define a function called the **Cost Function** that accounts for the prediction errors of the model. We try to minimize the cost function so that we can obtain a model that fits the data as good as possible. To reach the optima of the cost function, we employ a method that is used in almost all of machine learning called **Gradient Descent**.  

---

#### Note

The relationship established between the target and the predictors is a statistical relation and not determinsitic. A deterministic relation is possible only when the data is actually prefectly linear.

---

#### Useful Resources

* **[Overview of Gradient Descent](https://medium.com/@saishruthi.tn/math-behind-gradient-descent-4d66eb96d68d)**  
 
* (Optional) This **[article's](http://www.stat.cmu.edu/~cshalizi/mreg/15/lectures/03/lecture-03.pdf)** sections 2 and 3 explain the concept of Linear Regression as a Statistical Model, where you can calculate certain statistical quantities to determine and improve the accuracy of your model. This is known as **Optimisation**.
 

## Logistic Regression

Logistic regression is a classifier that uses regression to obtain the probability of the input data belonging to one of various classes. Unlike Linear Regression, where the target values are continuous real valued, the target variables here are drawn from a finite set of discrete values. Formulation of logistic regression can be made where the parameters are estimated using gradient descent.  

* This **[article](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)** covers the major aspects of Logistic Regression and should give you a firm grasp on the mathematics behind this algorithm

### Binary Logistic Regression

Binary logistic regression is used for classififcation into only 2 classes. Checkout **[this](https://www.statisticssolutions.com/binary-logistic-regression/)** short read on Binary Logistic Regression. 
<br>The output of a binary logistic classifier is a probability value between 0 and 1, where 0 and 1 represent the two classes. By now you must be familiar with activation functions. The activation function used for Logistic Regression is the Sigmoid Function, which is also known as the Logistic Activation function. You can read more about it **[here](https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6)**. 

### Multinomial Logistic Regression

Logistic regression can be binary or multinomial in nature. The **multinomial logistic regression** is also termed as **Softmax Regression**. 
* Go through this **[article](https://stats.idre.ucla.edu/stata/dae/multinomiallogistic-regression/)** to go deeper into the concepts of Multinomial Logistic Regression. 

The activation function used in the case of Multinomial Logistic Regression is known as the Softmax Activation Function. 

* Checkout this great **[article](https://medium.com/data-science-bootcamp/understand-the-softmax-function-in-minutes-f3a59641e86d)** on Softmax basics. 

Basically, the softmax function takes in a vector of real values as input, and generates a probability vector as the output. The dimension of this vector is the same as the number of classes for classification, and hence a single vector element having higher value than the rest of the vector elements helps us to classify the input vector (representative of an image, text, etc.) into a class. 


 
## Generalised Linear Models

On a very high level, Generalised Linear Models (GLM) are a superclass of all linear models including Linear and Logistic Regression that we talked about earlier. 

* Linear Regression is based on the assumption that the data assumes **Gaussian/Normal Distribution**.
* Binary Logistic Regression is based on the assumption that data assumes **Bernoulli Distribution**.

GLM's are based on Exponential Family Functions. **[Exponential Family](https://en.wikipedia.org/wiki/Exponential_family)** includes these two and a lot of other distributions of data that we talked about in week 1. So therefore GLM's serve as a generalisation of all linear models. To get a firm hold on generalised linear models, head **[here](https://towardsdatascience.com/generalized-linear-models-9cbf848bb8ab)**.

Go through **[this](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)** playlist by 3blue1brown to develop a better visual understaning about neural networks.

---
