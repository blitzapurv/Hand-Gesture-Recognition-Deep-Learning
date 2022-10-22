# Hand-Gesture-Recognition-Deep-Learning
A Deep Learning based approach to classify human gestures for smart appliances.

To install the requirements use: ***pip install -r Requirements.txt***

## Problem Statement
A home electronics company, XYZ, manufactures state of the art smart televisions. XYZ wants to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

- Thumbs up: Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards 10 seconds
- Right swipe: 'Jump' forward 10 seconds
- Stop: Pause the movie
- Each video is a sequence of 30 frames (or images)

## Understanding the Dataset
The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

Data Source: [link](https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL)

## Consolidated Final Models
![model_summary](https://user-images.githubusercontent.com/93088807/190855991-410233e4-eed9-4ed5-8edd-71704806160b.png)

After doing all the experiments, we finalized Model 15(b) - CNN+GRU with augmentation as the final model.
Training Accuracy : 98%, Validation Accuracy : 93%. Very good validation accuracy.

- Number of Parameters, Total params: 1,395,813 with Trainable params: 1,394,821, which is decent when compared to other models. Model is not too heavy and gives good results.
- Learning rate decay was crucial in achieving this accuracy.
- The best weights of CNN-LSTM(GRU): model-00026-0.05170-0.98718-0.25728-0.93000.h5 (16.11 MB). we considered these set of weights for model testing.
