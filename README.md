# Overview
*"There's a thin line between likably old-fashioned and fuddy-duddy,and The Count of Monte Cristo . . .never quite settles on either side"*

The Rotten Tomatoes movie review dataset is a corpus of movie reviews used for sentiment analysis,originally collected by Pang and Lee [1].In their work on sentiment treebanks, Socher et al. [2] used Amazon's Mechanical Turk to create fine-grained labels for all parsed phrases in the corpus.This competition presents a chance to benchmark your sentiment-analysis ideas on the Rotten Tomatoes dataset.You are asked to label phrases on a scale of five values : negative,somewhat negative,neutral,somewhat positive,positive.Obstacles like sentence negation,sarcasm,terseness,language ambiguity,and many others make this task very challenging
![Treebank](images/treebank.png)

Kaggle is hosting this competition for the machine learning comunity to use for fun and practice.This competition was inspired by the work of Socher et al [2].You can explore the accompanying website that accompanies the paper:
[nlp.stanford.edu/sentiment/](https://nlp.stanford.edu/sentiment/)

There you will find have source code,a live demo,and even an online interface to help train the model.

[1] Pang and L.Lee.2005.*Seeing stars :Exploiting class relationships for sentiment categorization with respect to rating scales*.In ACL,pages 115-124

[2] *Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank*,Richard Socher,Alex Perelygin,Jean Wu,Jason Chuang,Chris Manning,Andrew Ng and Chriss Potts.Conference on Empirical Methods in NLP (EMNLP 2013).

# Evaluation
Submissions are evaluated on classification accuracy (the percent of labels that are predicted correctly) for every parsed phrase.

# Dataset
The dataset is comprised of tab-separated files with phrases from the Rotten Tomatoes dataset.The train/test split has been preserved for the purposes of benchmarking,but the sentences have been shuffled from their original order.Each phrase has a PhraseId.Each sentence has a SentenceId.Phrases that are repeated (such as short/commond words) are only included once in the data

- train.tsv contains the phrases and their associated sentiment labels.Kaggle have additionally provided a SentenceId so that you can track which phrases belong to a single sentence

- test.tsv contains just phrases.You must assign a sentiment label to each phrase

The sentiment labels are :
0 - negative

1 - somewhat negative

2 - neutral

3 - somewhat positive

4 - positive

- sampleSubmission.csv : sample submission

# Our approach
Our approach is to use TF-IDF to vectorize reviews. Model we use is One versus Rest (a Logistic Regression version)

# Our result
Accuracy = 0,57

