---
layout: post
title: Creating Neural Networks using TensorFlow and Keras 
date: 2023-06-09 16:42:00-0400
last_edited:
categories: ["Machine Learning"]
related_posts: false
img: assets/img/neural_network.jpeg
---

In order to keep track of the many different ways one can train a regression/classification algorithm using TensorFlow and Keras, I thought I would create a high-level cheatsheet containing several coding examples.

## Multiclass Classification 

```python
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense
from tensorflow.keras.activations import linear, sigmoid

# Model
model = Sequential([
    # Use dense Layers, which are simple layers of neurons in which each neuron receives input from all the neurons of the previous layer.
    tf.keras.layers.Dense(units=25, activation='sigmoid'),
    tf.keras.layers.Dense(units=25, activation='sigmoid'),.
    # For more stable and accurate results, combine softmax and SparseCategoricalCrossentropy loss function
    tf.keras.layers.Dense(units=10, activation='linear'),
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

