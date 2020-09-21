# Siamese Network implementation using Pytorch
Implementation of Few-shot learning with Siamese Network using Pytorch.

Not in all cases there would be enough samples for in a class for efficient training of CNNs. Conventional training of Convolutional Neural Network, which require thousands of samples per class would fail or rather not produce accurate results when there are few samples in a class. Few-shot learning tries to solve the problem of image verification when the quantity of data available for training Deep Learning models is less. 

Siamese networks is a class of deep learning networks which consists of two or more identical networks (sharing the same number of layers and weights), which accept distinct inputs but are joined by an energy function at the top. During backpropagation, the weights updating is mirrored across both networks. Rather than classifying an image to an output label, siamese network tries to distinguish between the pair of images. 

<br></br>
<strong> Simple representation of Siamese Network </strong>

<p align ="center">
  <img src="https://user-images.githubusercontent.com/37014747/93771637-68381f80-fc3b-11ea-9375-f17aa81ec86f.jpeg" />
</p>

<br></br>

<strong> Network used in this repository (Koch et al.) </strong>

<p align ="center">
  <img src="https://user-images.githubusercontent.com/37014747/93769003-e1ce0e80-fc37-11ea-9183-489a964fa81d.png" />
</p>

<br></br>
***Label 1 represents dissimilar pairs.***

***Label 0 represents similar pairs.***

This repository implements the code for Siamese Neural Networks for One-shot Image Recognition by Koch et al., using Pytorch. Two loss functions are tested with Siamese networks - Contrastive loss and Binary Cross Entropy loss.

<br></br>
<strong> Training and validation losses plot with BCELoss </strong>
![bce100ep0 001lr](https://user-images.githubusercontent.com/37014747/93770743-3d999700-fc3a-11ea-8fdc-2467e01fd96b.png)


Dataset used : [Omniglot](https://www.kaggle.com/watesoyan/omniglot "Omniglot Dataset")

Other Datasets : 

[MNIST](https://github.com/myleott/mnist_png "MNIST Dataset")

[AT&T Databese of Faces](https://www.kaggle.com/kasikrit/att-database-of-faces "AT&T")



### Steps to reproduce this project:
1. Clone this repository.
2. Create an anaconda environment.
3. Install the required packages with **requirements.txt**
4. Run the jupyter notebook files with required loss function.


### Omniglot Dataset:
The Omniglot dataset consists of 50 different alphabets, 30 used in a background set and 20 used in a evaluation set. Each alphabet has a number of characters from 14 to 55 different characters drawn by 20 different subjects, resulting in 20 (105x105) images for each character. This dataset is split into training (30 alphabets), validation (10 alphabets) and testing (10 alphabets) sets.

<p align ="center">
  <br>Sample of dataset</br>
  <img src="https://user-images.githubusercontent.com/37014747/93771943-d1b82e00-fc3b-11ea-810d-5187e3ecdd1b.png" width="300" height="300"/>
</p>

<br></br>
### Results

![Testing_0001](https://user-images.githubusercontent.com/37014747/93770580-fe6b4600-fc39-11ea-9bb6-a01e52a3581b.jpg)
