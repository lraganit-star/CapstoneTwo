# Neural Network for Neural Tumors

According to the American Brain Tumor Association, approximately 80,000 people get diagnosed with a primary brain tumor, half of which are formed from glial cells. Even worse, for metastatic brain tumors have been diagnosed in about 10-30% of cancer patients. Most of these secondary tumors occur in patients ages 3-12 and 40-70 years old.

The placement of where the tumor grows can have different effects on the patient. These include, but are not limited to: behavioral changes, smell or vision loss, paralysis, and muscle weakness.

## Data

Images have been obtained from this kaggle dataset: https://www.kaggle.com/shanan93/brain-mri-segmentation-95-5-accuracy

![](images/mri.png)


The images that we're going to be using for the models will be of mri slices. MRIs are created by using magnetic and radio frequencies of light in order to get different slices of the brain. 

![](images/tumor.png)


To make the tumor stand out compared to that of the rest of the soft tissue of the brain, the patient has contrast dye injected into their blood. The tumor indicated in this image would be malignant due to the abnormal shape shown through the mask image. 

![](images/benign.png)


Compared to malignant tumors, benign tumors are not grow and invade surrounding tissues. However, they are still harmful to the patient because it can compress surrounding brain tissue and cause many problems consisting of, but limited to, vision, hearing, and balance dificulties. 


## Creating the Models

Three different neural networks were used to train the MRIs. 

### Building a brain
Neural networks are composed of 5 layers (not including the input or output layer). These are:

1. Convolutional Layer: the purpose of this layer is to extract the features from the input data (MRIs). This will give us a feature map in order to get the information about the different layers of the image.

2. Pooling Layer: in order to make the output from the convolutional layer to be easier for computations, the pooling layer is used to reduce the size of the feature map.

3. Fully Connected Layer: used to classify the image into a label

4. Dropout: neural networks have a tendency to overfit as it tries to learn more about the input data. This is fixed by adding dropout layers by randomly dropping the neurons used in the connected layer. 

5. Activation Function: Defines the output of the model. The outcome can change according to the activation function that is chosen. 

## Results

### Basic Sequential Model
Sequential Model = 0.941 (test accuracy), 0.169 (test score)
![](images/sequential_model.png)
- Accuracy increased a lot around epoch 25

### AlexNet Model
![](images/alex_arch.png)
AlexNet = 0.942 (test accuracy), 0.195 (test score)
![](images/alex_model.png)
- Worked the best in terms of accuracy, but not by much

### GoogleNet Model
![](images/google_arch.png)
GoogleNet = 0.907 (test accuracy), 0.251 (test score)
![](images/google_model.png)
- hardest neural network out of the four to build

### LeNet 5 Model
![](images/lenet_arch.png)
LeNet 5 = 0.944 (test accuracy), 0.217 (test score)
![](images/lenet_model.png)
- each epoch took about 6 minutes to run

