# sameerganesheupgrad_03

## CNN_Waste_segregation_Assignment (Waste Material Segregation for Improving Waste Management)

# Objective
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

# The key goals are:

Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
Improve waste segregation efficiency to support recycling and reduce landfill waste.
Understand the properties of different waste materials to optimise sorting methods for sustainability.
Data Understanding
The Dataset consists of images of some common waste materials.

Food Waste
Metal

# Conclusion:
   ## Data Findings
1. There are in all 7625 images given in the dataset which belongs to 7 waste segregation classes.

  #### Class mapping:
      Cardboard: 0
      Food_Waste: 1
      Glass: 2
      Metal: 3
      Other: 4
      Paper: 5
      Plastic: 6    
2. The number of images of each class is not balanced. Below is the distribution.
      Cardboard: 540 images
      Food_Waste: 1000 images
      Glass: 750 images
      Metal: 1000 images
      Other: 1010 images
      Paper: 1030 images
3. The number of images pertaining to plastic are more than 2x of the volume of other classes.
4. This distribution could potentially lead to class imbalance.
5. All images are of uniform size 256 x 256.
6. Data set partitioned into training, and test sets for model development and evaluation.

 ## Model Training results:
 1. Tried Creating models with different combination of conv layers, batch size, no of filters, batch normaliation, pooling and dropouts.
2. Not all the models executed, few got stuck for very long time, due to resource constraint. Did not included data augmentation being option and resource constraint.
3. **Batch normalization** did not showed any significant contribution towards improving the accuracy.
4. Adding **Drop out layer** helped in improving the accuracy
5. **Overall Accuracy**: The model has an overall accuracy of 46%, indicating that it correctly classifies waste products less than half the time.
6. Class Performance:
   **Plastic** : This class has the highest recall (0.88), meaning the model is good at identifying plastic waste. It also has a relatively high f1-score (0.56), 
                 indicating a balance between precision and recall.  
   **Paper**: Despite having the highest precision (0.75), the recall is quite low (0.23), suggesting that while the model is accurate when it predicts paper, it often misses paper 
                 items.  
   **Metal**: This class has the lowest precision (0.32) and recall (0.07), indicating poor performance in identifying metal waste.  

8. **Class Imbalance**: The precision, recall & f1-score vary significantly across different classes, with Plastic having the highest number of instances (689) and Cardboard the lowest (162). This imbalance can affect the model's performance, as it may be biased towards classes with more instances.
9. These insights suggest areas for improvement, such as addressing class imbalance and enhancing the model's ability to identify certain classes like Glass, Metals etc. 





## Technologies used

  #### numpy version: 1.26.4
  #### pandas version: 2.2.2
  #### seaborn version: 0.13.2
  #### matplotlib version: 3.8.4
  #### PIL version: 10.3.0
  #### tensorflow version: 2.16.2
  #### keras version: 3.9.0
  #### sklearn version: 1.4.2
