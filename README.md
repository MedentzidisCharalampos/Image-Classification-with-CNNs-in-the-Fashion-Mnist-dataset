# Image-Classification-with-CNNs-in-the-Fashion-Mnist-dataset
The Fashion MNIST dataset, which contains 70,000 grayscale images in 10 categories.  
We will build and train a neural network to classify images of clothing using Convolutional Neural Networks

The dataset:

Fashion Mnist consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. 

The Preprocessing of the dataset:

The training set:

The pixel values are rescaled in the [0, 1]
The images are: a. rotated by 40 b. shifted by 0.2 (the width and height seperately) d. sheared by 0.2 e. zoomed by 0.2 f. horizontal fliped
The dimesions rescaled (reduced) to 150 x 150
The batch size is: 126
The validation set:

The dimesions rescaled (reduced) to 150 x 150
The batch size is: 126
The architecture of the model:

A Convolutional Layer with 64 filters, 3 x 3 kernel size, Relu activation function and (150, 150, 3) as input size
A Pooling Layer with 2 x 2 window and Max Pool
A Convolutional Layer with 64 filters, 3 x 3 kernel size, Relu activation function
A Pooling Layer with 2 x 2 window and Max Pool
A Convolutional Layer with 128 filters, 3 x 3 kernel size, Relu activation function
A Pooling Layer with 2 x 2 window and Max Pool
A Convolutional Layer with 128 filters, 3 x 3 kernel size, Relu activation function
A Pooling Layer with 2 x 2 window and Max Pool
A Flatten Layer tha squash the the output of the previous layer into a 1D dimension
A Dropout Layer with 0.5 rate
A Dense Layer with 512-units and Relu activation function
A Dense Layer with 3-units and Softmax activation function
The model is compiled with categorical crossentropy as lost function and RMSProp as optimizer. The model is trained for 25 epochs.

The outcome:

The accuracy is 98.10 % and the validation accuracy is 95.43 %.
The training is improving and trending towards one.
The validation zig-zag a bit, but it is always between 0.9 and 1 after the first few epochs.
