# Raman Classifier Challenge

### Challenge Description:
Thank you for your interest in this challenge! Classifying cells by their cell type and cell state is very pertinent to our lab's work on the [Human Cell Atlas project](https://www.humancellatlas.org/). With the advent of [single-cell sequencing technology](https://en.wikipedia.org/wiki/Single_cell_sequencing) over the past decade, this task has become more feasible than ever before.  Individual cells have a variety of features that determine what *type* of cell they are (e.g. liver cell, brain cell) and also what *state* they're in (e.g. healthy cell, cell under stress, etc.)

Our lab has done a lot of work using genomic and [transcriptomic](https://en.wikipedia.org/wiki/Transcriptome) features to classify cells. In this challenge, we'll consider the use of [Raman spectroscopy](https://en.wikipedia.org/wiki/Raman_spectroscopy) as another set of features. Raman (*pronounced Rah-mon*] spectroscopy extracts a spectral signal from individual cells that may be able to differentiate cells by their cell type and cell state.

We've provided all the data for this challenge in `data/raman_data.csv` and a jupyter notebook named `raman_challenge.ipynb` to write your solutions.

The data is formatted as follows: Each of the rows represents the Raman spectra of one cell as well as its labeled condition. You can think of these condition labels as cell states. Each of the columns are either a Raman feature, a cell label, or other cellular metadata. The Raman features are called wavenumbers.

To complete this challenge, please provide a detailed analysis of this data and use machine learning methods to draw scientific conclusions.  We encourage you to spend **no more than 6 hours** completing this challenge.

**Please include your main findings in the provided jupyter notebook and make sure to address each of these points:**
- Load and pre-process the spectral data provided (see `data/raman_data.csv`)
- Create a classifier to assign cell state labels to spectral features
- Evaluate the performance of the classifier
- Interpret why the classifier is making decisions
- Clearly state your scientifically-sound conclusions based on the results and visuals
- Once finished, state approximately how long you spent on the challenge (in hours and minutes)


When you're finished, please place this notebook and any other code you wrote into a zipped folder and e-mail to <tbiancal@broadinstitute.org>. 
