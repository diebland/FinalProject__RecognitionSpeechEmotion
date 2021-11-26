# Voice Emotion Recognition

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/image.jpeg">
</p>

## Project Overview

Voice analysis technologies are quickly becoming an ever-present part of everyday life, either in our personal devices or when we are in relation with customer services.

Voice-activated menu systems have the ability to analyze the voice and emotions of the customers as they describe their issue and allow call centers to be as responsive as possible. 

Also, let's imagine a voice controlled personal music assistant that could analyse the voice emotions of the person and play the adequate playlist depending on the emotion detected.

With this project, I will explore audio features of human voice and understand how they can be used by machine learning to detect emotions.  
Understanding emotions may help us to better communicate our needs, our feelings and build healty realtionships with other people.
[Google Slides Presentation](https://docs.google.com/presentation/d/1VzdeTRmIjxPRJDCaYT7dFo-GpK1PKkBmoERj_KBmHvg/edit?usp=sharing)


## Dataset
The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)" by Livingstone & Russo is licensed under CC BY-NA-SC 4.0 contains 1440 audio files from 24 Actors vocalizing two lexically-matched statements. Emotions include angry, happy, sad, fearful, calm, neutral, disgust, and surprised. [Click for dataset]( https://zenodo.org/record/1188976)



## Process


1)	See **EDA.ipynb**: Loaded audio files and created visualizations of audio features

- *Signal of the audio* : An audio signal is a variation of air pressure in a certain quantity over time.

- *Mel Spectogram* : A spectogramm is a way to visually represent a signal’s loudness, or amplitude, as it varies over time at different frequencies. A spectogramm is obtained by computing Fast-Fourier-Transformation on overlapping windowed segments of the signal.
A *mel spectrogram* is a spectrogram where the frequencies are converted to the mel scale (y-axis). The colors represents the amplitude of the signal.

- *MFCCS* :  MFCCs are the coefficients of the Mel-Frequency Cesptrum (MFC) which is a representation of the short-term power spectrum of a sound. Since MFCC features represent phonemes (distinct units of sound), MFCCs are commonly used as features in speech recognition systems. 

- *Chroma*  :  Chroma is a 12-element vector that measures energy from the sound pitch usually in deciBels (dB).

Visualizing the statement "Kids are talking by the door" said by a neutral female voice
<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/image1.png">
</p>

Visualizing mel spectogram of happy, sad, angry and surprise
<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Image2.png">
</p>


2)	See **Modeling.ipynb**:

- *First Step* :  
Conducted feature extraction (log-mel spectrograms) resulting into dataframe (see **mel_24_8.csv**) and built Model with MLP Classifier. Obtained an accuracy score of 13.3% with the model having contrasting results : some emotions are well predicted while some others not all. 

The model has been improved by applying standardization to the data. Accuracy score of 45.5%. Good improvment of our model, though some errors are made i.e angry or fear predicted as happy. 

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Classification_report_1.png">
</p>

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Sample_results_2.png">
</p>

- *Second Step*:  
Conducted extraction of different features, melspectogram, chroma and MFCCS resulting into dataframe (see **mel_chroma_mfccs_24_8.csv**) and built Model with MLP Classifier. Obtained an accuracy score of % with the model having more difficulty classifying the neutral emotion.
Again, I have applied standardization to the data to increase the model performances.

Accuracy Score of 73.3%. Good quality of predictions. However fear and disgust still predicted as happy. The model seems to detected strong emotions but is not able to determine if they are positive or negative emotions.

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Classification_report_2.png">
</p>

- *Third Step*:  
Reduced the dataframe to seven emotions (see **mel_chroma_mfccs_24_7.csv**) and run the MPL Classifier Model. Accuracy score : 73.2% %. The scores of the model have not been improved

The scores of our model have not improved but the prediction of the emotions seems to be more balanced.

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Classification_report_3.png">
</p>

<p align="center">
  <img width="460" height="300" src="https://github.com/diebland/FinalProject__RecognitionSpeechEmotion/blob/main/images/Sample_results_3.png">
</p>


3)	See **Images** for all .png and **Audio** for sample audio files


## Conclusions  

- Possible to explore more feature engineering  
- Consider datas from other sources   
- Implement other classifier models  


## Libraries

List of libraries (with a link to the documentation):

- [Librosa](http://https://librosa.org//"Title")   

- [Pandas](http://https://pandas.pydata.org/"Title")  

- [Numpy](http://https://numpy.org/doc/"Title")   

- [Matplotlib](http://https://matplotlib.org/3.1.1/"Title")  

- [Seaborn](http://https://seaborn.pydata.org/"Title")   

- [Scikit-learn](http://scikit-learn.org/stable/index.html/"Title") 


## Ressources  

- [Visualizing Sounds Using Librosa Machine Learning Library! by Priya Kalyanakrishnan](http://https://www.analyticsvidhya.com/blog/2021/06/visualizing-sounds-librosa///"Title")

- [Understanding the mel spectogram by Leland Roberts](http://https://medium.com/analytics-vidhya/understanding-the-mel-spectrogram-fca2afa2ce53//"Title")

- [Getting to know the mel spectogram by Dalya Gartzman](http://https://towardsdatascience.com/getting-to-know-the-mel-spectrogram-31bca3e2d9d0//"Title")

- [how-i-understood-what-features-to-consider-while-training-audio-files by Joel Jogy](http://https://towardsdatascience.com/how-i-understood-what-features-to-consider-while-training-audio-files-eedfb6e9002b//"Title")

- [Voyage au centre de l'audition](http://http://www.cochlea.eu/son//"Title")




