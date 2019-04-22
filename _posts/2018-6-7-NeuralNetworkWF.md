---
layout: post
title: Neural Network WorkFlow
excerpt_separator: <!--more-->
---

So when I first started implementing I was overwhelmed at how the flow of Neural Networks was implemented. I *thought* had a general idea of forward propagation, loss function, activation functions and backwards propagation. But really I had no idea how to put together all these parts to make a working Neural Network which has led me to document what I have learned. I think it is important to document your struggles to understand a topic, because when it is your turn to explain the topic to others you can refresh your memory of small things that you may have struggled with.

<!--more-->
1. The input:
    My initial struggle: How does a neural network take in a 32x32 image? Now looking back this seems trivial.
    What I learned: That flatten function you see when using libraries to use neural nets... well that is how you input images. It takes the 32 x 32 matrix and turns it into a 1d array with 1024 inputs. Each pixel becomes its own input.
    This may seem like something I should have known but somehow I missed this until I had to implement it. This fact about a neural network also highlights the benefits of a convolutional neural net. It better fits the structure of an image input and can detect images that are oriented in different places.
       
2. Forward Propagation:
    Forward Propagation takes the input, multiplies it by the weight, sums the input and uses the activation function and passes this value to the next layer. In order to translate this into code you will need a function that performs matrix multiplication and sums the input for the appropriate hidden node and then a function that applies the activation function to these sums. The activation function can be different for the output layer, in the case where there are many categories for a classification problem it is common to see a softmax activation. It is best to make all these in function that take small steps because it makes them much easier to test!

3. Backpropagation:
    Backpropagation is used to train neural networks and involves quite a bit of math. It is used to calculate the gradient and propagate this back to layers and update the weights.  It involves partial derivatives, the chain rule and keeping track of inputs, weights and outputs. I highly recommend this [explanation](https://www.ics.uci.edu/~pjsadows/notes.pdf). To further understand backpropagation I would recommend reading up on gradients (gradient descent), partial derivatives (of activation functions) and your basic linear algebra.

4. The Output:
    This is the easy and fun (or sometimes frustrating) part. Your output what you get as a result of forward propagation but it is usually more accurate after backpropagation. There are different error functions you can use to represent your results depending on your type of data.