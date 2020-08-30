<img src="images/broad_logo.png" width="300"/> 

# The KCO Machine Learning Challenge 2020

<img src="images/image.png" width="500"/>   

## Cell classification using Raman spectroscopy


### Introduction
Thank you for your interest in this machine learning challenge! In this challenge, you will build a model for classifing cells exposed to different nutrient concentrations. Individual cells exhibit a variety of states, for example, if they are exposed to high concentration of nutrients vs they are starving. One way to extract the cell state is to look at the cell's [Raman spectrum](https://en.wikipedia.org/wiki/Raman_spectroscopy) (Raman is pronounced *Rah-muhn*). Here, we will provide you with a dataset of Raman spectra emitted by cells fed with different amounts of nutrient. 
Can you predict the nutrient concentration of a cell from its Raman spectrum?

More specifically, we took some cells of the bacterium *E. coli*, which have been divided into four different groups; each group is exposed to a different concentration of the nutrient cAMP (see figure below). We then extracted a bunch of cells from each condition, and for each cell we measured the Raman spectra using a special microscope. The Raman spectrum is a one-dimensional function, $R(k)$, where $k$ is the wavelength (more-or-less the inverse of the frequency - but don't worry: you will not need physics details for the task).

<img src="images/ecoli_states.png" width="300"/>
 
The purpose of this challenge is to pre-screen candidates for a Fall research internship at the Klarman Cell Observatory. We sincerely hope you will partecipate to the challenge!


### Data structure
We have provided the data for this challenge in `data/raman_data.csv`.

The data is formatted as follows:
- Each of the 178 rows contains the group (field `condition` - these are the labels) and Raman spectra of a cell (second column onward - these are the features). 
- Therefore, each row contains 1286 ordered features (the column names correspond to each measured wavelength). 
- The label names are `0mM`, `0.1mM`, `0.5mM`, `1mM` and refer to nutrient concentration (_ie_ `1mM` means that cells are exposed to more nutrient than `0.5mM`). 

### Your submission
**Please submit a Jupyter notebook by Sep 10. The notebook should include a detailed analysis of our data, the machine learning methods you used and your scientific conclusions.**

Consider the following points in your analysis: 

- Load the data from`data/raman_data.csv`. Choose a way to visualize the dataset and describe it.
- Pre-process the data:
    - Some Raman features possess outliers: can you remove them?
    - Only a subset of Raman features are biologically relevant: those whose wavelengths are in between 800 cm^-1 and 1800 cm^-1$. Please restrict your analysis to those features.
    - Make sure you standardize your data (_ie_ zero mean, unit variance) if you use a machine learning model that requires it.
- Train a classifier that predicts the `condition`, given as input the Raman features of a cell.
    - You can use a simple model from an existing library such as sklearn.
    - We would welcome if you coded your own model using a framework such as Keras or PyTorch.
    - Explain what loss function you are using and why.
- Evaluate the performance of yout classifier.
    - Make sure you clearly define in the notebook the training set and the test set (holdout some data for the test set).
    - Which evaluation metric are you using and why? Are you monitoring false negatives and false positives? 
    - When you evaluate your model, we would welcome if you perform a K-fold validation (_ie_ averaging model perfomance over various train/test sets).
- Interpret why the classifier is making decisions.
    - Can you analyze the feature importance? (_ie_ which wavelength is more relevant for classification purposes).
- Build a pairwise classifier (as opposed to the multi-class of the previous point):
    - Build a classifier that distinguishes between _pairs_ of conditions (_eg_ `0mM` vs `1mM`). 
    - Quantify how well the classifier distinguishes each pair: is it easier for the model to distinguish between two similar, or different, nutrient concentrations?
    - Produce a figure that shows your findings.

When you're finished, please place this notebook and any other code you wrote into a zipped folder and e-mail to Tommaso Biancalani <tbiancal@broadinstitute.org>. 

**This challenge was created by Tommaso Biancalani, Shreya Gaddam, Taylor James-Sorenson, and Koseki Kobayashi-Kirschvink**