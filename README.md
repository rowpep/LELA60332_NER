 LELA60332_NER
Named Entity Recognition (NER) with Transformer Models

This repository contains code for a NER projectusing transformer based models.

-'Encoder_NER_3_7labels_CL2_F.ipynb': An encoder only model for classification

-'Seq2Seq_NER_3_7labels.ipynb': A sequence-to-sequence model that maps token sequences to label sequences

Both models are trained and evaluated with the same two BIO-tagged dataset.
There are two tagsets:

-Full BIO Tagset: 'B-ORG', 'I-ORG', B-PER', 'I-PER', 'B-LOC', 'I-LOC', 'O'

-Simplififed Tagset: 'B', 'I', 'O'

The data for both models is derived from the Universal Dependencies NER datasets: en_ewt and en_pud. 

Requirments for the models:

-Python 3.7+

-Jupyter Notebook

-Pytorch

-Transformers

-scikit-learn

-pandas

-numpy

Files:

Encover_NER_3_7labels.ipynb

Uses an encoder only model with a token classifier head. Trains using cross-entropy loss. Evaluates with macro F1 scores and unlabelled and labelled span accruacy. Works with both 3 and 7 labels.

Seq2Seq_NER_3_7labels.ipynb

USes a T5 sequence to sequence model. Inputs areprefixed with "ner" for task specification. Outputs are decoded sequences of tags. Evaluates with macroF1 scores and labelled and unlabelled span accuray. Also works with 3 or7 labels. 

Running the notebooks

Each notebook is self contained. The data will download automatically. Seq2Seq model will run for 3 epochs and Encoder will run for 30 epochs. The model is then evaluated on validation and test sets. Access to a GPU is preferred otherwise device type will need to be changed to cpu. 


Reproducibility

Random seeds are fixed to ensure conssitent shuffling.
