# What's this
Implementation of NIN(Network In Network) by chainer


# Dependencies

    git clone https://github.com/nutszebra/network_in_network.git
    cd network_in_network
    git submodule init
    git submodule update

# How to run
    python main.py -p ./ -g 0 


# Details about my implementation

* Data augmentation  
Train: Pictures are randomly resized in the range of [32, 36], then 32x32 patches are extracted randomly and are normalized locally. Horizontal flipping is applied with 0.5 probability.  
Test: Pictures are resized to 32x32, then they are normalized locally. Single image test is used to calculate total accuracy.  
* Network detail  
https://gist.github.com/mavenlin/e56253735ef32c3c296d


# Cifar10 result

| network              | depth | total accuracy (%) |
|:---------------------|-------|-------------------:|
| my implementation    | 9     | 90.10               |
| NIN [[1]][Paper]      | 9     | 91.19              |

<img src="https://github.com/nutszebra/network_in_network/blob/master/loss.jpg" alt="loss" title="loss">
<img src="https://github.com/nutszebra/network_in_network/blob/master/accuracy.jpg" alt="total accuracy" title="total accuracy">

# References
Network In Network [[1]][Paper]

[paper]: https://arxiv.org/abs/1312.4400 "Paper"
