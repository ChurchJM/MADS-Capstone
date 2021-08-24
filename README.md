# Classification of Seismic Events Using Unsupervised Machine Learning
## Capstone Project, Master of Applied Data Science
### University of Michigan
Jeff Church (churchjm@umich.edu) \
Dongdong Yao (dongdony@umich.edu) \
Yihe Huang (yiheh@umich.edu)

This repository contains all the necessary materials to reproduce our machine learning analyses, except for the data files which can be downloaded from [Google Drive](https://drive.google.com/drive/folders/1-Eex84NC7S8D0qj-rliZ34Xw5-PKQuaS?usp=sharing).  All project code is contained in three Jupyter notebooks.

[Project Summary]

### Data Set
The data set available on Google Drive contains the following files and subfolders.
* Labeled EQ and Blasts
  * blasts.list.  The onset times of mining blasts in our labeled dataset.
  * inducedEQ.list.  The onset times of fracking-induced earthquakes in our labeled dataset.
  * Numpy files containing downloaded waveforms, event onset times (Unix timestamps), and STFT spectrograms computed from waveforms.  If missing or deleted, these files are created by the data preparation notebook using the two .list files.
* PhaseNet Picks
  * Four .tar.gz files containing the PhaseNet picks for the years 2013, 2014, 2015, and 2016.  These archives must be extracted before recreating the numpy files in the directory.
  * Numpy files containing downloaded waveforms, event onset times (Unix timestamps), and STFT spectrograms computed from waveforms.  If missing or deleted, these files are created by the data preparation notebook using the contents of the .tar.gz archives.
  * Numpy files containing some intermediate results from the DEC notebook.

**Note:** All of these files may be safely deleted and recreated except for the .list files and .tar.gz archives, which are the "starting point" of the project.  

Please follow these steps to reproduce my capstone project machine learning analyses:
1. Download the full datasets from .
2. Point ROOT_PATH in all three notebooks to the location of the downloaded data folder.
3. If any of the data needs to be re-downloaded or re-processed, run the Capstone_Data_Preparation_(Final).ipynb notebook.  This shouldn't be necessary as the data folder already contains the intermediate data files created by the data preparation notebook.
4. Run the Capstone_Traditional_(Final).ipynb and Capstone_DEC_(Final).ipynb notebooks.  These notebooks are standalone so the order doesn't matter.

All three notebooks were developed in the Google Colab Pro environment, so a GPU is recommended.  Note that even with a GPU, the MNIST section of the DEC notebook can take about an hour to run on its own.
