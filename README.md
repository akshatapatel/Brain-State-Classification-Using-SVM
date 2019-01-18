# Brain-State-Classification-Using-SVM
Using Support Vector Machine and Prinicipal Component Analysis to classify Brain State from fMRI images

### Image Preprocessing:
•	Realignment of the brain fMRI images for standardization in Matlab
•	Segmentation of the non-brain voxels in Matlab
### Feature Selection
•	Masking all the images to keep only the brain voxels in the image.
•	Dimensionality reduction using Principal Component Analysis so that only the important features of the image are retained in the process, thereby decreasing the training time.
### Classification
•	Classification of the brain images to be in 1 of the 4 states recorded: rest, finger movement, lips movement or foot movement. 

•	This is performed by training it using an SVM [Support Vector Machine] and finding the test set accuracy using K-Fold Cross Validation.

### Running the code:

• Run the matlab files for realignment for test and retest images(test_realign.m and retest_realign.m). It would generate a realigned 3D image.

• Run the matlab files for segmentation (creating a mask) for the realigned test and retest images(test_segmentation.m and retest_segmentation.m). This file uses the realigned image generated in the previous step to create a background mask of the brain. I have used the 6th tissue which segments the brain voxels from the background voxels. Only the 6th tissue is selected(“Native Space”) while all the other tissues are not selected(“None”). It generates a mask image which is used for masking in the ipython file.

• Run the ipython notebook file for masking the images and implementing SVM and KFold Cross Validation for the test and the retest images(with and without PCA[Principal Component Analysis]).
