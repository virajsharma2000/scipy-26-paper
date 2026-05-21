# scipy-26-paper

test code for the scipy research paper 

Main problem that I realised last year when I was getting introduced to mech interp:

Activation space is billions of dimensions with complex non-linear geometry. We cant expect all of it to be encodable in text. 

Text-based interpretability creates a limitation that high-dimensional model cognition may break - its like saying that the model may do something that we dont even have words for. So our text based autencoders, tracers, lens etc will not be able to represent it.

We need sensors, lot of sensitive sensors that can tap into human wide capability to sense what they cannot put into words so that ve can create safety or misalignment detection which is more robust


1. First thing I wwant to do it demonstrate that a classifier using raw activations is better than a classifier using SAE features. I am not saying SAE is bad, just saying that due to the need to activations to featue text, we lose some data. I may also be saying something obvious. We all know its "Sparse" duh! ...but I want to make a point
I will use GPT2 (my trusted model I can run on my system easily, but I am using colab. And for SAE I will hook he Hooked instance to layer 8.

There are two types of numbers bring crunched - SAE and raw. Just to show SAE misses out.

https://colab.research.google.com/drive/1RhdafOFerOEFsL7Wdrph6tCEdcBGKBSv?usp=sharing
