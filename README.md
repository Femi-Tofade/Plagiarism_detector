# Plagiarism Detector Project

## Project Overview <a name="project_overview"></a>

In this project, a plagiarism detector is deployed using Amazon SageMaker and PyTorch using the [Corpus of Plagiarised Short Answers](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html) by Paul Clough and Mark Stevenson at the University of Sheffield. The plagiarism detector examines a text file and performs binary classification; labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text.

## File Descriptions <a name="files"></a>

### Folders: 
**data:** contains the original data [Corpus of Plagiarised Short Answers](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html)

**notebook_ims:** contains the images used in the notebooks

**plagiarism_data:** contains the preprocessed and cleaned data with selected engineered features

**source_pytorch:** contains the model and train functions when using a pytroch model

**source_sklearn:** contains the train fuctions when using a sklearn model

### Files:
**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.

**Notebook 2: Feature Engineering**
* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**
* Upload train/test feature data to S3.
* Define a binary classification model and a training script.
* Train the model and deploy it using SageMaker.
* Evaluate the deployed classifier.

**helpers.py: functions used in the notebooks**

**problem_unittests.py: unit tests for the notebooks**

## Licensing, Authors, and Acknowledgements<a name="licensing"></a>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Acknowledge to [Udacity](https://www.udacity.com/) and to Paul Clough and Mark Stevenson for the data [Corpus of Plagiarised Short Answers](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html).  

Please see the [README](https://github.com/udacity/ML_SageMaker_Studies/tree/master/README.md) in the root directory for instructions on setting up a SageMaker notebook and downloading the project files (as well as the other notebooks).
