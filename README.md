# Image-Classification-with-CNNs-in-the-Fashion-Mnist-dataset
The Fashion MNIST dataset, which contains 70,000 grayscale images in 10 categories.  
We will build and train a neural network to classify images of clothing using Convolutional Neural Networks

The dataset:

Fashion Mnist consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. 

The Preprocessing of the dataset:

The training set:

The pixel values are rescaled in the [0, 1].  
The batch size is 32.  

The validation set:

The pixel values are rescaled in the [0, 1].  
The batch size is 32.  

The architecture of the model:

A Convolutional Layer with 32 filters, 3 x 3 kernel size, Relu activation function and (28, 28, 1) as input size.  
A Pooling Layer with 2 x 2 window and Max Pool with Stride 2.  
A Convolutional Layer with 64 filters, 3 x 3 kernel size, Relu activation function.  
A Pooling Layer with 2 x 2 window and Max Pool with Stride 2.  
A Flatten Layer squash the output of the previous layer into a 1D dimension.  
A Dense Layer with 128-units and Relu activation function.  
A Dense Layer with 10-units and Softmax activation function.  

The model is compiled with  Sparse Categorical Crossentropy as lost function and adam as optimizer.  
The model is trained for 10 epochs.  

The outcome:  

The accuracy is 99.81 % and the validation accuracy is 98.73 %.  
