## This is STEP4

## Problem:Emotion Detection from Facial Expression

### Objective
Facial detection, landmark detection, gender classification and emotion recognition, based on visual appearance
have great potential for real-world applications such as automatic cosmetics, entertainment, human-app
interaction, advertisement promotion etc. In this homework, we focus on building a CNN model for emotion
classification from image inputs.

### Goals
The goal of this project is to familiarize yourself with CNN pipeline and get your hands wet on formal data analytics
competition. You are expected to finish the following tasks:
1. Develop your deep learning models for emotion classification using Keras.
2. Gain experience in network design, loss design, loss plotting, performance evaluation and other hyperparameter
tunings.
3. Follow instructions posted on Piazza for submitting your model to the Autolab website.

### Training
Train your model with dataset as specified on Piazza. Specifically, you’ll use two directories. One is images
directory, which contains files specific to training. Another is data directory, under which there is a legend.csv,
which maps an image in the images directory with a facial expression.
### Testing
With the trained model from the above dataset, you’ll test it on images in the test directory. Note that you’ll need
to normalize the images (some template scripts will be provided).
### Evaluation
Models are scored on classification accuracy. Since this is a multi-class problem, the score is simply the number of
correct classifications divided by the total number of elements in the test set. Your accuracy on a test set will be
provided by autograder, but your grade on this HW is not a strict function of this score.
### Submission Format
The solution file contains two columns: Image and Emotion. Image is the name of the image file and acts as a key.
The emotion class is Emotion and must in {anger, contempt, disgust, fear, happiness, neutral, sadness, surprise}.
The file should contain a header and have the following format: