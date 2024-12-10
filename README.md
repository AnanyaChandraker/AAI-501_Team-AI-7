Abstract:

The automotive industry is undergoing a rapid transformation, with autonomous vehicles at the forefront of technological advancement. As self-driving cars become increasingly sophisticated, accurate lane detection emerges as a critical component for ensuring safe and efficient navigation.  Modern vehicles are becoming increasingly reliant on advanced driver-assistance systems (ADAS) . Accurate lane detection is critical in these systems, ensuring that vehicles stay within their designated lanes. Traditionally post-processing techniques have been employed for achieving the task of lane detection. While post-processing techniques help with detection accuracy, they often lack robustness and scalability. They are limited in the detection of only a limited number of lanes, which affects the decision-making algorithm to efficiently change the lanes as the vehicle navigates. This project focuses on developing an automated lane detecting system which utilizes the advanced Deep learning methods to develop models that are capable of pixel-wise lane segmentation and lane Classification to detect lanes. This is achieved by ERFNet and LCNet which are efficient CNN Models.

This project is based on the paper submitted by Fabio Pizzati et. al (2018)

Fabio Pizzati, Marco Allodi, Alejandro Barrera, Fernando García  - Lane Detection and Classification using Cascaded CNNs doi:https://doi.org/10.48550/arXiv.1907.01294

1.	ENVIRONMENT DETAILS OF PROJECT:
a.	The Dataset used is TuSimple 
b.	Model Training Environment: Kaggle Platform is been used for Model Training using GPU P100, GPURAM: 16 GB,, CPU RAM: 29 GB, Python: 3.8
c.	Execution Environment: Kaggle Platform is been used for Execution using CPU RAM: 29 GB, Python: 3.8

2. TRAINING THE MODELS TO GENERATE DIFFERENT CLASSIFICATION OF ROAD CONFIGURATIONS:

A.	TRAINING PARAMETERS AND METHODS:

a.	Cascaded CNNs: ERFNet and LCNet
Hyperparameters:
b.	Batch Size: 16
c.	Epochs: 40
d.	Learning Rate: 1×10−21×10−2
Input Dimensions:
e.	Width: 640 pixels
f.	Height: 360 pixels
Custom Loss Function:
g.	Cross Entropy Loss: Used for multi-class segmentation.
h.	Binary Cross Entropy: Addresses background-foreground loss.
i.	Dice Loss: Minimizes overlap and maximizes similarity, particularly useful for imbalanced datasets where the object of interest is small compared to the background.
j.	Learning Rate Adjustment: A learning rate scheduler is implemented to adjust the learning rate dynamically during training.
k.	Optimizer: SGD optimizer is used to enhance convergence and model performance.
l.	Evaluation Metric: Intersection over Union (IoU) metric is employed to assess model accuracy. While it does not directly correlate with overall accuracy, it provides insights into segmentation performance.
m.	Classification: A descriptor extracts individual lanes from the processed outputs.

3. We are using IoU (Intersection Over Union) to validate the model. It is a widely used metric for image segmentation tasks. The IoU of our model is 0.20. (Ideal IoU value is 0.5 meaning the model Is good). We have low IoU because of hardware resourse constraints. As we can see from the Epochs, our models IoU kept increasing to 0.2 over 40 epochs. If we increase the epoch further, we can get good IoU.Result 1: Output of segmentation network
