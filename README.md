# Malaria-Disease-prediction.
Dataset: https://www.kaggle.com/iarunava/cell-images-for-detecting-malaria

Malaria remains a major burden on global health, with roughly 200 million cases worldwide and more than 400,000 deaths per year. Besides biomedical research and political efforts, modern information technology is playing a key role in many attempts at fighting the disease

Malaria is one of the major public health problems in India. Early prediction of a Malaria outbreak is the key for control of malaria morbidity, mortality as well as reducing the risk of transmission of malaria in the community and can help policymakers, health providers, medical officers, ministry of health and other health organizations to better target medical resources to areas of greatest need.


![Untitled](https://user-images.githubusercontent.com/38343027/95302560-bd14a080-089f-11eb-912e-79bb8659692a.jpg)


It is pretty clear that malaria is prevalent across the globe especially in tropical regions. The motivation for this project is however based on the nature and fatality of this disease. Initially if an infected mosquito bites you, parasites carried by the mosquito will get in your blood and start destroying oxygen-carrying RBCs (red blood cells). Typically the first symptoms of malaria are similar to the flu or a virus when you usually start feeling sick within a few days or weeks after the mosquito bite. However these deadly parasites can live in your body for over a year without any problems! Thus, a delay in the right treatment can lead to complications and even death. Hence early and effective testing and detection of malaria can save lives.


The World Health Organization (WHO) has released several crucial facts on malaria which you can check out here. In short, nearly half the world’s population is at risk from malaria and there are over 200 million malaria cases and approximately 400,000 deaths due to malaria every year. This gives us all the more motivation to make malaria detection and diagnosis fast, easy and effective.



# Deep Learning for Malaria Detection

Deep Learning models, or to be more specific, Convolutional Neural Networks (CNNs) have proven to be really effective in a wide variety of computer vision tasks. While we assume that you have some knowledge on CNNs, in case you don’t, feel free to dive deeper into them by checking out this article here. Briefly, The key layers in a CNN model include convolution and pooling layers as depicted in the following figure.

# Infected Image

![C137P98ThinF_IMG_20151005_163712_cell_80](https://user-images.githubusercontent.com/38343027/95303949-83dd3000-08a1-11eb-9b4d-773680646024.png)



# Uninfected Image

![C2NThinF_IMG_20150604_114751_cell_107](https://user-images.githubusercontent.com/38343027/95304089-b7b85580-08a1-11eb-9cb2-c70eca73c924.png)



ResNet-50 is a convolutional neural network that is 50 layers deep. You can load a pretrained version of the network trained on more than a million images from the ImageNet database. The pretrained network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals. As a result, the network has learned rich feature representations for a wide range of images. The network has an image input size of 224-by-224.

![Left-ResNet50-architecture-Blocks-with-dotted-line-represents-modules-that-might-be](https://user-images.githubusercontent.com/38343027/95303247-9a36bc00-08a0-11eb-83f8-f43fd9b7ad06.png)

The ResNet-50 model consists of 5 stages each with a convolution and Identity block. Each convolution block has 3 convolution layers and each identity block also has 3 convolution layers. The ResNet-50 has over 23 million trainable parameters.

# What is Residual Learning?

In general, in a deep convolutional neural network, several layers are stacked and are trained to the task at hand. The network learns several low/mid/high level features at the end of its layers. In residual learning, instead of trying to learn some features, we try to learn some residual. Residual can be simply understood as subtraction of feature learned from input of that layer. ResNet does this using shortcut connections (directly connecting input of nth layer to some (n+x)th layer. It has proved that training this form of networks is easier than training simple deep convolutional neural networks and also the problem of degrading accuracy is resolved.

This is the fundamental concept of ResNet.






# Conclusion

ResNet is a powerful backbone model that is used very frequently in many computer vision tasks
ResNet uses skip connection to add the output from an earlier layer to a later layer. This helps it mitigate the vanishing gradient problem
You can use Keras to load pretrained ResNet 50 .



