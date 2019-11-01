# Satellite-Imagery-Prediction
Multi-label Prediction
Planet Amazon (satellite imaging) dataset (Kaggle)
The dataset contains satellite images of various terrains, each having their own number of different labels. The labels represent:
• Weather: cloudy, partly cloudy
• Primary - primary rainforest
• Agriculture, roads	
Data pre-processing involves transforming training images by playing around with the lighting and zoom levels. FastAI’s Datablock API is used to apply transforms, convert data in databunch object and normalise it.  This data is passed through a CNN and the model is trained. Since, we are working with multi-label data, we need to set a threshold which determines if the image contains a class (unlike normal accuracy and f2 score methods for single-label problems), which is achieved by using the partial method (setting threshold parameter equal to 0.2). 
This is followed by the standard transfer learning process, as mentioned above in the image classification problem. The process is performed twice, once for the 128x128px images and then with the 256x256px images.
