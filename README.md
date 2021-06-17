# MNIST Classification

 ## MNIST Dataset

The MNIST database is a dataset of handwritten digits. It has 60,000 training samples, and 10,000 test samples. Each image is represented by 28x28 pixels, each
containing a value 0 - 255 with its grayscale value.

The MNIST database is available at http://yann.lecun.com/exdb/mnist/

## Objective

Our objective is to develop an algorithm that takes as input an image and correclty determine which number is shown in the image.

## Approach

### Preprocessing

1. Since the MNIST dataset doesn't contain a validation set, we will take an arbitrary 10% of the training set as our validation set. This way we can achieve an 80, 10, 10 split.
2. Then we will scale the inputs so that they end up in a scale between 0 and 1. Since each input is in a greyscale between 0 and 255, we could simply divide each input by 255 and we will achieve the desired result. 
3. To improve memory ussage we will divide our train set into n batches. Then, we will shuffle the data to have it as randomly spread as possible.

### Model

1. Since each image is 28 x 28, we could flatten them and end up with an input layer of size m * 784 inputs, where m is the number of images in the set.
2. We will use 2 hidden layers of initially 50 nodes each and an output layer of size 10 since we have 10 digits (numbers 0 to 9).
3. We'll use the relu activation function in both of our hidden layers 
4. For the output layer we will use the softmax activation function since we want to transform the final values into probabilities.

### Optimizer and Loss Function

1. For our optimizer we will use the adaptive moment estimation (adam) and for our loss function we will choose a SparseCategoricalCrossentropy.

### Training

Using tensorflow training the data is just a matter of calling the fit method on our model object and passing a few arguments. In our case we will pass it the training data, the number of epochs (iterations), our validation inputs and validation targets, and a verbose of 2 so that we could make sure to receive only the most important information in each epoch.

### Testing the Model

Once we train our training and validation sets we will test our model using test set to make sure that we didn't overfit the hyperparameters.

## Results and Future Considerations

After testing our model we achieved a final test accuracy of a little over 98%. In the future we could definitely improve our algorithm by tuning our hyperparameters. We could increase the number of hidden units and layers, play with different activation functions and learning rate, and so on.

This was definitely an extremely educational process and I look forward to continuing my machine learning journey!
