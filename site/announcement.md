GermEval2024 Shared Task: GerMS-Detect -- Sexism Detection in German Online News Fora
 
CALL FOR PARTICIPATION

10 September 2024 at KONVENS 2024, Vienna, Austria

[https://ofai.github.io/GermEval2024-GerMS/](https://ofai.github.io/GermEval2024-GerMS/)

---- Task description ----

This shared task is about the detection of sexism/misogyny in comments posted in (mostly) German language to the comment section of an Austrian online newspaper. The data was originally collected for the development of a classifier that supports human moderators in detecting potentially sexist comments or identify comment fora with a high rate of sexist comments. The texts identified as being sexist are often especially challenging for automatic classification because they often refer to some implied context which is not available or are formulated in a subtle way, avoiding strong or outright offensive language. The main aim of annotating the presence and strength of sexism/misogyny in the corpus was to identify comments which make it less welcoming to women to participate in the conversation. Since the sexism/misogyny present in this corpus is often present in a subtle form that avoids outright offensiveness or curse words, there are many texts where annotators have different opinios on whether the text should be regarded as sexist, or which degree of sexism should be assigned to it. This shared task therefore also provides an opportunity to learn about how to deal with diverging opinions among annotators and how to train models on such a corpus which potentially can also inform about how diverging the opinions on a new text might be.

The shared task is divided into two subtasks:

Subtask 1: predict a binary label indicating the presence or absence of sexism in different ways, based on the original grading of the texts by several annotators; also predict the majority grading assigned by annotators.

Subtask 2: predict binary soft labels, based on the different opinions of annotators about the text; predict the distribution of the original gradings by annotators

Each of the Subtask 1 and Subtask 2 competitions are organized into two different tracks, a closed track and an open track. In the closed track, models are limited as to what kind of data for pretraining is allowed. Only the closed track counts towards the competition of the shared task and a closed track submission is required for the submission of a paper. In the open track, any additional data or models are allowed. The open track does NOT count towards the competition ranking but has its own leader board and has been added to allow for the exploration of interesting strategies which may be hard to reproduce.

---- Timeline ----

    Trial phase: April 20 - April 29, 2024
    Development phase: May 1 - June 6, 2024
    Competition phase: June 8 - June 25, 2024
    Paper submission due: July 1, 2024
    Camera ready due: July 20, 2024
    Shared Task @KONVENS: 10 September, 2024

---- Organizers ----

The task is organized by the Austrian Research Institute for Artificial Intelligence (OFAI). The organizing team are:

    Brigitte Krenn (brigitte.krenn (AT) ofai.at)
    Johann Petrak (johann.petrak (AT) ofai.at)
    Stephanie Gross (stephanie.gross (AT) ofai.at)



