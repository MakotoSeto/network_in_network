# What's this
Implementation of Network In Network by chainer


# Dependencies

    git clone https://github.com/nutszebra/network_in_network.git
    cd network_in_network
    git submodule init
    git submodule update

# How to run
    python main.py -p ./ -g 0 


# Details about my implementation
All hyperparameters and network architecture are the same as in [[1]][Paper] except for data-augmentation.  
* Data augmentation  
Train: Pictures are randomly resized in the range of [32, 36], then 32x32 patches are extracted randomly and are normalized locally. Horizontal flipping is applied with 0.5 probability.  
Test: Pictures are resized to 32x32, then they are normalized locally. Single image test is used to calculate total accuracy.  

# Cifar10 result

| network              | depth | total accuracy (%) |
|:---------------------|-------|-------------------:|
| my implementation    | 9     | soon               |


# References
Network In Network [[1]][Paper]

[paper]: https://arxiv.org/abs/1312.4400 "Paper"
