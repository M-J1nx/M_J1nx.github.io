---
title:  "Basic concept of deep learning"
excerpt: "What's deep learning? what it means?"
categories: 
- MachineLearning
tags:
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-04-02
last_modified_at: 2025-04-02
---

## What is Deep learning?
Deep Learning is learning method using artificial neural network. 

By using artificial neural network, we can get positive affects below :
- Various utilization
- Can be composed relatively easily

## Composition of arificial neural network
**Training model to minimize objective function**

Neural network is consisted by input layer, hidden layer and output layer.
(But, if you count how many layers in neural network, input layer is not considered.)

Deep learning model is learned through four stages below : 
- Make sure which problem it is : binary classification, multi classification, linear regression, expectation
- Preparing data
- Composing neural network
- Improve its quality by adjusting parameter
- (Ex. the number of hidden layer, the number of artificial neurons in hidden layer, evok etc.)

## About back propagation
- Forward propagation : add weight(w) and bias(b) to value from before layer and pass it to next layer
=> Calculate and save variables from input layer to output layer
- Back propagation : Edit weight and bias to minimize cost function or loss function from propagation result
