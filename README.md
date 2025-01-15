# Melanoma Detection Using CNN

## General Information:
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

 - Actinic keratosis
 - Basal cell carcinoma
 - Dermatofibroma
 - Melanoma
 - Nevus
 - Pigmented benign keratosis
 - Seborrheic keratosis
 - Squamous cell carcinoma
 - Vascular lesion
 
 Custom CNN models were build and were trained and analyzed on plain training data, then on data with keras augmentation followed by model trained on Augmentor augmentation. The results are satisfactory with about 94.5% 
 accuracy on the provided unseen test data.

 ## Conclusions:
### Model-1:
		- Accuracy is low at **47.5%**. This can be attributed to the following
    		- Not having enough labeled training data can lead to poor generalization. CNNs require large amounts of diverse data to learn effectively.
    		- Imbalanced Dataset: If some classes have significantly more samples than others, the model might become 	biased toward the more frequent classes, leading to poor performance on the less frequent ones.
		- Overfitting: When a model performs well on training data but poorly on validation data, it might be overfitting. This can occur if the model is too complex relative to the amount of training data.
### Model-2:
		- Validation accuracy has not improved (47.5%)
    	- There is a clear case of overfitting
    	- Total trainable params are 3,845,801
    	- The class imbalance can be a cause of this overfitting
    	- A good sample size can help the model quality
### Model-3:
    	- After increasing the size of the training dataset, the accuracy has improved (**94.6%**).
		- Total trainable params are 725,705
		- Overfitting is contained with the help of
    		- BatchNormalization
    		- Dropouts
    		- EarlyStopping
		- The model also runs with a Learning rate scheduler both with ReduceLROnPlateau and with Adam optimizer with less lr value


## Technologies Used
		Google-Colab, Jupyter Notebook, Goodle Storage
 Following libraries with their version are listed:
 Package                           Version
--------                          ---------
- Augmentor                         0.2.12
- autopep8                          2.3.1
- imageio                           2.36.1
- jupyter                           1.1.1
- keras                             3.8.0
- keras-models                      0.0.7
- matplotlib                        3.8.4
- numpy                             1.26.4
- pandas                            2.2.2
- pep8                              1.7.1
- scikit-image                      0.25.0
- scikit-learn                      1.5.1
- scipy                             1.13.1
- seaborn                           0.13.2
- sequential                        1.0.0
- statsmodels                       0.14.2
- tensorboard                       2.18.0
- tensorboard-data-server           0.7.2
- tensorflow                        2.18.0
- tensorflow-macos                  2.16.2

## Acknowledgements
1. Dataset is provided by International Skin Imaging Collaboration (ISIC)
2. This is an assignment submitted to Upgrad

## Contact
Created by [@prscsy] - feel free to contact me!

