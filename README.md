# Using Deep Learning to classify the Fashion-MNIST dataset

## Context
Fashion-MNIST is a dataset of Zalando's article images—consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. Zalando intends Fashion-MNIST to serve as a direct drop-in replacement for the original MNIST dataset for benchmarking machine learning algorithms. It shares the same image size and structure of training and testing splits.

The original MNIST dataset contains a lot of handwritten digits. Members of the AI/ML/Data Science community love this dataset and use it as a benchmark to validate their algorithms. In fact, MNIST is often the first dataset researchers try. "If it doesn't work on MNIST, it won't work at all", they said. "Well, if it does work on MNIST, it may still fail on others."

## Content
Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and test data sets have 785 columns. The first column consists of the class labels (see above), and represents the article of clothing. The rest of the columns contain the pixel-values of the associated image.

### Labels
Each training and test example is assigned to one of the following labels:

0 T-shirt/top
1 Trouser
2 Pullover
3 Dress
4 Coat
5 Sandal
6 Shirt
7 Sneaker
8 Bag
9 Ankle boot

## Work done
A neural network is proposed to classify the images of this dataset. The neural network is implemented using the PyTorch library, trained on the training data and validated on the testing data for 50 epochs. The neural network is a simple feedforward neural network with 3 hidden layers. The first hidden layer has 256 neurons, the second has 128 neurons and the third has 64 neurons. The activation function used is ReLU. The output layer has 10 neurons, one for each class. The loss function used is the cross-entropy loss function. The optimizer used is the Adam optimizer. The learning rate is 0.003. The neural network is trained on the training data and validated on the testing data for 50 epochs. The neural network achieves an accuracy of ~87% on the testing data. I also avoided overfitting through regularization, such as dropout while monitoring the validation performance during training. 