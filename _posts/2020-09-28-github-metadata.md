---
layout: post
title:  Let's pay some Attention !
date: 2020-09-02 21:01:00
description: Introduction to Attention Mechanism
---

Before discussing a new technology or methodology, we should try to understand the need of it. And so, let us know what gave path to the Transformer Networks. 

## Challenges with Recurrent Neural Networks
<br />
<img align='left' src="https://dev-to-uploads.s3.amazonaws.com/i/ptwajkhdgj3i1zhgsqgv.png" width="750" height="450" />
_(Image Source : mc.ai)_

Gradients are simply vectors pointing in the direction of highest rate of increase of the function. During backpropagation, gradients go through matrix multiplication multiple times using the chain rule. Small gradients get smaller until they vanish and thus it gets harder to train the weights. This is called the vanishing gradient problem.
While smaller gradients vanish, if your gradient is a large value they go on increasing and result in very large updates to our network. This is known as the exploding gradient problem. 

Another challenge one faces with RNNs is that of 'reccurence'. Recurrence prevents parallel computation.
Also, large number of training steps are required to train an RNN.

Solution to all our problems is - __Transformers__!
As the title says, _Attention is all you need_ by [Vaswani et al, (2017)](https://arxiv.org/abs/1706.03762) is the paper that introduced the concept of transformers.
Let us first understand the __Attention Mechanism__.
Below attached is an image from my notes of [Prof. Pascal Poupart's](https://www.youtube.com/channel/UC7ZVvEo7-B7lA6LY2MVX72A) lecture on Transformers.

<img align='left' src="https://dev-to-uploads.s3.amazonaws.com/i/nvhmz014asq2ygtwip42.jpg" width="750" height="450" />


Attention Mechanism mimics the retrieval of a value (v) for a query (q) based on a key (k) in the database. 
We have a query and some keys (k1, k2, k3, k4), we aim to produce an output which is  a linear combination of values where the weights come from the similarity between our query and keys. 
In the above diagram, the first layer consists of the keys (vectors). We generate another layer from the similarity comparison of these keys with the query (q). Thus the second layer consists of similarities (s).

We take softmax of these values to yield another layer (a). The product of values in (a) with the values (v) gives us the attention value. 

So far we have understood what gave rise to the need of _Attention_ and what exactly is _Attention Mechanism_.
What more will we cover?
- Multihead Attention
- Masked Multihead Attention
- Layer Normalisation 
- Positional Embedding
- Comparison of Self Attention and Recurrent Layers

Let's cover all this in the next blog! 
You can follow me on [twitter](https://twitter.com/ShambhaviCodes) where I share all the good content and blogs! 
