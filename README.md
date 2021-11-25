# Voice Emotion Recognition


![voiceEmotion](/Users\diebl\lab\FinalProject__RecognitionSpeechEmotion/image.jpeg)  

 

## Project Overview

Voice analysis technologies are quickly becoming an ever-present part of everyday life, either in our personal devices or when we are in relation with customer services.

Voice-activated menu systems have the ability to analyze the voice and emotions of the customers as they describe their issue and allow call centers to be as responsive as possible. 

Also, let's imagine a voice controlled personal music assistant that could analyse the voice emotions of the person and play the adequate playlist depending on the emotion detected.

With this project, I will explore audio features of human voice and understand how they can be used by machine learning to detect emotions.  
Understanding emotions may help us to better communicate our needs, our feelings and build healty realtionships with other people.


## Dataset
The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)" by Livingstone & Russo is licensed under CC BY-NA-SC 4.0 contains 1440 audio files from 24 Actors vocalizing two lexically-matched statements. Emotions include angry, happy, sad, fearful, calm, neutral, disgust, and surprised. [Click for dataset]( https://zenodo.org/record/1188976)



## Process


1)	See **EDA.ipynb**: Loaded audio files and created visualizations of audio features

- *Signal of the audio* : An audio signal is a variation of air pressure in a certain quantity over time. 

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/Waveplot_FemaleCalm.png">
</p>

- *Log Mel Spectogram* : A spectogramm is a way to visually represent a signal’s loudness, or amplitude, as it varies over time at different frequencies. A spectogramm is obtained by computing Fast-Fourier-Transformation on overlapping windowed segments of the signal.
A *Log mel spectrogram* is a spectrogram where the frequencies are converted to the mel scale (y-axis). The colors represents the amplitude of the signal.

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>

- *MFCCS* :  MFCCs are the coefficients of the Mel-Frequency Cesptrum (MFC) which is a representation of the short-term power spectrum of a sound. Since MFCC features represent phonemes (distinct units of sound), MFCCs are commonly used as features in speech recognition systems. 


<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>

- *Chroma*  :  Chroma is a 12-element vector that measures energy from the sound pitch usually in deciBels (dB).

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>


2)	See **Modeling.ipynb**:

- First Step :
Conducted feature extraction (log-mel spectrograms) resulting into dataframe (see **mel_24_8.csv**) and built Model with MLP Classifier. Obtained an accuracy score of 13.3% with the model having contrasting results : some emotions are well predicted while some others not all. 

The model has been improved by applying standardization to the data. Accuracy score of 45.5%. Good improvment of our model, though some errors are made i.e angry or fear predicted as happy. 

- Second Step
Conducted extraction of different features, melspectogram, chroma and MFCCS resulting into dataframe (see **mel_chroma_mfccs_24_8.csv**) and built Model with MLP Classifier. Obtained an accuracy score of % with the model having more difficulty classifying the neutral emotion.
Again, I have applied standardization to the data to increase the model performances.

Accuracy Score of 73.3%. Good quality of predictions. However fear and disgust still predicted as happy. The model seems to detected strong emotions but is not able to determine if they are positive or negative emotions.

- Third Step
Reduced the dataframe to seven emotions (see **mel_chroma_mfccs_24_7.csv**) and run the MPL Classifier Model. Accuracy score : 73.2% %. The scores of the model have not been improved

The scores of our model have not improvded but the prediction of the emotions seem to be more balanced.


<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/Initial_%26_Augmented_Model_Photos/Augmented_Model_Accuracy.png">
</p>


<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/Initial_%26_Augmented_Model_Photos/Augmented_Model_Confusion_Matrix.png">
</p>



3)	See **Uploads** for all .png and sample audio files

## Conclusion  

## Libraries

List of libraries (with a link to the documentation):

- [Librosa](http://https://librosa.org//"Title")   

- [Pandas](http://https://pandas.pydata.org/"Title")  

- [Numpy](http://https://numpy.org/doc/"Title")   

- [Matplotlib](http://https://matplotlib.org/3.1.1/"Title")  

- [Seaborn](http://https://seaborn.pydata.org/"Title")   

- [Scikit-learn](http://scikit-learn.org/stable/index.html/"Title") 

## Ressources

List of very helpful articles

