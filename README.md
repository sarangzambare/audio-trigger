# audio-trigger

### Under Construction


This repository is for trigger-word detection/ digit recognition in speech using recurrent neural networks


Trigger word/ wake word detection is one of the most common applications of sequence models. The goal is to detect instances when a certain word is uttered, and more often than not, recognise the said word from amongst a small pool of "wake words"

In this repository, I demonstrate a GRU network, in combination with 1D Convolution, to detect three words:

**One, Two and Three**

The entire process has the following steps :

1. Generate training dataset with labels.
2. Convert audio files into **spectrograms**
3. Train a combination of 1D Convolution and Recurrent layers to detect utterances.


## Generating training dataset:

All sounds in this project are taken from the [Google speech commands dataset](https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html).

The dataset has 1 sec audio samples of a host of different words, but I will only be audio clips of the words "One", "Two" and "Three" and a combination of some other random words like **"Bird", "Bed", "Happy", "House" which would be labelled as "negative"**

The dataset also has various background noises, like **"Someone doing the dishes", "Cat Meowing", "Running tap"**

All these sounds will be combined in various proportions to generate **10 sec** audio clips of words "One, Two and Three"
superimposed over the background noises, along with the "negatives"


Concurrently, an array of labels will be generated, with each label being a one-hot encoded vector :

```
[1.0, 0.0, 0.0, 0.0] => "One"
[0.0, 1.0, 0.0, 0.0] => "Two"
[0.0, 0.0, 1.0, 0.0] => "Three"
[0.0, 0.0, 0.0, 1.0] => "negative"
```











<intro>





<spectrogram>

<backward looking vs forward looking/ why uni-directional LSTMs>

<convolution for >
