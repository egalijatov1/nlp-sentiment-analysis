# Using Sentiment Multi-label Analysis for MARVEL Character Review

This project describes a model that predicts whether movie text line belongs to one or more emotional classes. After model is trained over one data-set of movie lines, it is used for character analysis of other data-set - MARVEL movie lines. This part includes exploring what emotions characters encounter through a movie. For character analysis dataset of MARVEL movie lines is used, where most important characters are analysed. This model uses features derived from word and char n-grams, parts-ofspeech, word embedding and Opinion Lexicon.

## DATA
- [XED dataset](https://github.com/Helsinki-NLP/XED) consists of emotion annotated movie subtitles (data/en-annotated.tsv).
  Movie lines in this dataset have following distribution:
  ![image](https://user-images.githubusercontent.com/88715320/155518300-441e86e7-4d9a-4833-8082-cce2d61f1b45.png)
- [Marvel Universe dataset](https://github.com/prestondunton/marvel-dialogue-nlp) is created from the transcripts of Marvel Universe movies (data/mcu.csv).
  This dataset contains lines from over 600 characters. In this project only the most important ones are considered:
  ![image](https://user-images.githubusercontent.com/88715320/155518439-9a7a66a5-a6a8-458c-86fb-d7ea447ac33f.png)

- [GloVe](https://www.kaggle.com/rtatman/glove-global-vectors-for-word-representation) - Global Vectors for Word Representation

## METHODS
Two approaches for classification are compared: LinearRegression and LinearSVC (Suport Vector Classifier) classification algorithms. To translate these into multi-label problem, OneVsRestClassifier was used. This estimator uses the binary relevance method, which involves training one binary classifier independently for each label.

## REPORT
In file [Sentiment_multi_label_MARVEL.pdf](https://github.com/egalijatov1/nlp-sentiment-analysis/blob/main/Sentiment_multi_label_MARVEL.pdf) you can find detailed project description. This includes preprocessing and feature extraction as well as presentation of results.
