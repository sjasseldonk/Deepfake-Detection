# Deepfake Video Detection using Deep Convolutional and Hand-Crafted Facial Features with a Long Short-Term Memory Network
This repo contains code for detecting deepfake videos using hand-crafted facial features toghether with deep CNN extracted features. These features are then fed into a LSTM network to model temporal (in)consistencies across video frames. Finally, a fully connected layer is added to the model to predict whether a video has been subject to manipulation or not. The hand-crafted facial features were extracted through the open-source facial toolkit OpenFace. The CNN features were extracted with the Xception network of Chollet (2017) with pre-trained weights from ImageNet. All models have been implemented in Keras and trained on the Celeb-DF dataset. 

The figure below gives a general visualization of the model used in this study. 

<img width="900" alt="proposed_architecture" src="https://user-images.githubusercontent.com/54868192/118968775-99a0f080-b96c-11eb-8c18-2319e549178c.png">

Three models have been evaluated to examine whether hand-crafted facial features can improve the classification performance:
1. Proposed model: CNN + Hand-crafted Features + LSTM (see figure above)
2. Baseline model: CNN + LSTM
3. Baseline model: Hand-crafted Features + LSTM

Also, the impact of two frame selection methods have been tested. The first frame selection method is based on the first N consequtive video frames. The second frame selection method selects frames at an equal interval. 

For more information, consult full master paper here that has been submitted for the degree of Master of Science in Data Science & Society. 

## Results
The Area Under the ROC Curve and validation accuracies for different frame selection methods are shown below. The 

![aucresults](https://user-images.githubusercontent.com/54868192/118982644-eb9d4280-b97b-11eb-9a32-ee45ec46ce7f.png)



## Acknowlegdements

Celeb-DF V2 Dataset: http://www.cs.albany.edu/~lsw/celeb-deepfakeforensics.html





