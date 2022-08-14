**Data Set Used: Maestro(MIDI and Audio Edited for Synchronous TRacks and Organization) is a dataset composed of about 200 hours of virtuosic piano performances captured with fine alignment (~3 ms) between note labels and audio waveforms. It has around 1200 files

Algorithm Used: Recurrent Neural Network**

We trained a model using a collection of Midi files from Maestro Dataset. 
The Model predicts next note in the sequence using recurrent neural network

We use pretty midi library to create and parse MIDI files.
 Pyfluidsynth is used for generating audio playback in Colab.


