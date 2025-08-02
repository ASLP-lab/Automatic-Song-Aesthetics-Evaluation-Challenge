AUDEEG Challenge ICASSP 2024 Dataset
============================
Data for the [Auditory EEG Decoding challenge](https://exporl.github.io/auditory-eeg-challenge-2023/)

The folder contains multiple folders:  

   1. `split_data(.zip)` contains already preprocessed, split and normalized data; ready for model training/evaluation. 
If you want to get started quickly, you can opt to only download this folder/zipfile.

   2. `preprocessed_eeg(.zip)` and `preprocessed_stimuli(.zip)` contain preprocessed EEG and stimuli files (envelope and mel features) respectively.
At this stage data is not yet split into different sets and normalized. To go from this to the data in `split_data`, you will have to run run_splitting_and_normalization.py, of our code base 

   3. `raw_eeg(_x.zip)` and `stimuli(.zip)` contain the raw EEG and stimuli files. If you want to process the stimuli files, you can run run_preprocessing.py. The processed stimuli files will be stored in the `processed_stimuli`.
Currently, no preprocessing code is made available to preprocess EEG, so you will have to write your own implementation or use the precomputed `processed_eeg` folder.

Make sure to download/unzip these folders into the same folder (e.g. `challenge_folder`).

After downloading the data, get started by cloning the [github code repository](https://github.com/exporl/auditory-eeg-challenge-2023-code) 

