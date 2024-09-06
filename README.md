# Predicting Plant Traits
This project is about predicting different plant traits, given plant images and their ancillary features for training. The main model used a pre-trained ResNet-50 model to extract features from the images, concatenating them with the given ancillary features, and using them as input into XGBoost, which is a fine-tuned boosting algorithm. This model architecture resulted in an average R2 score of slightly under 0.28 on the test set, showing the success of the model.

# Project Overview
The dataset came from the TRY database (for plant trait information) and the iNaturalist database (for the plant photographs). The training set consisted of 43,363 different plant images, such as the one shown in below, along with 163 different numerical features for each of them. The training set consisted of 6,391 images, each with the same number of numerical features. The goal was to predict 6 different target trait values using the given data. The evaluation metric used to score the submission and determine its accuracy was the R2 score. This metric is commonly used for evaluating regression models, and it measures the ratio of variations in the target variables. In order to predict the traits, it was clear that data from the images and the numerical values needed to be used in order to produce an accurate model. At first, a combined neural network was used, with both a ResNet-50 and the numerical features as inputs. This method follows similarly to the one done in the original article by Schiller et al. (2021). However, after examining further, it was determined that a boosting algorithm would be more effective for this project. The XGBoost was used alongside the ResNet-50 to predict the trait values more accurately.

<img width="297" alt="Plant" src="https://github.com/user-attachments/assets/3aa47aa5-7663-457f-83c4-e62acb39d387">


# References
Schiller, C., S. Schmidtlein, C. Boonman, A. Moreno-Martínez, and T. Kattenborn (2021). “Deep learning and citizen science enable automated plant trait predictions from photographs”. Scientific Reports, vol. 11, no. 16395.
