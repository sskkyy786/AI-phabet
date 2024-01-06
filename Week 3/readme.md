# Week 3

This week, we'll study about feedforward neural networks <br/>

## FeedForward Neural Networks
The feedforward neural network was the first and simplest type of artificial neural network devised. In this network, the information moves in only one direction, forward, from the input nodes, through the hidden nodes (if any) and to the output nodes.

## **Forward Propagation**: <br/>
To put it simply, the process that runs inside a neuron for forward propagation is, the neuron takes n input data (training examples) x1, x2,..., xn and first assigns random weights and biases to all the input variables and calculate their weighted sum Z, and further pass it inside an activation function, g(x) such as a sigmoid (later we'll also talk about other alternatives for it),giving g(Z) = A. 
<br/>
Similarly, we calculate this activation, A for all the neurons in all the layers. The activations of the previous layer act as input data for the next layer and the activation of the last layer gives the output, y^(y-hat)
* Just as a quick revision, you can rewatch this [3blue1brown video](https://www.youtube.com/watch?v=aircAruvnKk), to have a good visualisation of the forward propagation in a feed forward nn.
* Refer to this [article](https://drive.google.com/file/d/1B53zYGIZRkB0V4qrF7EmnPrly_SGBN7b/view?usp=sharing) to understand more and implement code as well (Pl refer to [this](https://drive.google.com/file/d/1PFk7u8kHyoj3xOyEFnb77IVv2LsFl1TR/view?usp=sharing) pdf for the incomplete image on page 7).
<br/><br/>
### **Activation Functions** <br/>
We can use different types of activation functions such as sigmoid, tanh, Relu (rectified linear unit), leaky relu.
- Refer to this [website](https://www.analyticsvidhya.com/blog/2020/01/fundamentals-deep-learning-activation-functions-when-to-use-them/) and [video](https://www.youtube.com/watch?v=Xvg00QnyaIY&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=30) to know about all of them.<br/>
- [Why do we need non-linear activation functions](https://www.youtube.com/watch?v=NkOv_k7r6no&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=31)<br/> <br/>
Though, we generally prefer tanh over sigmoid since, both have similar properties, but tanh gives output whose mean can be centralised to 0 and has some other benefits which can be seen in [this](https://www.youtube.com/watch?v=nD5ag-Q1sms&t=405s) video.
Both of these activation functions, share one disadvantage that the slope tends to 0 when the numbers are very large or very small, thus the process of making improvememts slows down here, the leaky Relu function serves as a benefit in this case as it's slope never collapses. However, for practical purposes even relu function works well. While using for classification, we prefer the output of the last layer to be between 0 and 1, thus we use L-1 layers with relu activation and the last year with sigmoid activation for good results in a L layer NN.<br/> <br/>
Refer to [this](https://www.youtube.com/watch?v=G6djH3I0rG0&list=PLreVlKwe2Z0TTN9vNEsMhA2JVswctec2g) playlist to have a good idea about activation functions and their advantages.

<br/>
By now, our model has made it's first prediction, but this was with random weights and biases, hence the results were very random, we need to train our model. Now, to begin it's training the model must know where it went wrong. thus it needs a function to compute loss.

### **Optimization Problem**<br/>
Typically, a neural network model is trained using the gradient descent optimization algorithm and weights are updated using the backpropagation of error algorithm.The gradient descent algorithm seeks to change the weights so that the next evaluation reduces the error, meaning the optimization algorithm is navigating down the gradient (or slope) of error.Now that we know that training neural nets solves an optimization problem, we can look at how the error of a given set of weights is calculated.<br/>

## **Loss Function**<br/>
With neural networks, we seek to minimize the error. As such, the objective function is often referred to as a cost function or a loss function and the value calculated by the loss function is referred to as simply “loss.”

### **Maximum Likelihood And Cross Entropy** <br/>
Maximum likelihood seeks to find the optimum values for the parameters by maximizing a likelihood function derived from the training data.<br/>
When modeling a classification problem where we are interested in mapping input variables to a class label, we can model the problem as predicting the probability of an example belonging to each class. In a binary classification problem, there would be two classes, so we may predict the probability of the example belonging to the first class.<br/>
Therefore, under maximum likelihood estimation, we would seek a set of model weights that minimize the difference between the model’s predicted probability distribution given the dataset and the distribution of probabilities in the training dataset. This is called the cross-entropy. <br/> <br/>

**Cross Entropy Loss and Mean Squared Loss(MSE)** are the losses we use of classification and regression problems respectively. To know the reasons behind chck [this video](https://www.youtube.com/watch?v=2ca_K2rgNVA). PS: since, this is a NPTEL video i would suggest watching on 1.5x speed or higher xD

## Back Propagation

Under Back Propagation, we use the loss calculated using loss function to make currections to our model. For this, we use Gradient Descent and then update our parameters accordingly. Which we covered in these [videos by 3Blue1Brown](https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) last week.

We keep on repeating forward and backward propagation for many epochs to decrease value of cost function and increase accuracy.

## Back Propagation Implementation <u>(IMPORTANT!!)</u>

Please go through these notes to understand how the gradient matrices are made in the model's code
- Go through [these](https://drive.google.com/file/d/1nYFK9exhw38IHi2jIVAsULDjEwoNjNVK/view?usp=sharing) notes followed by [this](https://drive.google.com/file/d/1colfg5wiFnABfl1ds4E89Hh_Elp-1ECk/view?usp=sharing) (download it for better resolution) file.

## Multi-class Classification using NN
Rather than just to classify an object between yes/no. If we wish to classify it into more than 2 items using NN, we can do it similarly just the only difference will be that the output yhat will be a Mx1 matrix rather than 1x1 for a m class classifier.
- Refer [this](https://www.youtube.com/watch?v=oOSXQP7C7ck) to see it's implementation.

## Useful Resources
- A read to these notes: [Multi Layer NN](http://ufldl.stanford.edu/tutorial/supervised/MultiLayerNeuralNetworks/) is a worth to compile your understandings
- Refer to this [playlist](https://www.youtube.com/watch?v=bxe2T-V8XRs&list=PLiaHhY2iBX9hdHaRr6b7XevZtgZRa1PoU) to see implementation of a complete NN
- Check this [link](https://medium.com/@shaistha24/basic-concepts-you-should-know-before-starting-with-the-neural-networks-nn-3-6db79028e56d) for an intuitive run through and answers to few questions rising inside you.
## Additional Resources to explore
- Refer to this [article](http://neuralnetworksanddeeplearning.com/chap3.html) to know more intuitively about various topics and learn how to improve your model.
---
