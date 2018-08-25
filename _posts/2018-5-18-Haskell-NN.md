---
layout: post
title: Neural Net in Haskell!
---

I built a neural net from scratch in Haskell! See it here: [neural net repo](https://github.com/enmccarthy/hcnn)


Currently I have a fully implemented neural network running in haskell that achieves an 84% accuracy on the image set that I actually grabbed from this [blog post](https://crypto.stanford.edu/~blynn/haskell/brain.html)! This blog post has an awesome main function that makes debugging your neural network easier, by providing some visuals. 


I feel like I learned a crazy amount from this project and I hope to continue it and update this blog post with more details. Are you looking to implement your own Neural Network in Haskell? I highly recommend it. But I recommend that you start from scratch and struggle before you look at anyone elses code. The hardest part for me was the backpropagation. I thought I had a grasp on that concept until I started implementing it. I highly recommend this [explanation](https://www.ics.uci.edu/~pjsadows/notes.pdf) and to supplement it with the many blogs you can find about how to compute backpropagation (as you will find out it varies with what activation function you use). Taking the time to write out what the matrices looks like at every step is frustrating but very helpful in the long run. Don't know where to start? Start with learning about forward propagation. Write small tests that check your work as you go. You can see more on my blog post on the Neural Network Workflow.

What I learned about Haskell during this project: 
1. Haskell has lazy evaluation, this can cause very inefficient memory and can cause loss of data.

2. I/O: anytime a Haskell function takes in anything I/O the function that takes this in must also return a I/O type. For example say you have the type [((I/O Int), (I/O Float))]

 
I have a long list of TODOs for this project, including extending functionality, implementing tests, better documentation and parallelizing it.
