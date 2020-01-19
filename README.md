# ZooniverseData

This repository contains two Jupyter notebooks and the datasets that are described in the arxiv paper [HumBug Zooniverse: a crowd-sourced acoustic mosquito datase](https://www.google.com).

The `notebooks` folder contains two files, `metadata.ipynb` contains instructions on how to process and visualise the full dataset  with labels found in `labels/coarse_data_2sec.csv`, with a breakdown of the sources of recordings and the number of labels obtained from the crowdsourcing on Zooniverse. `baseline.ipynb` details an example use, where labels are aggregated from the 2 second overlapping audio recordings, to form a dataset `audio_1sec` found in `data` with its corresponding label `audio_1sec.csv` in `labels`.

The required packages for reproducing the code are given in the first cell of each notebook. This code has been tested in Python 3.


