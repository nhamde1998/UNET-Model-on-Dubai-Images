# UNET-Model-on-Dubai-Images
The files include code for a U-NET convolutional Model for satellite image classification.
The project is implemented using Anaconda's Jupyter Notebook on local machine. It takes time dependent on how deep the model is and how big of data is.
There are total of 6 classes viz building, land, road, veg, water and unlabeled. The model uses the UNET convolutional model which can be found here https://arxiv.org/abs/1505.04597.

This project was only a practise for deep learning and doesn't provide guidance how many deep layers or other parameters should be used for training the model. But it is useful for someone wanting to learn how to train the model.
This project requires libraries like OpenCV, PIL, numpy, patchify, scikit-learn, matplotlib, keras, tensorflow, segmentation_models. These libraries were installed in Anaconda's command prompt and later imported in the notebook where the code is written and run. Following is the example how to install the libraries in the command prompt:
>>> pip install patchify

Make sure that these libraries are installed.

Make sure that the all training data and corresponding ground truth data is well distributed in separate folders in a main folder. In this particular case, the dataset was divided in to images and mask folders. These folders were put in the 8 folders named as Tile 1, Tile 2, Tile 3, etc. 

Decide the image_patchsize variable for patchifying the images and masks in to patches of the said size, which are later on saved as training dataset in the form of numpy array image_dataset and mask_dataset.

The mask dataset has the values in decimal format in three channels of rgb representing a class. These classes are converted in to values representing the classes viz building, land, road, veg, water and unlabeled and stored in labels variable. So this variable contains all the classified ground truth data of corresponding training patches.

