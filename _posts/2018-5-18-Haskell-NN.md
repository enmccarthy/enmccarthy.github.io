---
layout: post
title: Neural Net in Haskell!
---

I built a neural net from scratch in Haskell! See it here: [neural net repo](https://github.com/enmccarthy/hcnn)


Currently I have a fully implemented neural network running in haskell that achieves an 84% accuracy on the image set that I actually grabbed from this [blog post](https://crypto.stanford.edu/~blynn/haskell/brain.html)! This blog post has an awesome main function that makes debugging your neural network easier, by providing visuals. 


I feel like I learned a crazy amount from this project. Are you looking to implement your own Neural Network in Haskell? I recommend that you start from scratch and struggle before you look at anyone else's code. I highly recommend this [explanation](https://www.ics.uci.edu/~pjsadows/notes.pdf) of back propagation and to supplement it with the many blogs you can find about how to compute backpropagation (as you will find out it varies with what activation function you use). Don't know where to start? Start with learning about forward propagation. Write small tests that check your work as you go. 

What I learned about Haskell during this project: 
1. Haskell has lazy evaluation, this can cause very inefficient memory and can cause loss of data.

2. I/O: anytime a Haskell function takes in anything I/O the function that takes this in must also return a I/O type. For example say you have the type [((I/O Int), (I/O Float))]

