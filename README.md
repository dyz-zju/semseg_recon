#Semantic Segmentation Using Fully Convolutional Networks with added Reconstruction Loss 
An attempt to improve the quality of segmentation obtained by the algorithm proposed in [Fully Convolutional Networks for Semantic Segmentation](http://arxiv.org/pdf/1605.06211v1.pdf) (FCNs). 

The implementation is built on top of the base code provided by Sarath Shekkizhar [link](https://github.com/shekkizh/FCN.tensorflow/) 

## Network Details
 - The network is coded to be lightweight such that it can be easily trained on a 2GB GPU with a batchsize of 5.
 - The VGG-f network was made fully convolutional for the purpose. It was initialised with weights from a neetwork pre-trained on the ImageNet dataset. These weights had to be derived from a matconvnet model made available by the VGG lab.
 - The PASCAL-VOC 2012 Dataset was used to train the network.  

## Results and Observation
 - Was available to match the performance of the baseline network (VGG-f) version and improve the pixel-level accuracy by a significant aount for particular categories.
 - A bit more experimentation may even lead to better results than the baseline.
 - Sharper and more fine-grained segmentations were seen in several test cases.

## Running the Code
 - Move the file for the required model from the appropriate folder to the parent directory. For example if you want to train the FCN8 network, move the FCN-8.py (replacing the FCN.py file) file from the FCN8 folder to its parent folder and run it.
 - Create a directory called logs-8 to save the trained model.
 - A directory called Model_zoo should hold the vgg-f matconvnet weights to initialise the model with.
 - Data_zoo holds the training and the validation data.
