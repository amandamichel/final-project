# A *Deeper* Look into Deep AI
## Loss Functions and Gradient Boosting

Models! That's what all this is for: computers taking in data and trying to produce something of it. Deep AI is at the core of many of these models for the complexity of their neural networks (for a more in robust explanation of what lies at the core of Deep AI, [click here](reflection3.md)). Whether the model is performing data regression, classification, or ranking, there must be a way to check how well the model performing-- and how to improve its performance. This is where loss functions and gradient boosting can come into play.

The purpose of a loss function is quite simple: it tells us the error between the output of a given model and the target output. The larger the difference between values (the return of the loss function), the poorer the performance of the model. PyTorch specifically has a number of loss functions that can be applied to your own code. Each loss function has a different mathematical calculation for its loss value, each telling something different about the accuracy of the data. This allows you to select a loss function that will best serve you and the desired functionality of your model.

Imagine you have a collection of models. All of these models are relatively weak, that is, they are not predicting as well as desired. However, all of these models are have the same response variable. For example, say we want to predict if a given W&M student will select to be remote or in person. We have several small models that take in different predictor variables. Each of the following is the predictor for a single model: (intended) major, home address, number of family members, age of parents, and year. Naturally, each of these models predicts with varying degrees of success. Our best bet is to find some way to combine these models...

... which is the express purpose gradient boosting! This technique takes in multiple weak prediction models and builds a single, stronger prediction model from them. How exactly does this technique build it better? Through the use of a loss function! Each weak model is added, one at a time, and the newer, stronger model takes from it to better its own prediction. The ideal combination of these models is found via optimization of the loss value of the new, stronger model. Gradient boosting allows you to combine multiple weak models to create a stronger model. 


*References*

[PyTorch Loss Functions: The Ultimate Guide,](https://neptune.ai/blog/pytorch-loss-functions?utm_source=deepaiI&utm_medium=post&utm_campaign=blog-pytorch-loss-functions) *Neptune* (16 Oct 2020). <br/>
[Gradient Boosting Definition,](https://deepai.org/machine-learning-glossary-and-terms/gradient-boosting) *DeepAI* (17 May 2019). <br/>
