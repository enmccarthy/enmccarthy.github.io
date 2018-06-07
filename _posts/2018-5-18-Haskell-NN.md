---
layout: post
title: Neural Net in Haskell!
---

I built a neural net from scratch in Haskell! See it here: [1]:(https://github.com/enmccarthy/hcnn)

Currently I have a fully implemented neural network running in haskell that achieves an 84% accuracy on the image set that I actually grabbed from this blog post [2]:(https://crypto.stanford.edu/~blynn/haskell/brain.html)! This blog post has an awesome main function that make debugging your neural network easier, since it provides some visuals. 


I feel like I learned a crazy amount from this project and I hope to continue it. Are you looking to implement your own Neural Network in Haskell? I highly recommend it. But I recommend that you start from scratch and struggle before you look at anyone elses code. The hardest part for me was the backwardspropagation. I thought I had a grasp on that concept until I started implementing it. I highly recommend this explanation [3]: (https://www.ics.uci.edu/~pjsadows/notes.pdf) and to supplement it with the many blogs you can find about how to compute back propagation. Taking the time to write out what the matrices looks like at every step is frustrating but very helpful in the long run.


I have a long list of TODOs for this project, including extending functionality, implementing tests, better documentation and parallelizing it.