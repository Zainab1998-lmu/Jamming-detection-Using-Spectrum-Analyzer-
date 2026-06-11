# Jamming-detection-Using-Spectrum-Analyzer-

This repository implements a Decision Tree (DT) algorithm on the processed signal features and simulates the framework described in the thesis ‘Jamming Detection and Classification using Decision Trees for Resource‑Constrained Systems’.

This repository implements a Decision Tree (DT) algorithm on the processed signal features and simulates the framework described in the thesis ‘Jamming Detection and Classification using Decision Trees for Resource‑Constrained Systems’.
<h1>What Does It Do?</h1>
This system is a prototype for detection and classification system.
The system acts as a spectrum monitor to protect spacecraft uplink communications by identifying and classifying Radio Frequency (RF) interference.  
<h1>Why This framework?</h1>
This framework uses:

1. Availability of the Required equipment.
2. Processesing raw signal inputs and utilizing a Decision Tree (DT) Machine Learning classifier to categorize incoming signals into four distinct classes: Clear, Single-Tone Jamming, Gaussian Jamming, or Sweep Jamming. 

The project is structured into two essential sections: the hardware setup configuration and the modular Python software pipeline. 
<h1>The Hardware Setup</h1> 

1. Spectrun Analyzer FPC1500.
2. Personal Computer (PC).
3. Receive Antenna. 
4. Signal Jammer  Source.
5. Walkie-Talkies

<h1>Operational Parameters & Environment</h1> 

- The Center Frequency: 467.57069 MHz, 
- Testing Environment:  a well-controlled lab verificationby placing the receiving antenna and the jamming/source antennas in a fixed line-of-sight configuration to eliminate environmental fading discrepancies. 

<h1>The Python Implementation</h1>
<h3>Prerequisites</h3>

- Python 3.10+
- Virtual environment (recommended)
<h3>Required Software</h3>

- Python 3.10+
- pip (Python package manager)
- Git (for cloning the repository)
<h3>Recommended Tools</h3>

- VS Code or PyCharm (for code editing)
- Terminal/Command Prompt (for running scripts)
<h3>Install Dependencies</h3>

- numpy
- pandas
- matplotlib
- scikit-learn

<h1>Spectrum Analyzer connection + Traces Collection</h1>
From "Collect Traces" File: 

1. Establishes connection to the Spectrum Analyzer 
2. Automates data collection by capturing individual signal traces over short intervals, tracking the highest amplitudes across specified frequency bin regions. The system collects 500 traces per signal type across 9 distinct power variance scenarios. 
<h1>Feature Extraction</h1>
From the " Extracting Features" File: 

Generateing data matrices to extract 4 explicit operational markers from each spectrum trace to build the dataset:  
1. Signal Power ($dB$)
2. Noise Floor ($dB$)
3. SNR ($dB$)
4. Edge Frequency ($Hz$)
<h1>Labeling The classes</h1>
From "Labeling The classes" File: 

Giving label for each signal types:

- Clear For Clear Signals.
- SingleTone For Single Tone Jamming Signals.
- Sweep For Sweep Jamming Signals.
- Gaussian For Gaussian Jamming Signals. 
<h1>Training and Validating The DT Algorithm</h1>
From "Training tDecision Tree algorithm" File.

Training the model with 14,000 distinct samples. 
<h1>Decision Tree Validation</h1>
Validating the model with new dataset, and exporting the classification reports (Precision, Recall, F1 scores) and multi-class heatmapped confusion matrices. 
