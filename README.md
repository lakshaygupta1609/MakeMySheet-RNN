**Data Set Used: Maestro(MIDI and Audio Edited for Synchronous TRacks and Organization) is a dataset composed of about 200 hours of virtuosic piano performances captured with fine alignment (~3 ms) between note labels and audio waveforms. It has around 1200 files

Algorithm Used: Recurrent Neural Network**

We trained a model using a collection of Midi files from Maestro Dataset. 
The Model predicts next note in the sequence using recurrent neural network

We use pretty midi library to create and parse MIDI files.
 Pyfluidsynth is used for generating audio playback in Colab.

Steps: 
We used pretty_midi to parse a single MIDI file and inspect the format of the notes.
Further we extract notes & the instruments used
We have used three variables to represent a note when training the model: pitch, step and duration. The pitch is the perceptual quality of the sound as a MIDI note number. The step is the time elapsed from the previous note or start of the track. The duration is how long the note will be playing in seconds and is the difference between the note end and note start times.
Then we Create the training dataset by extracting notes from the MIDI files
We train the model on batches of sequences of notes. Each example will consist of a sequence of notes as the input features, and the next note as the label. In this way, the model will be trained to predict the next note in a sequence.
Now the model is trained!
