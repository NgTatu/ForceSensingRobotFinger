# Deep Learning-based Force Sensing for Robot Finger
This work proposes a method for force sensing using deep learning models for robot fingers having transparent soft skin. The system can successfully remove the background noise in the photos containing the deformation information of the fnger skin. To achieve this, the *inRange* function of OpenCV is ultilized with the below boundary values for the three color channels.
|              | Hue            | Saturation    | Value         |
| :---         |     :---:      |         :---: |         :---: |
| High boundary| 141            | 255           | 255           |
| Low boundary | 54             | 139           | 33            |


Here is an example of a image captured by the camera inside the finger before and after background removal.


<img src='img/sample_data.jpg'/>
The images are then used as the input for a deep learning model, which predicts the position and magnitude of the exerted force. Four deep learning models are trained with the training data set to realize an optimal architecture. The selected models are LeNet, [AlexNet](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf), VGG11 and VGG16.
