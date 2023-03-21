# SSCIMA
Sequential Sentence Classification in Medical Abstracts


#### Aim
Implement a deep learning model architecture that utilizes NLP techniques to classify the abstracts of RCT(Randomized Controlled Trial) Medical Papers.
Classification into classes of Background, Objective, Method, Result, or Conclusion.

##### 1. Problem Statement

        Over 1 million RCTs have been published so far and around half of them are in PubMed, which makes it challenging for medical investigators to pinpoint the information they are looking for. When researchers search for previous literature, e.g., to write systematic reviews, they often skim through abstracts in order to quickly check whether the papers match the criteria of interest. This process is easier when abstracts are structured, i.e., the text in an abstract is divided into semantic headings such as the objective, method, result, and conclusion. However, over half of published RCT abstracts are unstructured, which makes it more difficult to quickly access the information of interest.


The problem is of Sequential Sentence Classification problem, that is, the classification of short texts that appear in sequences.


##### 2. Technological Area: NLP and Deep Learning
Classical linguistic methods for natural language processing required experts in language defining rules to cover specific cases. These worked in narrow cases but turned out to be fragile. 
Statistical methods improve upon classical linguistic methods by learning rules and models from data rather than requiring them to be specified in a top-down manner. They result in much better performance, but must still be complemented with hand-crafted augmentations by language experts in order to achieve useful results.
Often, a pipeline of statistical methods is required to achieve a single modeling outcome, such as in the case of machine translation.
Deep learning methods are starting to out-compete the statistical methods on some challenging natural language processing problems with singular and simpler models.


Deep learning methods are popular, primarily because they are delivering: 
1. Drop-in Replacement Models
2. New NLP Models
3. Feature Learning
4. Continued Improvement
5. End-to-End Models


Impressive Applications of Deep Learning
1. Automatic Image Caption Generation
2. Automatic Translation of Text
3. Automatic Text Classification


##### 3. Existing Systems
1. Many of the existing text classification techniques like Bag of words, Vector Semantic, Word Embedding, and Probabilistic Language model consider the importance of words individually and not in a long sequence.
2. Techniques like sequence labeling, parsing, and semantics consider a sequence of sentences but do not dive deep into the complex nature and meaning of human languages and their quirks in them.


##### Methodology
1. Getting the data ready
2. Preprocessing the data
3. Feature Engineering
4. Building a model
5. Fitting the data into the model
6. Evaluate the model
7. Improving the model through experimentation
8. Predicting on the saved model


##### Implementation 


Implementation involved building a series of models, starting by getting a baseline, and improving throughout using the NLP and Deep Learning techniques. The models developed in the process are:
1. TF-IDF Multinomial Naive Bayes - A baseline model
2. Conv1D with token embedding
3. Feature Extraction with pre-trained token-embedding
4. Conv1D with character embedding
5. Hybrid Embedding = token embedding + character embedding
6. Transfer learning with pre-trained token embedding + character embedding + positional embedding


##### Results 


Based on the F1 score. Probably explain what is F1 score here.
baseline                                        0.69
custom_token_embed_conv1d                0.80
pretrained_token_embed                        0.74
custom_char_embed_conv1d                0.69
hybrid_char_token_embed                        0.75
tribrid_pos_char_token_embed                0.85


##### Conclusion


We found out that the model with Transfer learning with pre-trained token embedding + character embedding + positional embedding performed well covering a wide range of samples and providing an F1 score of 85% accuracy.


##### Future works
1. Train the model on a bigger and complete dataset
2. Develop interfaces and applications for the usage of the model
3. Classification mechanisms for papers other than Medical research
