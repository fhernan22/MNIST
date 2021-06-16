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
2. Then we will scale the inputs so that they end up in a scale between 0 and 1. Since each input is in a greyscale between 0 and 255, we could simply divide each input by 255 
and we will achieve the desired result. 

To be continued...

