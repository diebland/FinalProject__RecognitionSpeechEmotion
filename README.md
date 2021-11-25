# Voice Emotion Recognition


![voiceEmotion](/Users\diebl\lab\FinalProject__RecognitionSpeechEmotion/image.jpeg)  

 

## Project Overview

Voice analysis technologies are quickly becoming an ever-present part of everyday life, either in our personal devices or when we are in relation with customer service.

Voice-activated menu systems have the ability to analyze the voice and emotions of the customers as they describe their issue and allow call centers to be as responsive as possible. 

Also, let's imagine a voice controlled personal assistant that could analyse the voice emotions of the person and play the adequate playlist depending on the emotion detected.

With this project, I will explore audio features of human voice and understand how they can be used by machine learning to detect emotions.  
Understanding emotions may help us to better communicate our needs, our feelings and build healty realtionships with other people.


## Dataset
The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)" by Livingstone & Russo is licensed under CC BY-NA-SC 4.0 contains 1440 audio files from 24 Actors vocalizing two lexically-matched statements. Emotions include angry, happy, sad, fearful, calm, neutral, disgust, and surprised. [Click for dataset]( https://zenodo.org/record/1188976)



## Process


1)	See **EDA.ipynb**: Loaded audio files and created visualizations of audio features

- *Signal of the audio* defintion

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/Waveplot_FemaleCalm.png">
</p>

- *Log Mel Spectogram* definition

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>

- *MFCCS* definition

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>

- *Chroma*  

<p align="center">
  <img width="460" height="300" src="https://github.com/mkosaka1/capstone_project/blob/master/Uploads/EDA_Photos/MelSpec_FemaleCalm.png">
</p>


2)	See **Modeling.ipynb**:

- First Step :
Conducted feature extraction (log-mel spectrograms) resulting into dataframe (see **.csv**) and built Model with MLP Classifier. Obtained an accuracy score of % with the model having difficulty classifying citer les émotions.
The model has been improved by applying standardization to the data. Accuracy score of

- Second Step
Conducted extraction of different features, melspectogram, chroma and MFCCS resulting into dataframe (see **.csv**) and built Model with MLP Classifier. Obtained an accuracy score of % with the model having more difficulty classifying the neutral emotion.
Again, I have applied standardization to the data to increase the model performances.

- Third Step
Reduced the dataframe to seven emotions and run the MPL Classifier Model. Accuracy score : %. The scores of the model are not improved 


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

