# Yewno-Task

Approach:
A Naive Bayes (Bernoulli model) classifier is built to classify the author and title of a given text sample. The classifier is trained on the files in the corpus, and feature vectors contain information on the words present in each file.

Testing:
The training data came from the Project Gutenberg files avaliable in NLTK. The test data consisted of a sample (consisting of a few sentences) from each file in the corpus. For evaluation, the accuracy of the classifier for both the training data and test data were printed to stdout. 

Potential Pitfalls:
-Scalability
The time expensive part of the code is reading in the words of each file to create its unique feature vector. However, the way the code is designed, new files can be added to the existing model without repeating this expensive process for files already present in the model.
Possibilities for addressing this scalability issue: 
*Use features other than words present in the document for classification. For instance, document length, average sentence length, vocabulary size, etc.
*Examine the model to determine common words (such as function words) that do not differ drastically in probability across the documents in the corpus. Then redo the model, first stripping these words from the files before training.

-Generalizability
Using the files available in NLTK from Project Gutenberg, the code assumes files are named in the format author-title.txt. Depending on the organization of the corpus and its filenaming conventions, author andtitle may not be so easily identified for each document. Named Entity Recognition could be used to extract the author and title of a file during training to create the class labels.
