# Text classification for topic-specific newspaper collections
Text classification is the process of categorizing text into pre-defined groups. By using Natural Language Processing (NLP) methods, text classifiers can automatically analyze text and then assign a set of given categories based on the research question. This automated classification of text into predefined categories is an important method for managing and processing a large number of newspaper clippings. This also applies to subcorpora for a specific research topic (e.g. migration). The goal of this notebook is to train a model with your previously manually created corpus and use this model to get an overview of the category distribution in your collection (see figure below). Another goal is to organize your classified data for further analysis. This makes it possible, for example, to examine advertising on a specific topic.

This notebook was used with a collection for the case study on emigration and shows how a model can be trained to classify topic-specific collections. For the training/testing corpus, a collection with the keywords "Auswander*", "Ausgewanderte", "Emigrant*", "Emigrierte", "Emigration", "Kolonist*", and "Ansiedler*" (all different German words for emigrants or emigration) have been created. In addition, information on the pre-defined gropus (news, ads, culture...) were added using numbers between one and ten. 

For classification, topic modelling (gensim library) was chosen because it showed the best performance (after experiments with word embeddings or LDA and word embeddings combined). Thanks to the Python package sklearn, it is relatively easy to test different classifiers for a given topic classification task. Logistic regression was chosen as binary classifier. 

*Output graph using an unseen collection on the topic of emigration  (sample of 1631 newspaper clippings).* 

![Collection on the topic of Emigration](images/cat.PNG)


Read more about <a href="https://monkeylearn.com/blog/introduction-to-topic-modeling/" target="_blank">Topic Modeling</a> and <a href="https://towardsdatascience.com/logistic-regression-model-tuning-with-scikit-learn-part-1-425142e01af5" target="_blank">Logistic Regression Model Tuning</a>.

Acknowledgments:

This work has been inspired by a notebook on <a href="https://www.kaggle.com/vukglisovic/classification-combining-lda-and-word2vec" target="_blank">LDA and word embeddings</a> and several other soursces that provided help on how to build models. This work was supported by the European Union's Horizon 2020 research and innovation programme under grant 770299 (NewsEye).
