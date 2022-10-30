# Fake_News_Detection #

## Introduction ##
This repo is about Fake News Detection using Text-RNN, Text-Transformer(BERT, SciBERT, RoBERTA etc.,) Models

I have taken the following paper to implement.
I have splitted this into two phases such as __Phase-1__ and  __Phase-2__

- [x] __Phase-1__ completed

- [ ] __Phase-2__ In-Progress

* Phase-1 :

  * I have re-implemented the base paper with few changes and below are the models being used:

1. Text-RNN
2. Text-Transformers + 5 fold CV, 5 models
3. Text-Transformers + 5 fold CV, 1 model
4. Text-Transformers + 5 fold CV, 5 models, Pseudo Labeling

* Phase-2:

1. Extend the base paper with as a further work, encoder-decoder based models such as T5 can be a good option for further enhancing the prediction results.
2. Get more dataset which includes images, URL and other associated metadata for this problem statement

Base paper link: https://arxiv.org/pdf/2101.02359v1.pdf

### Problem Statement ###
During COVID-19 pandemic, People expressed their perspective about pandemic and its severity in their own way in Internet which leads to panic among many of us.The data sources are social media platforms such as Facebook, Twitter, Instagram. It takes time and effort to figure out what is fake news and what isn’t as the news are circulated in Internet in a rapid pace.  
Like Children we must work our way through something we perceive as fake news. Manually validating all these statements which makes the Individual who is validating will be mentally drainable and exhaustive.

### Dataset & EDA ###


There were totally 9 different datasets has been used for this model building in which 6 are official and 3 were from Internet sources.
To have a better understanding, it is always good to perform EDA extensively to unhide the information pertained by the data in it.


### Methodology ###

There are 2 methodologies proposed by the author:
1.	Text-RNN model based on bi-directional LSTM
2.	Text transformers based on Transformers model

### Experiments ###

Text-RNN: 

Epoch: set to 120; Learning rate: set to 0.01; batch size: set to 40; Text length: set to 140; Drop out rate: set to 0.2. 

The learning rate is multiplied by the attenuation coefficient 0.1 every 30 epochs

Text- Transformers: 

Epoch for each fold: set to 12; batch size: set to 40; Text length: set to 140; Due to model complexity, different training strategy has been followed as below:

1. Label smoothing
2. Learning rate warm up
3. Learning rate cosine decay
4. Domain Pre-training

### Results ###

For detailed result, please refer the respective model .ipynb file for each epochs.

I have provided Google drive link for an abstractive output file for each model

Link : https://drive.google.com/file/d/1CJetbg93Amo2GnRAO6WFqz2jwQKIbid2/view?usp=sharing

Please send me an access request if you wish to view the abstractive output file

### Conclusion ### 

In this paper, the author developed two models by applying different strategies and how each model outperforms the other when applying different strategies of K-fold CV techniques, Pseudo labeling algorithm etc., 
As a further work, encoder-decoder based models such as T5 can be a good option for further enhancing the prediction results.

## Technical Details ##

* All the code has been executed in __Google colab pro+ with TPU__ environment as the models are heavy, Hence reduced the batch size and epochs to overcome the __"ResourceExhaustedError"__ during code run-time


## Credits ##

* __A special thanks to the authors of the above mentioned paper__ :smiley:
* __Another notable mention to my mentor Kavindra Sharma for guiding me through this journey__ :smiley:

