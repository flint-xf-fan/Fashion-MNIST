# Fashion-MNIST & Original MNIST

[//]: # (Image References)

[image1]: ./assets/loss.png

[image2]: ./assets/acc.png

[image3]: ./assets/mnistRecord.PNG

The exact same model applied to both original MNIST and new fashion-mnist.

---

### Architecture

    _________________________________________________________________
    Layer (type)                 Output Shape              Param #   
    =================================================================
    input_1 (InputLayer)         (None, 1, 28, 28)         0         
    _________________________________________________________________
    batch_normalization_1 (Batch (None, 1, 28, 28)         112       
    _________________________________________________________________
    conv2d_1 (Conv2D)            (None, 64, 24, 24)        1664      
    _________________________________________________________________
    max_pooling2d_1 (MaxPooling2 (None, 64, 12, 12)        0         
    _________________________________________________________________
    conv2d_2 (Conv2D)            (None, 512, 8, 8)         819712    
    _________________________________________________________________
    max_pooling2d_2 (MaxPooling2 (None, 512, 4, 4)         0         
    _________________________________________________________________
    flatten_1 (Flatten)          (None, 8192)              0         
    _________________________________________________________________
    dense_1 (Dense)              (None, 128)               1048704   
    _________________________________________________________________
    dropout_1 (Dropout)          (None, 128)               0         
    _________________________________________________________________
    dense_2 (Dense)              (None, 64)                8256      
    _________________________________________________________________
    dropout_2 (Dropout)          (None, 64)                0         
    _________________________________________________________________
    dense_3 (Dense)              (None, 10)                650       
    =================================================================
    Total params: 1,879,098
    Trainable params: 1,879,042
    Non-trainable params: 56

### Hyperparameters

`epochs = 30`
`batch_size = 256`
`opt = Adam(decay=0.001)`
`drop_out = 0.35`


## Result

## MNIST

![alt text][image3]


## Fashion-MNIST

### Loss

![alt text][image1]

### Accuracy

![alt text][image2]


## Data Reference
https://github.com/zalandoresearch/fashion-mnist

