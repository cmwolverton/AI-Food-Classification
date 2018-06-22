# AI-Food-Classification
Use Deep Learning and Artificial Intelligence with TensorFlow to classify food into 11 categories. Dataset used and description can be found here:
<a href="https://mmspg.epfl.ch/food-image-datasetsp" target="_blank">Food-11</a>

# Prerequisites
Download the dataset from link: <a href="http://grebvm2.epfl.ch/lin/food/Food-11.zip" target="_blank">Food-11.zip</a>. Extract zip file as "Food-11" into the same folder 'AI-Food-Classification'. Ensure that "Food-11" has 3 sub directories.

# Run
Run the JupyterNote 'Food-Classification-Exploratory-Data-Analysis'. Output images will be stored in 'food-classification-eda-images' directory

# Analysis
Input size analysis: 
![alt text](https://github.com/shbharath/AI-Food-Classification/blob/master/food-classification-eda-images/input_size_exploration.png "Sizing the Image Analysis")

# Alexnet 

Alexnet Architecture Diagram
![alt text](https://github.com/cmwolverton/AI-Food-Classification/blob/master/Alexnet/AlexnetConfiguration.png "Alexnet architecture")
Alexnet is well know as the 2012 winner of the ImageNet Large Scale Visual Recognition Challenge created by 
the SuperVision group, consisting of Alex Krizhevsky, Geoffrey Hinton, and Ilya Sutskever.  Its creation was a 
major breakthrough in the computer vision field because it ushered in the use of convolutional neural networks.  
The architecture consists of 5 convolutional layers and 3 fully connected layers.  

Our team chose to base its work on Alexnet because of significance in the field, and its relative simplicity 
compared to the most recent innovations in network architectures.  We considered the simplicity a positive 
aspect for providing insights to students.

We took advantage of transfer learning by initializing the network with weights learned by the ImageNet training.  
We finetuned the network to classify images from the Food-11 dataset.  We allowed only the weights of the 
final two fully connected layers of the network to update as the network was trained.  The decision to take
this approach was motivated by the intuition that the convolutional layers converged to filters which produce 
"features" of the images which can then be used for classification in the fully connected layers.
