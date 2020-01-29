****************
* Introduction *
****************

The eSound-Challenge software is a simple patch written in Pd (Pure data), provided to help you with the tasks in the E-Sound Mobility Challenge hackaton. It is aimed to facilitate the exploration and manipulation of sound files according to vehicle driving simulation data. Similarly, it provides simple ways to experiment with different mapping curves, and to render a simulation file according to the challenge guidelines.

The main reasons to use Pd as the programming language chosen are (a) its suitability to deal with audio processing in realtime, (b) its cross-platform capabilities, and (c) that is a relatively easy-to-use language, so you could eventually make variations of the provided tool to adjust it to your needs.


***********************
* Feature description *
***********************

(1) Soundfile management
========================

- Load up to 8 uncompressed audio files (wav or aif) of <=1 second of duration at 44100 Hz (as required by the challenge).
- Files will play in loop continuously
- Perform simple manipulations on the soundfiles:
		- Fill shorter durations with silence (FILL)
		- Adjust the starting point of the loop for reading various soundfiles in sync (OFFSET).
		- Adjust overall volume of each individual soundtrack
		- Mute individual tracks

- Master controls for volume, phase sync and mute
- A high-pass filter has been set to emulate the frequency response of the car loudspeaker.


(2) Car simulation
==================


(3) Transfer functions
======================


(4) Memories and presets
========================

The program offers a way to SAVE and LOAD the state of the tool with all its components to disk (soundfiles, soundfile management, and transfer). For safety, everytime a user saves a state, 10 new files will be created in your system: 
	(1-8) audio files in wav format at 44100/16, exactly as loaded in the tool; 
	(9) a preset file, with the current program-state;
	(10) and a space-separated text file with the transfer functions for velocity-to-pitch, velocity-to-gain and acceleration-to-gain for all 8 soundfiles.

This latter soundfile can be easily imported in any spreadsheet format for further inspection and analysis.

Additionally, all the curves generated with the tool can be stored as presets and loaded anywhere to facilitate the manipulation of the program.


(5) Video simulation and export
===============================



****************
* Installation *
****************

In the following lines we go through the steps you need to follow to get things working properly.

(1) Obtaining Pd
================

To be able to enjoy the complete functionality of the provided tool you need two different versions of Pd running: (a) the latest Pd-vanilla version (as of March 2019, 0.49.1) and (b) a copy of Pd-extended (0.43.4). You can find appropriate versions for your OS in the following links:

	(a) https://puredata.info/downloads/pure-data
	(b) https://puredata.info/downloads/pd-extended

The reason for this unconvenient workaround is to be found in the video rendering extension. Pd is in a moment of transition and that brings some unconsistencies in compatibility with various extensions (something comparable to differences between python 2.x and 3.x). Anyway, we did not want to renounce to some powerful aspects of the most recent Pd version, but this last still lacks of proper integration of video extensions, useful to render and run your deliverable in a single package. It is for this reason 


(2) Getting everything in place in your computer
================================================




That is all for now, remember that I will be around to help with any problems or questions you might have

Have fun!


Ángel Faraldo, March 2019
