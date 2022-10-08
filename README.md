# Text-Mining-Pipeline
This is a four part text mining pipeline. 
In the first part, we attempt to perform text normalization and parsing using Bag-of-word on the metadata of 500 articles related to 
book history collected from the ISI Web of Science database. We computed the term frequence - inverse document frequency of the word stem and 
compute the cosine similarity between the titles of the articles.

In the second part, we attempt to examine racial biases of word embeddings using last names as proxies—some last names are more popular among 
certain racial groups than others. 
![Screenshot from 2022-10-07 17-30-51](https://user-images.githubusercontent.com/19349857/194684791-2e3798df-549b-4fb5-9484-de73cd98a790.png)

Also, We use LDA topic models to analyze the Human-Computer Interaction (HCI) research community’s research 
topics over time from title and abstract information for over 4,000 articles published in the CHI conference series (an annual ACM conference for Human-Computer Interaction research) between 1981-2014. The data is not collected by me.

In the third part, I attempt to reproduce Pang et al. (2002)’s experiments with some variations of Unigram and bigram features.

In part 4, I examined Named Entity Recognition (NER) problems on two datasets:
CoNLL2003—a dataset with about 20K annotated sentences from news articles. The entity types include person, location, organization, and miscellaneous. 
TwitterNER—a dataset with about 2.4K annotated sentences from social media posts (tweets) on Twitter. The entity types include person, location, company, facility, movie, music artist,
product, sports team, TV show, and others. 
We train Conditional Random Field (CRF) models on the training set of CoNLL2003 and evaluate the models’ effectiveness of recognizing person and 
location entities on the test set of CoNLL2003 and the TwitterNER dataset.  We train CRF models based on a variety of features:
Word features: we consider the current word and the previous/next words as features.
Prefix/suffix features: we consider the first/last k characters of the current word as prefix/suffix
features (k=3, 4, or 5).
Word shape features: we use the word shape features(X for uppercase
letter, x for lowercase letter, d for digits, and preserve non-alphanumeric characters). We also consider a shortened word shape that collapses 
repeated occurrences of X, x, or d into one. For word and prefix/suffix features, we also consider case-sensitive and case-folding versions of the 
features—the former one reserves letter case differences while the latter does not.
