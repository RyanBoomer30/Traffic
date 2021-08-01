To download the dataset:
https://cdn.cs50.net/ai/2020/spring/projects/5/gtsrb.zip 

Initualization phase:
Initualize a 3x3 convolution layer based on the input_shape of the first layer in order to get a feature map of the data set (getting the best features of the image). Next, apply a max pooling of 2x2 to reduce the size of the images. The resulting images will then be flatten out into an input layer.

Trial 1:
Two hidden layers with each 128 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0143 - accuracy: 0.9234 (so far best)

Trial 2:
Two hidden layers with each 64 nodes (relu activation), a dropout rate of 0.5, and an output layer using relu activation
Result: loss: 0.3587 - accuracy: 0.0065 (very terrible result)
Possible error: Using relu as an output activation

Trial 3:
Two hidden layers with each 64 nodes (relu activation), a dropout rate of 0.8, and an output layer using softmax activation
Result: loss: 0.0609 - accuracy: 0.4746 (not very terrible but still a bad result)
Possible error: Not enough training ndoes and too high of a dropout rate, causing even less nodes to train

Trial 4:
Three hidden layers with each 128 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0143 - accuracy: 0.9234 (new best result)

Trial 5:
Four hidden layers with each 128 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0107 - accuracy: 0.9468 (new best result)

Trial 6:
Four hidden layers with two layers of 128 nodes (relu activation) and two layers of 256 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0139 - accuracy: 0.9070 (good result but lower than the best)
Possible error: too many nodes, which caused overfitting and expensive train

Trial 7:
Four hidden layers with two layers of 128 nodes (relu activation) and two layers of 128 nodes (linear activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0322 - accuracy: 0.7345 (not as good of a result)
Possible error: using linear activation on two of the hidden layers

Trial 8:
Five hidden layers with each 128 nodes (relu activation), a dropout rate of 0.5, and an output layer using softmax activation
Result: loss: 0.0122 - accuracy: 0.9279 (good result but lower than the best)
Possible error: too many nodes, which caused overfitting and expensive train

Trial 9:
Four hidden layers with each 128 nodes (relu activation), a dropout rate of 0.3, and an output layer using softmax activation
Result: loss: 0.0112 - accuracy: 0.9424 (same as the best)
Possible error: Same result as the best but this model has lower dropout rate, therefore, more overfitting

Conclusion: the best neural network that draws out the best accuracy with the lowest loss rate is trial 5 since any more nodes, adjustment to the activation type or dropout rate would create a worse result.

