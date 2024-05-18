# ASL-Recognition-with-Deep-Learning-PyTorch

The image-based component of the American Sign Language (ASL) dataset comprises a vast array of high-resolution photographs capturing individual sign gestures and expressions. Each image is meticulously annotated to denote the specific sign being performed, providing valuable ground truth data for training and evaluation purposes. These images represent a diverse range of hand shapes, movements, and facial expressions, captured under various lighting conditions and backgrounds to simulate real-world scenarios. Researchers and developers leverage this image dataset to train deep learning models for accurate sign language recognition and understanding. By focusing solely on images, this segment of the ASL dataset enables the development of computer vision algorithms tailored specifically to analyze and interpret visual cues inherent in sign language communication.

![ASL image with labels](./static/asl-image-labels.png)

**Data Source:** [Kaggle: Synthetic ASL Alphabet](https://www.kaggle.com/datasets/lexset/synthetic-asl-alphabet)

This dataset created by Lexset contains 27000 images of the alphabet signed in American Sign Language. Each image is 512 x 512. The data is separated into a training and testing set. Within each set, there are 27 folders, one for each letter and an extra folder of random backgrounds. Each training folder contains 900 examples while each testing folder contains 100 examples.

![Datasets distributions](./static/data-set-distribution.png)
# Confusion Matrix
![Confusion Matrix](./static/confusion_matrix.png)
# Conclusions
1. I have compared training losses across epochs for RMSProp, ADAM, and SGD optimizers. Plotting the results revealed distinct optimization behaviors: 

    *While ADAM showcased spikes in training losses, SGD with momentum displayed a smooth decay. Interestingly, RMSProp demonstrated fewer spikes compared to ADAM, indicating its relative stability in optimization.*

    ![Comparison Graph](./static/compare-loss-optimizers.png)
2. Over-Fitting:

    - Training Loss (After 100 epochs): 1.19498580329e-07
    - Test Loss: 0.953

    We are observing over-fitting of the model to the training set. To overcome this issue, we can employ the following techniques:

        a. Obtain more datasets.
        b. Implement regularization methods.
        c. Design a new model architecture.



# References:

1. https://www.kaggle.com/datasets/lexset/synthetic-asl-alphabet
2. https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html
