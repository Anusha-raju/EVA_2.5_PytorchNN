# SESSION - PyTorch



## Assignment:



1. Write a neural network that can:

   1. take 2 inputs:

      1. an image from the MNIST dataset **(say 5),** and
      2. a random number between 0 and 9, **(say 7)**

   2. and gives two outputs:

      1. the "number" that was represented by the MNIST image (predict 5), and
      2. the "sum" of this number with the random number and the input image to the network (predict 5 + 7 = 12)   

   3. you can mix fully connected layers and convolution layers

   4. you can use one-hot encoding to represent the random number input and the "summed" output.

      1. Random number (7) can be represented as 0 0 0 0 0 0 0 1 0 0

      2. Sum (13) can be represented as:

         1. 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0
         2. 0b**1101** (remember that 4 digits in binary can at max represent 15, so we may need to go for 5 digits. i.e. 10010

         

## Loss Function

Negative Log-Likelihood Loss Function is used as MNIST classification and sum are multi class classification.

The Pytorch NLL Loss is expressed as: 

​																`log(x,y) = -log(y)` 

​									x represents the actual value and y the predicted value.





## Training Log

```
Epoch 1 : 
<ipython-input-38-c6d639d70f3b>:42: UserWarning: Implicit dimension choice for log_softmax has been deprecated. Change the call to include dim=X as an argument.
  return F.log_softmax(x), F.log_softmax(x1)
Train set: Average loss: 1.20
Test set: Average loss: 1.151, MNist Accuracy:98.2, Sum_Accuracy:20.07

Epoch 2 : 
Train set: Average loss: 0.95
Test set: Average loss: 0.963, MNist Accuracy:98.95, Sum_Accuracy:44.4

Epoch 3 : 
Train set: Average loss: 0.67
Test set: Average loss: 0.659, MNist Accuracy:98.99, Sum_Accuracy:88.68

Epoch 4 : 
Train set: Average loss: 0.35
Test set: Average loss: 0.351, MNist Accuracy:99.2, Sum_Accuracy:97.44
```













