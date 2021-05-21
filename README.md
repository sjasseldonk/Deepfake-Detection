# Deepfake Video Detection using Deep Convolutional and Hand-Crafted Facial Features with Long Short-Term Memory Network
This repo contains code for detecting deepfake videos using hand-crafted facial features toghether with deep CNN extracted features. These features are then fed into a LSTM network to model temporal (in)consistencies across video frames. Finally, a fully connected layer is added to the model to predict whether a video has been subject to manipulation or not. The hand-crafted facial features were extracted through the open-source facial toolkit OpenFace. The CNN features were extracted with the Xception network of Chollet (2017) with pre-trained weights from ImageNet. All models have been implemented in Keras and trained on the Celeb-DF dataset. 

The figure below gives a general visualization of the model used in this study. 

![proposedarchitecture](https://user-images.githubusercontent.com/54868192/118985505-c8c05d80-b97e-11eb-87de-101c8c032408.png)

Three models have been evaluated to examine whether hand-crafted facial features can improve the classification performance:
1. Proposed model: CNN + Hand-crafted Features + LSTM (see figure above)
2. Baseline model: CNN + LSTM
3. Baseline model: Hand-crafted Features + LSTM

Also, the impact of two frame selection methods have been tested. The first frame selection method is based on the first N consequtive video frames. The second frame selection method selects frames at an equal interval. 

For more information, consult full master paper here that has been submitted for the degree of Master of Science in Data Science & Society. 

## Project structuur
If you want to clone this repo, you should add the data into the following folders...

## Results
The figure below shows the Area Under the ROC Curve when using the different frame selection methods for the proposed and baseline CNN-LSTM model on the Celeb-DF Test Set.

![aucresults](https://user-images.githubusercontent.com/54868192/118982644-eb9d4280-b97b-11eb-9a32-ee45ec46ce7f.png)

The best performing proposed and baseline CNN-LSTM model were also tested on the FaceSwap and Deepfakes datasets from FaceForensics++. Both test sets came in two flavours, (i) raw videos and (ii) compressed videos. The table below summarizes the test results on these datasets where both models were trained on 10 frames with 15 frames in between. 

<img width="813" alt="testresultsff" src="https://user-images.githubusercontent.com/54868192/118984906-446dda80-b97e-11eb-8809-b3a434fc630d.png">


## Acknowlegdements
Celeb-DF V2 Dataset: http://www.cs.albany.edu/~lsw/celeb-deepfakeforensics.html

OpenFace: https://github.com/TadasBaltrusaitis/OpenFace

FaceForensics++: https://github.com/ondyari/FaceForensics



