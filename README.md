# VGG16---CIFAR10

The objective was to implement VGG16 in any Deep Learning framework and to edit the architecture to include Dropout layers, Batch Normalization other and small tweaks to perform image classification on CIFAR10 dataset.

The same was implemented in Keras with tensorflow backend. BatchNormalization and Dropout layers are added after each MaxPooling operation. Dense layers are changed to have 4096,512 and 10 neurons respectively.

ADAM is used as an optimizer with initial learning rate 1e-3. Categorical Crossentropy is used as the loss function and accuracy as a metric.

A learning rate scheduler is added which decreases the learning rate by a factor of 10 if the validation accuracy has not increased compared to it’s n-3rd run and if learning rate has not been decreased in the last 3 epochs.


Accuracy: ~ 85% in 21 epochs
