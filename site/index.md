# GermEval2024 Task GerMS

## GermEval2024 Task GerMSL Sexism Detection in German Online News Fora

This shared task is about the detection of sexism/misogyny in comments
posted in (mostly) German language to the comment section of an Austrian
online newspaper. 

The data was originally collected for the development of a classifier 
that supports the human moderators in detecting potentially sexist 
comments or identify comment fora with a high rate of sexist comments.

The texts identified as being sexist are often especially challenging
for automatic classification because they often refer to some implied 
context which is not available or are formulated in a subtle way, avoiding
strong or outright offensive language. 

Texts have been annotated by several human annotators, with a large portion
of the corpus being annotated by at least two annotators out of 7 who 
are forum moderators. 

The main aim of annotating the presence and strength of sexism/misogyny in 
the corpus was to identify comments which make it less welcoming to 
women to participate in the conversation. 
The full annotator guidelines with examples are available in an 
[English translation of the German original](guidelines.pdf)

Since the sexism/misogyny present in this corpus is often present in 
a subtle form that avoids outright offensiveness or curse words, 
there are many texts where annotators have different opinios on whether
the text should be regarded as sexist, or which degree of sexism should
be assigned to it. 

This shared task therefore also provides an opportunity to learn about
how to deal with diverging opinions among annotators and how to train 
models on such a corpus which potentially can also inform about how 
diverging the opinions on a new text might be. 

## Subtasks

The shared task is divided into two subtasks:

* [Subtask 1](subtask1.md): predict a binary label indicating the presence or absence of sexism in different ways, based on the original grading of the texts by several annotators; also predict the majority grading assigned by annotators. 
* [Subtask 2](subtask2.md): predict binary soft labels, based on the different opinions of annotators about the text; predict the distribution of the original gradings by annotators

## Closed and open tracks

Each of the [subtask 1](subtask1.html) and [subtask 2](subtask2.md) competitions 
are organized into two different tracks:

* [Closed Track](closed-track.md): in this track, models can only be trained with the provided training set. Models are limited as to what kind of data for pretraining is allowed. Only the closed track counts towards the competition of the shared task and a closed track submission is required for the submission of a paper. See the linked document for details.
* [Open Track](open-track.md): in this track, anything goes really: you can use language models, use your own training data (but you have to share it with the community) or use other interesting approaches. The open track does NOT count towards the competition ranking but has its own leader board and has been added to allow for the exploration of interesting strategies which may be hard to reproduce. 

 
## Timeline

* **Trial phase**:  April 16 - April 30, 2024
  * A small labeled dataset for training and a small unlabeled dataset to use for the submission are provided. This phase is for getting to know the 
    problem, dataset format, how to submit predictions, how submissions are evaluated and the evaluation shows up on the leaderboard etc. 
* **Development phase**: May 1 - June 6, 2024
  * During this phase, a labeled training set and an unlabeled test set are made available. The training set will contain the updated labeled versions of the 
    training and test set of the previous phase plus additional labeled examples. Submissions have to contain the predictions for the unlabeled test set
    and the evaluation of the submission will sho up on the leaderbord. 
* **Competition phase**: June 7 - June 25, 2024
  * During this phase, the training data will consist of the training data of the previous phase plus the labeled test data of the previous phase 
    and a new unlabeled test set is made available. You can upload the labels for 
    the test set to the competition site and your most last submission will be the one that will be used for ranking. During that phase, the leaderboard is not shown. 
    The final leaderboard/ranking is shown after the end of the competition phase. 
* **Paper submission due**: July 1, 2024
* **Camera ready due**: July 20, 2024
* **Shared Task @KONVENS**: 9 September, 2024

## Organizers

The task is organized by the [**Austrian Research Institute for Artificial Intelligence (OFAI)**](https://ofai.at). The organizing team are:

* [Brigitte Krenn](https://www.ofai.at/~brigitte.krenn/) (brigitte.krenn (AT) ofai.at)
* [Johann Petrak](https://johann-petrak.github.io/) (johann.petrak (AT) ofai.at)
* [Stephanie Gross](https://www.ofai.at/~stephanie.gross/) (stephanie.gross (AT) ofai.at)
