# Phonotactic Language Model

## About
This repo contains code from Mayer and Nelson (2020) for phonotactic learning with recurrent neural language models.

## Contents
- `src` contains all original code
- `sample_data` contains files for training both feature and embedding models on an IPA transcribed version of the [CMU pronouncing dictionary](https://http://www.speech.cs.cmu.edu/cgi-bin/cmudict), and using fit models to make predictions on the nonce words used in Daland et al (2011). 
  -   `corpora` contains Finnish, Quechua, and English corpora.
  -   `test_data` contains Finnish, Quechua, and English (Daland et al. 2011) test sets.
  -   `features` contains .csv files with featural specifications for Finnish, Quechua, and English. Based on the features from Hayes (2009).
- `notebooks` contains the Jupyter notebook for the class.

## Running the models
Requirements: Python 3.6+ with NumPy and Pytorch (1.0 or later)

Run the Jupyter notebook.
This will fit a 23x64 RNN (there are 23 features specified in `english.csv`) on the CMU dictionary with a 60/40 dev-train split for 10 epochs and create a text file, `Daland_judgements.txt`, which contains the perplexities the fit model assigns to all words listed in `Daland_et_al_IPA.txt`.

The embedding models can be run by omitting the final argument above.



