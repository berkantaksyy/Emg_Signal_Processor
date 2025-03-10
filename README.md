This code is an EMG (Electromyography) signal processing application. EMG is a technique that measures the electrical activity of muscles and this application is used to filter, analyze and visualize EMG signals. Here are the basic functions of the code and how it works:


1-) LoginWindow 
Purpose: Allows users to log in to the application. 
How does it work? 
-There are user name and password input fields. 
-The username and password are matched against valid predefined credentials. 
-When the correct credentials are entered, access to the EMG processing application is granted. 
-The background image (trial.png) is loaded and displayed.

2-) EMG İşleme Uygulaması (EMGProcessorApp)
Objective: To upload, filter, analyze and visualize EMG signals.
How does it work?

+Muscle Library 
-Contains predefined filtering parameters for different muscle groups (e.g. Biceps Brachii, Quadriceps Femoris). 
-GUI (Graphical User Interface): Users can select muscle category and muscle selection.
-Filtering parameters (lowcut, highcut, envelope, RMS window) can be entered or predefined values can be used.
-Notch filter (50 Hz or 60 Hz) and Q factor adjustable. -FFT (Fast Fourier Transform) and PSD (Power Spectral Density) analysis parameters can be set.
-File Upload: Users can upload TXT or CSV files containing EMG signals.

+Signal Processing
-The loaded signals are processed with notch filter and bandpass filter. 
-RMS (Root Mean Square) envelope is calculated. 
-Frequency analysis (FFT and PSD) is performed.

+Visualization: 
-Graphs of the raw signal, filtered signal, RMS envelope and frequency analysis are plotted.

3-) Signal Processing Functions
-Notch Filter: Used to suppress noise at a specific frequency (for example, 50 Hz mains noise).
-Bandpass Filter: Filters the signal over a specific frequency range (for example, 20-450 Hz).
-RMS Envelope: Calculates the amplitude envelope of the signal, representing muscle activation.
-FFT and PSD: Analyzes the frequency components of the signal.

4-) Visualization Time Domain Graphs
-Raw signal
-Filtered signal
-RMS envelope

5-) Frequency Domain Graphs 
-FFT of raw signal 
-PSD of filtered signal 
-FFT of RMS envelope

6-) Error Management 
-User inputs and errors that may occur during signal processing are captured and the user is informed. 
-Parameters are checked for validity (for example, lowcut < highcut).



