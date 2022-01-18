# Sign language digit recognizer
Recognizing multiple classes of objects is a common problem. Here, we have a 6-class problem where we want to recognize 6 digits (0, 1, 2, 3, 4, 5) of American Sign Language given an image of a hand. We build a neural network s for this multi-class classification task using TensorFlow. I did this project in the [Improving Deep Neural Networks: Hyperparameter Tuning, Regularization and Optimization](https://www.coursera.org/learn/deep-neural-network) course as part of the [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning).

## Datasets
We have 1080 training examples and 120 test examples, where each example is of shape (64, 64, 3) with each of RGB channel image is of size 64x64. The examples are labeled as one of 0, 1, 2, 3, 4, and 5 for the corresponding digits. These labels are one-hot encoded to be used as the target output of the recognizer, as shown below.

![One-hot encoding of class labels](images/hands.png)

## Neural network architecture
We used only TensorFlow and Keras API to build a neural network model and train it with `GradientTape`. The model we build has 3 layers: INPUT -> LINEAR -> RELU -> LINEAR -> RELU -> LINEAR -> SOFTMAX -> OUTPUT.
