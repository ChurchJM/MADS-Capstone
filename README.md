# Classification of Seismic Events Using Unsupervised Machine Learning
By, Jeff Church

Please follow these steps to reproduce my capstone project machine learning analyses:
1. Download the full datasets from [google drive](https://drive.google.com/drive/folders/1-Eex84NC7S8D0qj-rliZ34Xw5-PKQuaS?usp=sharing).
2. Point ROOT_PATH in all three notebooks to the location of the downloaded data folder.
3. If any of the data needs to be re-downloaded or re-processed, run the Capstone_Data_Preparation_(Final).ipynb notebook.  This shouldn't be necessary as the data folder already contains the intermediate data files created by the data preparation notebook.
4. Run the Capstone_Traditional_(Final).ipynb and Capstone_DEC_(Final).ipynb notebooks.  These notebooks are standalone so the order doesn't matter.

All three notebooks were developed in the Google Colab Pro environment, so a GPU is recommended.  Note that even with a GPU, the MNIST section of the DEC notebook can take about an hour to run on its own.
