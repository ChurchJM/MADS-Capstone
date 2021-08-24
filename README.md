# Classification of Seismic Events Using Unsupervised Machine Learning
## Capstone Project, Master of Applied Data Science
### University of Michigan
Jeff Church (churchjm@umich.edu) \
Dongdong Yao (dongdony@umich.edu) \
Yihe Huang (yiheh@umich.edu)

In this project we apply unsupervised machine learning techniques to build a pipeline for automatically extracting and classifying seismic events from continuous seismograms.  Events are automatically identified using the [PhaseNet](https://arxiv.org/abs/1803.03211) phase-picking tool, and separated (e.g. classified) using both traditional machine learning and deep learning based clustering techniques.  In both cases, we validate our modeling choices on a labeled dataset before applying them to the unlabeled PhaseNet events.

This repository contains all the necessary materials to reproduce our machine learning analyses, except for the data files which can be downloaded from [Google Drive](https://drive.google.com/drive/folders/1-Eex84NC7S8D0qj-rliZ34Xw5-PKQuaS?usp=sharing).  All project code is contained in three Jupyter notebooks.

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

All of these files may be safely deleted and recreated except for the .list files and .tar.gz archives, which are the "starting point" of the project.  

### Jupyter Notebooks
1. Capstone_Data_Preparation_(Final).npy.  This notebook prepares the waveforms and spectrograms described above.  It's not necessary to run this notebook if nothing has been deleted from the downloaded data files.
2. Capstone_Traditional_(Final).npy.  Contains the traditional machine learning analyses.
3. Capstone_DEC_(Final).npy.  Contains the deep learning analyses.

*The traditional machine learning and deep learning notebooks are standalone and may be run in any order, assuming all data is present.*

Minimal setup should be required to run the notebooks in your environment.  First, point the ROOT_PATH variable found in each notebook to the data folder downloaded from Google Drive.  Second, unless you plan to upload the notebooks to Google Colab, remove the drive mounting cell.  Everything else should work out of the box.  All notebooks were developed using the Google Colab Pro environment, so a GPU us recommended.  Note that even with a GPU, the MNIST section of the DEC notebook can take about an hour to run on its own.
