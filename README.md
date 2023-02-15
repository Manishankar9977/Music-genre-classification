
<h1 align="center">  Music-genre-classification </h1><img align='right'  >

<br/>




 
## DATASET 
 The **GTZAN** genre collection dataset was collected in 2000-2001. It consists of 1000 audio files each having 30 seconds duration. There are 10 classes ( 10 music genres) each containing 100 audio tracks. Each track is in .wav format. 

<p>
<img src ="https://cdn.pixabay.com/photo/2016/10/29/20/58/sound-1781569__340.png" height=200 width=500>
</p>

The dataset has the following folders:
- **Genres original** — A collection of 10 genres with 100 audio files each, all having a length of 30 seconds (the famous GTZAN dataset, the MNIST of sounds)

- **Images original** — A visual representation for each audio file. One way to classify data is through neural networks because NN’s usually take in some sort of image representation.

- **2 CSV files** — Containing features of the audio files. One file has for each song (30 seconds long) a mean and variance computed over multiple features that can be extracted from an audio file. The other file has the same structure, but the songs are split before into 3 seconds audio files.

This dataset can be downloaded from here: [Music-genre-classification dataset](https://www.kaggle.com/code/jvedarutvija/music-genre-classification)


<h2 align="center">Feature Extraction - MFCC</h2>
To perform Audio classification, we first preprocess the data to extract the audio signal's relevant features using <b>MFCC</b> and then pass those important features through the deep neural network for the audio classification. The <b>Mel Frequency Cepstral Coefficients</b> (MFCCs) are short term spectral features of a signal which concisely describe the overall shape of a spectral envelope.
MFCCs extracted from Music-genre-classification dataset: 

<a ><img src="https://editor.analyticsvidhya.com/uploads/64880spectrogram.png"></a>


<h2 align="center"> Neural Networks </h2>
<p>
Neural networks have found profound success in the area of pattern recognition. By repeatedly showing a neural network inputs classified into groups, the network can be trained to discern the criteria used to classify, and it can do so in a generalized manner allowing successful classification of new inputs not used during training. With the explosion of digital music in recent years due to Napster and the Internet, the application of pattern recognition technology to digital audio has become increasingly interesting. 
</p>
<a > <img src = "https://data-flair.training/blogs/wp-content/uploads/sites/2/2020/05/music-genre-classifier-model.jpg" height=200> </a>

<h2 align="center"> Convolutional Neural Networks </h2>
<p>
CNNs or convolutional neural nets are a type of deep learning algorithm that does really well at learning images. To use them for Audio classification we extract features which look like images and shape them in a way in order to feed them into a CNN. We use the <a href="https://librosa.org/doc/latest/index.html">librosa</a> package to do the same. 
</p>
<a> <img src = "https://miro.medium.com/max/800/1*Ahllapa1yWfoLQhyNxE1hg.png" height=150> </a>

<h2 align="center"> Recurrent Neural Networks </h2>
<p>
Recurrent Neural nets are a type of deep learning algorithm that can remember sequences. Audio data tends to follow a pattern which can be exploited using RNNs to classify them.
In contrast to the CNN model's results we decide to use a stateful LSTM thats allows us to simplify the overall network structure. All we need here is the LSTM layer followed by a Dense layer.
</p>
<a> <img src="https://upload.wikimedia.org/wikipedia/commons/9/98/LSTM.png" height=200></a>

## App Link:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://manishankar9977-music-genre-classification-app-p5in0m.streamlit.app/
)


