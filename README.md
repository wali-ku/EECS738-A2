# EECS-738: Hidden Mark.. M.. (Assignment-2)
**Members**
  - Waqar Ali (2873101)
  - Pushkar Singh Negi (2946319)

The aim of this assignment is to use **H**idden **M**arkov **M**odel (```HMM```) to generate
text based on a given corpus.

All the work we have done for this assignment is fully documented in the
following notebook:
  - [Notebook](notebooks/Markov.ipynb)

The aim of this assignment is to use hidden markov model for text-generation.

**Dataset**: [Shakespeare's Plays](https://www.kaggle.com/kingburrito666/shakespeare-plays)

__Strategy__:
Following strategy is adopted to accomplish the main goal of this assignment:
  - Dataset is loaded into pandas and cleaned; giving a list of all of the player-lines
  - Markov model is built
    - Each line is tokenized
    - First-order and second-order markov chains are built based on tokens
  - A function is written ```(write_line ())``` which, given a word hint, generates a full sentence based on the pre-built markov chains
  - A play of given length is written; by randomly selecting starting words from Shakespeare's plays
  
In order to improve readability, the notebook is divided into sections based on the main task achieved in that section. Each of the section is described below:

## Section-1: Dataset Manipulation
---
The following main goals are achieved in this section:
  - Dataset is loaded
  - Uninteresting lines are deleted from the dataset
  - Lines are converted into a list of string for further processing
  
## Section-2: Hidden Markov Model
---
This section provides helper functions for building the hidden markov model on a text corpus. It is further divided into sub-section to increase modularity.
  - 2.1: Declaration of Global Control Switches
  - 2.2: Helper Functions for Text-Parsing
  - 2.3: Main Function for Building the ```HMM``` Model
  - 2.4: Helper Functions for Using the ```HMM``` Model for Text-Generation
  - 2.5: User API for Predicting Text Given a Sequence of Words

## Section-3: Demonstration
---
In this section, the hidden markov model is used for text-generation. For this purpose, a play of given length is written to demonstrate the correctness as well as extent and limitation of this model. Also the utility of user-API for text-generation given a word sequence is demonstrated.

**ACKNOWLEDGEMENT**: Following source has been used to understand the principles of text-generation using HMM:
  - [Reference](https://medium.com/ymedialabs-innovation/next-word-prediction-using-markov-model-570fc0475f96)
