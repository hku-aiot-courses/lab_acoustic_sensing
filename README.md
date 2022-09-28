# Acoustic Sensing

Acoustic sensing utilize sound as the sensing modality. Soundwaves are passively or impassively sent and received by sound devices. Our main challenge is to extract the useful information from the signals. In our lab, you will learn to use soundwaves (FMCW) on a ranging task. To be exact, we will guide you to implement the algorithm which could detect the distance using acoustic signals.

## Signal Processing Basics (10 points)
This part serves as a supplement for students without knowledge of signal processing. We will briefly introduce CFT, DFT and FFT with visualization. Further more, sampling, windows and zero padding will be mentioned to enhance your understanding of signals. You are required to 
- Implement `show_freq()` function which use FFT to get the frequencies of given signals.

## Play with sounds (10 points)
In this section, we will introduce `sounddevice`, a Python module providing bindings for the PortAudio library and a few convenience functions to play and record NumPy arrays containing audio signals. You will learn how to interact with your on-device microphone and speakers. You are required to 
- Implement a `callback` function which would record the sounds from the speakers of a given audio with definite parameters.
- (Optional with bonus) Implement a recorder which can simultaneously show the recorded waves 

## Generating the FMCW waves (20 points)

We choose FMCW as the sent signals. The definition of it will be first introduced. After implementing the generating modules, you can clearly see the spectrum of FMCW wave. You are encouraged to play the FMCW waves and observe the metrics of it. You are required to
- Implement `fmcw_generator()` with given parameters

## Ranging with acoustic signals (40 points)

We will provide a dataset in this section. This dataset is a received signal of FMCW. After load the dataset, you will see the signals both in time and frequency domain. You will learn a very simple algorithm which can roughly measure the distance. You are required to
- Implement the `fft_raw()` function, where you need to perform FFT on the signals and visualize the outcomes
- Implement the `data_preprocessing()` module, where you are required to filt out the background noise, find the start point, and align with the sent signals
- Implement the `compute_distance()` function, where you shall implement the core of the algorithms and output the distance you measured

## Advanced tasks (Bonus)

In this section, we will provide some clues or hints. You can refer to papers or real industrial applications. You are suggested to
- Change some parameters and enhance the signal processing details
- Collect some dataset by yourself
- Improve the robustness and correctness of the algorithm 
- Transplant your code to mobile devices (e.g. phones or smart speakers) and perform the task on them
- Others (Confirmation needed)