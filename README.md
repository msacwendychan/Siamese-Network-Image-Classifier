# Siamese Network Image Classifier

This project is to implement a 2D image classifier using Siamese Network architecture which consists of a multi-layer perception network, and successfully  build  a neural  network classifier  that  can  classify  handwritten  images  from  the MNIST digital image database.  The  network  should  be  able  to  differentiate  if  the  input  images belong  to  the same class or different classes.

The classification starts by taking two images as the input of two subnetworks with same  weights, and transforming the images into vector representations, then  the  images  are analyzed  and  the  image  distance  is calculated.  A constructive  loss  function  is optimized  to  help  with  the learning  process.  The  use  of  the  function  is  to minimize  the  distance  of  a positive pair from the same class while maximizing the distance of a negative pair from different classes. 

Several types of trainings and testings were done on the original unwarped images and warped images with different deformation parameters. Moreover, staged-learning  training  and  testing  strategy were applied  in  order  to  form  more meaningful experiments and results.


## The Neural Network Architecture

The network was formed based on CNN sequential model that constructs of a linear stack of layers. 3 sets of convolutional layers and 2 sets of fully connected layers were implemented as the main architecture.
The general architecture consists of:

Layer                     | Size           | Parameters
------------------------- | -------------  | --------------------------------
Conv2D                    | 16 x 5 x 5     | Stride = 1
MaxPooling2D              | 2 x 2          | Stride = 2
------------------------- | -------------  | --------------------------------
Conv2D                    | 32 x 3 x 3     | Stride = 1
MaxPooling2D              | 2 x 2          | Stride = 2
------------------------- | -------------  | --------------------------------
Conv2D + Dropout          | 64 x 3 x 3     | Stride = 1; Dropout rate = 0.25
Flatten                   | n.a.           | n.a.
------------------------- | -------------  | --------------------------------
Fully Connected + Dropout | 576            | Dropout rate = 0.25
------------------------- | -------------  | --------------------------------
Fully Connected           | 128            | n.a.

## Data Source

NMIST database (http://yann.lecun.com/exdb/mnist/) is a handwritten digits database which has 60,000 training and 
10,000 testing images. The experiment has expanded the training dataset to 100,000 images. The dataset will be deformed with different rotation and strength transformation for meaingful testing. 

## Built With

* [Python](https://www.python.org) - Used to create the main program
* [NumPy](http://www.numpy.org) - a Python package employed for multi-dimensional array
* [Tensorflow Keras](https://www.tensorflow.org/guide/keras) - the API of tensorflow to build deep neural network 

## Contributing

Pull requests and improvement are welcome. :) Please make sure to include commit comments for each change made. 

## Credits

Team: Liying Shi and Zhiyi Wu



