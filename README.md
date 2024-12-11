# AAI-501_Team-AI-7 (AI-Based Lane Detection)
This project is a part of the AAI_500_Group7 course in the Applied Artificial Intelligence Program at the University of San Diego (USD) to develop an AI-based Lane Detection model.

# Abstract :

The automotive industry is undergoing a rapid transformation, with autonomous vehicles at the forefront of technological advancement. As self-driving cars become increasingly sophisticated, accurate lane detection emerges as a critical component for ensuring safe and efficient navigation.  Modern vehicles are becoming increasingly reliant on advanced driver-assistance systems (ADAS) . Accurate lane detection is critical in these systems, ensuring that vehicles stay within their designated lanes. Traditionally post-processing techniques have been employed for achieving the task of lane detection. While post-processing techniques help with detection accuracy, they often lack robustness and scalability. They are limited in the detection of only a limited number of lanes, which affects the decision-making algorithm to efficiently change the lanes as the vehicle navigates. This project focuses on developing an automated lane detecting system which utilizes the advanced Deep learning methods to develop models that are capable of pixel-wise lane segmentation and lane Classification to detect lanes. This is achieved by ERFNet and LCNet which are efficient CNN Models.

This project is based on the paper submitted by Fabio Pizzati et. al (2018)

Fabio Pizzati, Marco Allodi, Alejandro Barrera, Fernando García  - Lane Detection and Classification using Cascaded CNNs doi:https://doi.org/10.48550/arXiv.1907.01294

Here’s a Markdown representation of the provided query regarding training parameters and methods, results, and conclusions related to lane detection models using Cascaded CNNs like ERFNet and LCNet.

# Training Parameters and Methods

## Cascaded CNNs: ERFNet and LCNet

### Hyperparameters:
- **Batch Size**: 16
- **Epochs**: 40
- **Learning Rate**: \(1 \times 10^{-2}\)

### Input Dimensions:
- **Width**: 640 pixels
- **Height**: 360 pixels

### Custom Loss Function:
- **Cross Entropy Loss**: Used for multi-class segmentation.
- **Binary Cross Entropy**: Addresses background-foreground loss.
- **Dice Loss**: Minimizes overlap and maximizes similarity, particularly useful for imbalanced datasets where the object of interest is small compared to the background.
- **Learning Rate Adjustment**: A learning rate scheduler is implemented to adjust the learning rate dynamically during training.
- **Optimizer**: SGD optimizer is used to enhance convergence and model performance.
- **Evaluation Metric**: Intersection over Union (IoU) metric is employed to assess model accuracy. While it does not directly correlate with overall accuracy, it provides insights into segmentation performance.
- **Classification**: A descriptor extracts individual lanes from the processed outputs.

# Results and Conclusion

We have used IoU (Intersection Over Union) to validate the model. It is a widely used metric for image segmentation tasks. The IoU of our model is 0.20 (the ideal IoU value is 0.5, meaning the model is good). We have a low IoU because of hardware resource constraints. As we can see from the epochs, our model's IoU kept increasing to 0.20 over 40 epochs. 

# Acknowledgements
We would like to extend our thanks to our Professor Premkumar Chithaluru for the support and contiued guidance providded througout the Project of Course AAI- 501 A1 - Introduction to Artificial Intelligence course (OL - IN FALL 20024 B)


