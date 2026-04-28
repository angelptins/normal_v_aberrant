# Normal vs Aberrant Classification
This repository detaisl our work on machine learning-based classification of video samples and corresponding pose estimate data into either Normal or Aberrant buckets, according to ground truth diagnosis labels at 2 year follow-ups.

## Steps to Reproduce Results

> git clone https://github.com/angelptins/normal_v_aberrant.git

Download the features (`X_feats.np`) from the Google Drive link below. Access to the data will be granted manually for now.

> https://drive.google.com/file/d/1ffgbQMEwmiTi-i7F7ArfIrW4parGquF5/view?usp=drive_link

The above file contains a numpy array of shape `<1179, 37, 2700>`, corresponding to 1179 video recordings, 37 engineered time series, and 2700 time steps (90 seconds of recording at 30 FPS). The 1179 rows (in the 0th axis of the numpy array) correspond directly to the metadata present in `df_meta_constructed_reindexed.csv`, which has information about patient demographics, recording specifics, and diagnosis status.

Use the `env.yaml` file in this repository to create a conda/mamba environment for development/testing; the environment is also named `normal_v_aberrant`.

Once the repository has been clone and the environment set up, execute the Jupyter notebook to recreate the results we have observed. Experiments are instantiated with global random seeds for the sake of determinism. 

If you do not have a GPU available, this notebook will take a long time to run (hours). For our experiments, we used one RTX A6000, and it took approximately 30 miutes to run 20 trials. Results can also be reproduced using the last few cells and the corresponding files in the `df_metrics` directory. These were output directly from the training process and have not been altered. These files confirm the results presented.

## Details about Pose Estimate Data/Features

## Details about Label Data

## References
