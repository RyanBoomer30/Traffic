# Harvard CSCI S-80 project

To download the dataset:
https://cdn.cs50.net/ai/2020/spring/projects/5/gtsrb.zip 

Initualization phase:
Initualize a 3x3 convolution layer based on the input_shape of the first layer in order to get a feature map of the data set (getting the best features of the image). Next, apply a max pooling of 2x2 to reduce the size of the images. The resulting images will then be flatten out into an input layer.

Model:
Four hidden layers with each 128 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation

Result: loss: 0.0107 - accuracy: 0.9468
