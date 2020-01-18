# P03-World_Bank_Publications_Topics
## “Identifying Topics in World Bank Publications” | DrivenData Competition


This project was issued as a **Capstone Project** of the **Microsoft Professional Program - Artificial Intelligence Track**, which took the form of a DrivenData competition. The primary goal of such competition was to predict the topic(s) of research publications from the World Bank within 24 topic possibilities and given the first six pages of text from each document/research publication.


**Methodology followed:** Upon initial data exploration, this multilabel classification challenge was approached by building a straightforward model where:
1.	Feature extraction from the text documents (text vectorisation) was achieved by simply counting the individual word occurrences on each document;
2.	Label data was used has provided (i.e. with no pre-processing);
3.	Training was carried out using a “one-vs-the-rest” classifier supported on a “Logistic Regression” estimator;
4.	Performance was measured via the micro-averaged F1 score, as per the competition rules.

To improve model performance, a few experiments were performed comparing different token identification (or feature extraction) options and their combinations, such as “token patterns” via regular expressions, “stop words” and “n_grams”. Still with no satisfactory results, some research was carried out and two “vectorizing” techniques were added to model part one above for comparison– “Tf-idf” and “Hashing”. Also, with the aim of reducing computational time for any of three “vectorizers”, they were all complemented by a dimensionality reduction technique (chi-squared test). The winner ended up being the “Hashing” vectorizer with the best performance score and the shortest computational time. To further improve the performance, a last technique – “feature interaction for sparse matrices” - was added to the best scoring “vectorizer”. This last addition had the model performing at a satisfactory level, (ranking 77th place out of 249 competitors), as such no further improvements were pursued.

It is worth mentioning that due to unavailability on Scikit-learn library, two python objects authored by Peter Brun were used. These are identified on the Jupyter Notebook file attached, together with their source link.


**Problem/challenge type:** NLP, Multilabel classification, Supervised Learning


**Technologies used:** Python (pandas, numpy. matplotlib, itertools, scipy, sklearn), JupyterLab
