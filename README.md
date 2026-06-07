# scipy-26-paper

test code for the scipy research paper 

Main problem that I realised last year when I was getting introduced to mech interp:

Activation space is billions of dimensions with complex non-linear geometry. We cant expect all of it to be encodable in text. 

Text-based interpretability creates a limitation that high-dimensional model cognition may break - its like saying that the model may do something that we dont even have words for. So our natural language autencoders, tracers, lens etc will not be able to represent it.

We need sensors, lot of sensitive sensors that can tap into human wide capability to sense what they cannot put into words so that ve can create safety or misalignment detection which is more robust


1. First thing I wwant to do it demonstrate that a classifier using raw activations is better than a classifier using SAE features. I am not saying SAE is bad, just saying that due to the need to activations to featue text, we lose some data. I may also be saying something obvious. We all know its "Sparse" duh! ...but I want to make a point
I will use GPT2 (my trusted model I can run on my system easily, but I am using colab. And for SAE I will hook he Hooked instance to layer 8.

There are two types of numbers bring crunched - SAE and raw. Just to show SAE misses out.
This code below shows that the SAE Vs the raw activations numbers in a 3 test scenario to show that raw activations know something that SAE features don't. Its been done in a few ways first one shows the missing info (open in colab and run the large single cell, you will[ need HF secrets and permission to access your gooogle drive-> 
(https://github.com/virajsharma2000/scipy-26-paper/blob/main/scipy-2026-paper-info-loss-in-sae-v2.ipynb)

2. My next target is to create aa transducer that can convert the raw, raw raw...in that code, into something that can be felt through the right hardware

The path is simple 

raw act -> reduce dimenions, -> signal encoding -> BCI/touch/sound output -> some human guy -> Safety judgement. 

I will probably not be able to arrange the BCI or other hardware, I can create something for sound with speakers, but would that be enough?

With sound I did an experiment some time back but it was only to play the activations as musical instrument. I might have to try something similar. I am calling it activation sonification. I am not very sure iif we can generate sounds like hearing a heartbeat by a doctor, but I will try.

The experiment will be simple:

Take two categories of raw raw raw (e.g., model running factual vs. counterfacual text - thru the counterfactual prompts.)
Extract residual stream activations, reduce to ~10–20 dimensions (You tell me how thats done)
Map dimensions to audio parameters: pitch, tempo, timbre, spatial position — using a library that I am yet to dic=scover
Generate audio "signatures" for categore
play two clips, ask "which clip came from a model running false information?"

If its consistent - then sound can work.

Else I got BCI .. something I am dreading, equipement is expensive so I have to use some soft simulator...stay possted for more on that...

