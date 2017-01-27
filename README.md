# Yewno-Task

Approach:
A Naive Bayes (Bernoulli model) classifier is built to classify the author and
title of a given text sample. The classifier is trained on the files in the
corpus, and feature vectors contain information on the words present in each file.

Potential Pitfalls:
-The most time expensive part of the code is reading in the words of each file
to create its unique feature vector. However, the way the code is designed,
new files can be added to the existing model without repeating this expensive
process for files already present in the model.
-Using the files available in NLTK from Project Gutenberg, the code assumes files
are named in the format author-title. Depending on the organization of the corpus
and its filenaming conventions, Named Entity Recognition could be used to extract
the author and title of a file during training to create the class labels.
