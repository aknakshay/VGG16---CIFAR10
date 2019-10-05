# VGG16---CIFAR10

The objective was to implement VGG16 in any Deep Learning framework and to edit the architecture to include Dropout layers, Batch Normalization other and small tweaks to perform image classification on CIFAR10 dataset.

VGG16 is a deep learning model which improves the performance by focusing on increasing the depth of the network by stacking a large number of convolution filters of small size together. 

In VGG16, filters of receptive field 3 × 3 are used, comparatively very small to the filters used by the previous models. Instead of using a 7 × 7 filter, three 3 × 3 filters are used which decrease the trainable parameters and effectively covers the same receptive field.  With a convolution stride of 1 px, the padding used is ‘same’.  Max Pooling is performed over 2 × 2 px with a stride of 2. 

There are 16 weight layers and 5 max pool layers in the original architecture. Input image is of 224 × 224 dimensions and there are 138 million trainable parameters. 

The same was implemented in Keras with tensorflow backend. BatchNormalization and Dropout layers are added after each MaxPooling operation. Dense layers are changed to have 4096,512 and 10 neurons respectively.

ADAM is used as an optimizer with initial learning rate 1e-3. Categorical Crossentropy is used as the loss function and accuracy as a metric.

A learning rate scheduler is added which decreases the learning rate by a factor of 10 if the validation accuracy has not increased compared to it’s n-3rd run and if learning rate has not been decreased in the last 3 epochs.


Accuracy: ~ 85% in 21 epochs
