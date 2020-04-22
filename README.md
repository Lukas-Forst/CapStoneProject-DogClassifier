# CapStoneProject-DogClassifier
Dog Classifier for the Udacity Data Scientist CapStone Project

### Motivation
Get more Knowledge about Deep Learning and Image classification in a fun project.

### Files:
- Sample Output-Human.png	is a sample output when using a human picture as input
- Sample Output.png	 
- dog_app.ipynb -> project Notebook with all descriptions about the project
- sample_cnn.png showcases the used model architecture

A pipeline is created to process user-supplied images.
There are 2 types of images that get classified. 

The first are dog images, which estimate the breed of the canine.
The second are images of a person, which classifies a breed of canine that resembles the humane.
Other images won't get classified and will be returned with: </br>
"Uhmmm You are not a dog or a human! Can you please try another picture? THANKS"


For creating the CNN keras, tensorflow and python is used.
# Architecture
![sample architecture](https://raw.githubusercontent.com/Lukas-Forst/CapStoneProject-DogClassifier/master/sample_cnn.png)

- 3 Convolutional Layers: - Begining with 16, 32, 64 Filters used with a Relu Activation Function, kernel size of 2 and stride of 1
- Pooling Layer: used with each convolutional Layer to reduce dimensions
- Dropout Layer: was used annd tested with a probability of 0.25 but decreased the accuracy so wasn't used for the final layer.
- Global Average Pooling Layer: to calculate the average of the input tensor to create a 1D Vector.
- Dense Layer with a relu activation function

# Transferlearning:
Testing different Models:
- VGG16
- VGG19
- ResNet50

Models like Xception and Inception could be also be used for further experimentation and testing.

ResNet50 performed the best in comparison to the other two models.

The final Model was ResNet 50:
- GlobalAveragePooling Layer to minimize the input width andn height of the input image.
- Dense Layer with a softmax activation function was used to make a multi class prediction.

# Example classification

![ClassificationExample](https://raw.githubusercontent.com/Lukas-Forst/CapStoneProject-DogClassifier/master/Sample%20Output.png)
![ClassificationExample](https://raw.githubusercontent.com/Lukas-Forst/CapStoneProject-DogClassifier/master/Sample%20Output-Human.png)

Further improvements:
- Xception and Inception testing 
- Implement more Image augmentation
- Testing other Architectures on Resnet
- Create a webapp for the Dogapp
Pytorch Implementation: [link](https://github.com/Lukas-Forst/DeepLearning/tree/master/DogBreed%20Classification)
