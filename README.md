# ZooniverseData

This repository contains two Jupyter notebooks and the datasets that are described in the arxiv paper [HumBug Zooniverse: a crowd-sourced acoustic mosquito dataset](https://arxiv.org/abs/2001.04733).

The `notebooks` folder contains two files: `metadata.ipynb` contains instructions on how to process and visualise the full dataset with labels found in `labels/coarse_data_2sec.csv`, with a breakdown of the sources of recordings and the number of labels obtained from the crowdsourcing on Zooniverse. `baseline.ipynb` details an example use, where labels are aggregated from the 2 second overlapping audio recordings, to form a dataset `audio_1sec` found in `data` with its corresponding label `audio_1sec.csv` in `labels`. The baseline is a simple convolutional neural network performing classifications on the log-mel feature space with `librosa`. We supply a simple cross-entropy weighting for taking into account class imbalance.

We strongly recommend using the processed audio in non-overlapping 1 second segments, as the aggregation has been performed for the four recording groups. The votes supplied in `audio_1sec.csv` are given in the categories `{yes, no, not_sure}`.

The data is available to download at [humbug.ac.uk/Zooniverse_audio_1sec.zip] for the 1 second segments, and at [humbug.ac.uk/Zooniverse_audio_2sec.zip] for the overlapping original data. The wave files should be extracted to create the paths: ```ZooniverseData/data/audio_1sec``` and ```ZooniverseData/data/Zoo_segment```.


The required packages for reproducing the code are given in the first cell of each notebook. This code has been tested in:

`Windows 10`
`Anaconda3 5.2.0 Python 3.6`
`keras-gpu 2.3.1` installed via `conda install -c anaconda keras-gpu`


