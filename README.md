# Neural Network for Neural Tumors

Purpose: Using different neural network models to detect tumors within MRI brain images. 

## Data

Images have been obtained from kaggle: https://www.kaggle.com/shanan93/brain-mri-segmentation-95-5-accuracy

(Put images of brain here?)


## Creating the Models

Three different neural networks were used to train the MRIs. 

### Process of making models
Neural networks are composed of 5 layers (not including the input or output layer). These are:

1. Convolutional Layer: the purpose of this layer is to extract the features from the input data (MRIs). This will give us a feature map in order to get the information about the different layers of the image.

2. Pooling Layer: in order to make the output from the convolutional layer to be easier for computations, the pooling layer is used to reduce the size of the feature map.

3. Fully Connected Layer

4. Dropout: neural networks have a tendency to overfit as it tries to learn more about the input data. This is fixed by adding dropout layers by randomly dropping the neurons used in the connected layer. 

5. Activation Function: 

