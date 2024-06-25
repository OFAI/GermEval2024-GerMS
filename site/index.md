## GermEval2024 Shared Task: GerMS-Detect -- Sexism Detection in German Online News Fora

**UPDATE 2024-06-25**

* !! The paper deadline has been extended to July 3rd, 23:59 CET (Central European Time)
* !! The codabench deadline has been extended to June 28th, 23:59 CET
* Clarification: for the competition phase, only the latest 
  of several submissions will be considered, in other words, the one that 
  is showing up on the leaderboard for the subtask. Please make sure that your
  last submitted result is your best one and keep in mind that the total number
  of submissions is limited to 12 in the competition phase.


**UPDATE 2024-05-01**: 

* the **development phase** has started today and the training and test files have been added to the [downloads](download.html).
* the targets file for the trial task has been added to the [downloads](download.html).
* the [source code for the scoring program](https://github.com/OFAI/GermEval2024-GerMS/blob/main/python/scoring.py) is now available. See the [README](https://github.com/OFAI/GermEval2024-GerMS/blob/main/README.md).

**UPDATE 2024-04-30**: please not that we have updated the rules for [open track](open-track.html) and [closed track](closed-track.html) 
and corresponding paper submissions as well as the [terms and conditions](terms.html)

----

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
of the corpus being annotated by at least four annotators out of 10 (7 of whom 
are forum moderators). 

The main aim of annotating the presence and strength of sexism/misogyny in 
the corpus was to identify comments which make it less welcoming to 
women to participate in the conversation. 
The full annotator guidelines with examples are [available](guidelines.html). 

Since the sexism/misogyny present in this corpus is often present in 
a subtle form that avoids outright offensiveness or curse words, 
there are many texts where annotators have different opinions on whether
the text should be regarded as sexist, or which degree of sexism should
be assigned to it. 

This shared task therefore also provides an opportunity to learn about
how to deal with diverging opinions among annotators and how to train 
models on such a corpus which potentially can also inform about how 
diverging the opinions on a new text might be. 

## Subtasks

The shared task is divided into two subtasks:

* [Subtask 1](subtask1.md): predict a binary label indicating the presence or absence of sexism in different ways, based on the original grading of the texts by several annotators; also predict the majority grading assigned by annotators. 
* [Subtask 2](subtask2.md): predict binary soft labels, based on the different opinions of annotators about the text; predict the distribution of the original gradings by annotators.

## Closed and open tracks

Each of the [Subtask 1](subtask1.html) and [Subtask 2](subtask2.md) competitions 
are organized into two different tracks:

* [Closed Track](closed-track.md): in this track, models can only be trained with the provided training set. Models are limited as to what kind of data for pretraining is allowed. Only the closed track counts towards the competition of the shared task and a closed track submission is required for the submission of a paper. See the linked document for details.
* [Open Track](open-track.md): in this track, anything goes: you can use language models, use your own training data (but you have to share it with the community) or use other interesting approaches. The open track does NOT count towards the competition ranking but has its own leader board and has been added to allow for the exploration of interesting strategies which may be hard to reproduce. 

## Codabench Competitions

Before applying for participation in one or more of the Codabench competitions, make sure 
you have read the [terms and conditions](terms.html) and you have also filled out the 
[registration form](https://forms.gle/RBeVviyse2Jy97dK9) for you team.

* Subtask 1
  * [Subtask 1 Closed Track](https://www.codabench.org/competitions/2744)
  * [Subtask 1 Open Track](https://www.codabench.org/competitions/2745)
* Subtask 2
  * [Subtask 2 Closed Track](https://www.codabench.org/competitions/2746)
  * [Subtask 2 Open Track](https://www.codabench.org/competitions/2747)

## Files

The files can be downloaded from the [downloads page](download.html) as they
become available.
 
## Timeline

* **Trial phase**:  April 20 - April 29, 2024
  * A small labeled dataset for training and a small unlabeled dataset to use for the submission are provided. This phase is for getting to know the 
    problem, the dataset format, how to submit predictions, how submissions are evaluated and how the evaluation shows up on the leaderboard etc. 
* **Development phase**: May 1 - June 6, 2024
  * During this phase, a labeled training set and an unlabeled test set are made available. The training set will contain the updated labeled versions of the 
    training and test set of the previous phase plus additional labeled examples. Submissions have to contain the predictions for the unlabeled test set
    and the evaluation of the submission will show up on the leaderbord. 
* **Competition phase**: June 8 - ~~June 25~~ June 28 2024 23:59 CET
  * During this phase, the training data will consist of the training data of the previous phase plus the labeled test data of the previous phase 
    and a new unlabeled test set is made available. You can upload the labels for 
    the test set to the competition site and your latest submission will be the one that will be used for ranking. Please note that only submissions which adhere to all terms and rules are considered for the final ranking.
  * A preliminary final leaderboard/ranking is shown after the end of the competition phase. 
  * The final leaderboard/ranking will be available once paper review and final submission is completed, on July 21th 2024.
* **Paper submission due**: ~~July 1~~ July 3rd, 23:59 CET, 2024
* **Camera ready due**: July 20, 2024
* **[Shared Task @KONVENS](https://konvens-2024.univie.ac.at/)**: 10 September, 2024

## Feedback

If you have questions, if you encounter problems or if you want to give any other feedback for a subtask/trak, please use the corresponding
forum for the Codabench competition (or just any forum if your feedback applies to all of them):

* [Subtask 1 Closed Track Forum](https://www.codabench.org/forums/2662/)
* [Subtask 1 Closed Track Forum](https://www.codabench.org/forums/2663/)
* [Subtask 1 Closed Track Forum](https://www.codabench.org/forums/2664/)
* [Subtask 1 Closed Track Forum](https://www.codabench.org/forums/2665/)

Only if your feedback involves confidential information you do not want to share on one of these forums, contact 
the Organizers directly by email: germeval2024 (AT) ofai (DOT) at

## Organizers

The task is organized by the [**Austrian Research Institute for Artificial Intelligence (OFAI)**](https://ofai.at). The organizing team are:

* [Brigitte Krenn](https://www.ofai.at/~brigitte.krenn/) (brigitte.krenn (AT) ofai.at)
* [Johann Petrak](https://johann-petrak.github.io/) (johann.petrak (AT) ofai.at)
* [Stephanie Gross](https://www.ofai.at/~stephanie.gross/) (stephanie.gross (AT) ofai.at)
