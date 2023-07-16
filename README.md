# EEG Signal Analysis

This repository contains code for analyzing an EEG signal. It includes time-frequency analysis with baseline correction, calculation of percentage change between the signal and the baseline, and the application of Inter Trial Phase Consistency (ITPC) on three signal trials.

## Dataset

The UCI HAR Dataset is required for this analysis. Please download the dataset and ensure the following directory structure:

- Train data folder: "E:\\Downloads\\UCIHARDataset\\UCIHARDataset\\train\\Inertial Signals"
- Test data folder: "E:\\Downloads\\UCIHARDataset\\UCIHARDataset\\test\\Inertial Signals"
- Train labels file: "E:\\Downloads\\UCIHARDataset\\UCIHARDataset\\train\\y_train.txt"
- Test labels file: "E:\\Downloads\\UCIHARDataset\\UCIHARDataset\\test\\y_test.txt"

## Libraries

The following libraries are required to run the code:
- NumPy
- Pandas
- Plotly
- Matplotlib
- SciPy
- MNE


## Loading the Signal

The code includes functions to read and load the EEG signal from a specified file. It assumes the data is in a specific format. Modify the functions `read_signals_ucihar` and `read_labels_ucihar` to match the format of your EEG dataset.

## Time-Frequency Analysis with Baseline Correction

The code performs time-frequency analysis on the EEG signal using the Discrete Fourier Transform (DFT). It includes the following steps:
- Splitting the signal into windows of specified size and overlap.
- Applying the DFT on each window and calculating the amplitude spectrum.
- Visualizing the amplitude spectrum using pcolormesh plots.
- Applying baseline correction by subtracting the mean amplitude spectrum from each window.
- Visualizing the baseline-corrected amplitude spectrum.

## Percentage Change Calculation

The code calculates the percentage change between the amplitude spectrum and the baseline for each window. It includes the following steps:
- Subtracting the mean amplitude spectrum from each window.
- Dividing the result by the mean amplitude spectrum and multiplying by 100 to obtain the percentage change.
- Visualizing the percentage change using pcolormesh plots.

## Inter Trial Phase Consistency (ITPC)

The code calculates the Inter Trial Phase Consistency (ITPC) for three signal trials. It includes the following steps:
- Applying the DFT on each trial and calculating the phase spectrum.
- Averaging the phase spectra of the three trials.
- Calculating the absolute value of the average phase spectrum.
- Visualizing the ITPC using pcolormesh plots.
