# Maximum Entropy Markov Model for Named Entity Recognition
This project is an implementation of a Maximum Entropy Markov Model (MEMM) for Named Entity Recognition (NER). The model is trained and evaluated on the provided dataset, which includes labeled sentences for training and validation.

## Dataset
The dataset consists of two files:

* Training data: eng.train
* Validation data: eng.val

Each file contains sentences where each token is labeled with one of the following tags:

* PER (Person)
* ORG (Organization)
* LOC (Location)
* MISC (Miscellaneous)
* O (Non-entity)
## Model Overview
### Preprocessing
The preprocessing steps involve:

* Replacing all digits in the text with zeros for normalization.
* Loading sentences and splitting them into words and corresponding tags.
* Creating dictionaries and mappings for words and tags based on their frequencies.
### Training
The MEMM is trained using features extracted from each token in the sentences. Features include:

* Word identity
* Part of speech tags
* Capitalization
* Word shape (e.g., lowercase, digits)
* Prefixes and suffixes
The model employs a maximum entropy classifier to calculate the probabilities of transitioning between states (tags) given the observed features. The training process maximizes the likelihood of the tag sequences in the training data.

### Inference
During inference, the Viterbi algorithm is used to find the most likely sequence of tags for a given sentence based on the trained model.

## Results
The results of the model evaluation are printed to the console, including metrics such as precision, recall, and F1-score for each entity type, as well as overall accuracy.


