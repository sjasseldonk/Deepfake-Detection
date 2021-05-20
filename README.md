# Deepfake Video Detection using Deep Convolutional and Hand-Crafted Facial Features with a Long Short-Term Memory Network
This repo contains code for detecting deepfake videos using hand-crafted facial features toghether with deep CNN extracted features. These features are then fed into a LSTM network to model temporal (in)consistencies across video frames. Finally, a fully connected layer is added to the model to predict whether a video has been subject to manipulation or not. The hand-crafted facial features were extracted through the open-source facial toolkit OpenFace. The CNN features were extracted with the Xception network of Chollet (2017) with pre-trained weights from ImageNet. All models have been implemented in Keras and trained on the Celeb-DF dataset. 

The figure below gives a general visualization of the model used in this study. 

<img width="900" alt="proposed_architecture" src="https://user-images.githubusercontent.com/54868192/118968775-99a0f080-b96c-11eb-8c18-2319e549178c.png">

For more information, consult full master paper here that has been submitted for the degree of Master of Science in Data Science & Society. 

## Results


state of the art results


## Acknowlegdements
Celeb-DF V2 Dataset: http://www.cs.albany.edu/~lsw/celeb-deepfakeforensics.html 





