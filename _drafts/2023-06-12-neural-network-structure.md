---
layout: post
title: Creating Neural Networks using TensorFlow and Keras 
date: 2023-06-12 12:00:00-0400
last_edited:
categories: ["Machine Learning"]
related_posts: false
img: assets/img/code.jpg
---

To keep track of the many different ways one can improve a machine learning model using TensorFlow and Keras, I decided to create this self-referential sheet which contains several helpful tips/coding examples, based on [Andrew Ng's Advanced Learning Algorithms course](https://www.coursera.org/learn/advanced-learning-algorithms).

## Iterative loop of ML development
1. Choose architecture (model, data, etc)
2. Train model
    - train your parameters $$W,B$$ with the training set
3. Diagnostics (bias, variance, and error analysis)
    - tune model parameters such as complexity, regularization and number of examples with the cross-validation set
    - evaluate your 'real world' performance using the test set.
4. Repeat steps $$1$$-$$4$$ until model is complete


## Bias/Variance
If a model's $$J_{train}$$ is much higher than the baseline level of performance (e.g., human level performance, competing algorithms performance, guess based on experience), this is an indication that the model has **high bias** (the model is underfitting). 

If a model's cross validation error $$J_{cv}$$ is much higher than the training error $$J_{train}$$, this is an indication that the model has **high variance** (model is overfitting / generalizes "poorly"). 

If a model has high bias...
- Try getting additional features
- Try adding polynomial features
- Try decreasing $$\lambda$$

If a model has high variance...
- Get more training examples
- Try smaller sets of features (e.g., $$x, x^{2}$$ instead of $$x, x^{2}, x^{3}, x^{4}$$)
- Try increasing $$\lambda$$

Note that large neural networks are generally ``low bias'' machines. 
- If a large neural network $$\textit{does not}$$ do well on the training set, try creating a bigger network. 
- If a large neural network $$\textit{does}$$ do well on the training set, but poorly on the validation set, try getting more training examples. 
- If a large neural network does well on both the training set and the validation set, congratulations -- you're done! 

## Error Analysis
- If a model has misclassified (say) $$1,000$$ training examples, you could try manually examining (say) 100 (more if you have the time) of those examples and categorizing them based on common traits.
    - After doing this, you should have a better indication of which types of examples are misclassfied the most and therefore are maybe most fruitful to focus your attention on.
        - For example, if you find that "misspelling" examples are being misclassified the most, you might collect more data pertaining to misspellings.
- Note that one limitation of error analysis is that it's much easier to do for problems that humans are good at.

## Multiclass Classification 
```python
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense
from tensorflow.keras.activations import linear, sigmoid

# Model
model = Sequential([
    # Use dense Layers, which are simple layers of neurons in which each neuron receives input from all the neurons of the previous layer.
    tf.keras.layers.Dense(units=25, activation='sigmoid', name="L1"),
    tf.keras.layers.Dense(units=25, activation='sigmoid', name="L2"),.
    # For more stable and accurate results, combine softmax and SparseCategoricalCrossentropy loss function
    tf.keras.layers.Dense(units=10, activation='linear', name="L3"),
])

# Compile
model.compile(
    # Use Adam algorithm, which makes gradient descent faster by adjusting the learning rate automatically
    optimizer=tf.keras.optimizers.Adam(learning_rate=1e-3),
    # For more stable and accurate results, combine softmax and SparseCategoricalCrossentropy loss function
    loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True) 
)

# Fit
model.fit(X, Y, epochs=100)
```




