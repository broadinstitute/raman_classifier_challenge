<img src="images/broad_logo.png" width="300"/>  <img src="images/klarman_logo.png" width="350"/>
# The KCO Machine Learning Challenge 2020

<img src="images/rainbow.png" width="250"/>

## Cell classification using Raman spectroscopy


### Introduction
Thank you for your interest in our machine learning challenge! In this challenge, you will build a model for classifing cells exposed to different nutrient concentrations. Individual cells exhibit a variety of features: some of them determine the *cell type* (*e.g.* liver cells are different than brain cells); some others determine the *cell state* (*e.g.* are cells exposed to high concentration of nutrients or are they starving?). Leveraging AI models to determine the cell state is an essential problem for the construction of a [Human Cell Atlas project](https://www.humancellatlas.org/), which is among the main interests of our lab. 

The purpose of this challenge is to pre-screen candidates for a COOP internship at the Klarman Cell Observatory. We sincerely hope you will join us!

### Challenge Description
Your model will classify E. coli bacteria by their cell state. For this challenge, the E. coli have been divided into 5 different groups of varying concentration of the nutrient [cAMP](https://en.wikipedia.org/wiki/Cyclic_adenosine_monophosphate). Changing the amount of the nutrient will change how other genes are regulated in each cell, putting the five groups into five cell states.

<img src="images/ecoli_states.png" width="200"/>

We'd like to better understand whether spectroscopic features can be used to determine an E. coli cell's state. For this challenge, you will look at [Raman spectroscopy](https://en.wikipedia.org/wiki/Raman_spectroscopy) data (Raman is pronounced *Rah-mon*) as features to predict a cell's nutrient exposure.
 

### Data structure
We've provided all the data for this challenge in `data/raman_data.csv`.

The data is formatted as follows: Each of the rows represents the Raman spectra of one cell as well as its labeled condition. You can think of these condition labels as cell states. Each of the columns are either a Raman feature, a cell label, or other cellular metadata. The Raman features are called wavenumbers.

To complete this challenge, please provide a detailed analysis of this data and use machine learning methods to draw scientific conclusions.

### Your submission
**Please include your main findings in the provided jupyter notebook and make sure to address each of these points:**
- Load and pre-process the spectral data provided (see `data/raman_data.csv`)
- Create a classifier to assign cell state labels to spectral features
- Evaluate the performance of the classifier
- Interpret why the classifier is making decisions
- Clearly state your scientifically-sound conclusions based on the results and visuals
- Once finished, state approximately how long you spent on the challenge (in hours and minutes)


When you're finished, please place this notebook and any other code you wrote into a zipped folder and e-mail to Tommaso Biancalani <tbiancal@broadinstitute.org>. 
