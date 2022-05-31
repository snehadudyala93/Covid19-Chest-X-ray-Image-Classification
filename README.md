# Covid19-Chest-X-ray-Classification
Building an application on images which would help doctors to classify X-rays.

The aim of this project is to classify different kinds of Xray Images. We have three types of X-ray Images which are Covid19, Normal and Seasonal Flu.

# DataSet

The Data set has two folders Train and Test. Train has three different folders (Covid, Normal, Seasonal Flu)

# Process
Split the data into three buckets(Train, validation, Test)
  1. Built the model on Train data
  2. Measure performance on Validation data
  3. Pick where the performance is best both(mainly on validation)
  4. change the parameters accordingly
  5. predict on Test data

# Procedure 

# Step 1: Image Preprocessing 
        
Check for corrupted images and delete all the corrupted images. Assign classes to each image accordingly. Dataset needs to be converted into a DataBunch object, and in the case of the computer vision data - specifically into an ImageDataBunch subclass

Transform the data to generate more images. Here is the link for get_transform: https://docs.fast.ai/tutorial.albumentations.html. Normalize the data based on imagenet_stats.
 
Split the Train data to Train and Validation with 8:2 ratio.

# Step 2: Train Model

Built a CNN model for classification. Define the parameters for CNN Model which are epchos, learning rate, Loss function, Error Rate.
To built a network, selected Residual Network (ResNet50) because it will overcame the “vanishing gradient” problem, making it possible to construct networks with up to thousands of convolutional layers, which outperform shallower networks.

unfreeze the model to update weights to all the layers of the network.

select best learning rate which would give better results.

# Step 3: Interpret the results

Interpreted the results by using confusing matrix and saw the images which are wrongly predicted. If we see wrongly predicted images we can supply similar kind images to improve learning.

# step 4: Predictions on Test data

Predict the class on unseen data which is in Test folder.




        
