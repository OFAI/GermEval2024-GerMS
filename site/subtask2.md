# GermEval2024 GerMS - Subtask 2

IMPORTANT: please note that there is a [closed](closed-track.md) and an [open](open-track.md) track for this subtask!

**Only submissions to the closed track which follow the rules for the closed track qualify for a paper submission and only an accepted paper qualifies for the 
inclusion of your results in the final competition ranking.**

In subtask 2 the goal is to predict the distribution for each text in a dataset where the distribution is  derived from the original distribution of labels assigned by several human annotators. 

The human annotators assigned (according to the [annotation guidelines](guidelines.md) ) 
the strength of misogyny/sexism present in the given text via the following labels:

* `0-Kein`: no sexism/misogyny present
* `1-Gering`: mild sexism/misogyny
* `2-Vorhanden`: sexism/misogyny present
* `3-Stark`: strong sexism/misogyny
* `4-Extrem`: extreme sexism/misogyny

While the annotation guidelines define what kind of sexism/misogyny should get annotated, there has been made no attempt to give rules about how to decide on the strength. For this reason, if an annotator decided that sexism/misogyny is present in a text, the strength assigned is a matter of personal judgement.

The distributions to predict in subtask 2 are
* the binary distribution ('dist_bin'): two values are predicted, which add up to 1.
   * `dist_bin_0`: refers to the portion of annotators labeling the text as 'not-sexist' (`0-Kein`)
   * `dist_bin_1`: refers to the portion of annotators labeling the text as 'sexist' (`1-Gering`, `2-Vorhanden`, `3-Stark`, or `4-Extrem`).
* the multi score distribution ('dist_multi'): five values are predicted, which add up to 1.
   * `dist_multi_0`: predict the portion of annotators labeling the text as `0-Kein`.
   * `dist_multi_1`: predict the portion of annotators labeling the text as `1-Gering`.
   * `dist_multi_2`: predict the portion of annotators labeling the text as `2-Vorhanden`.
   * `dist_multi_3`: predict the portion of annotators labeling the text as `3-Stark`.
   * `dist_multi_4`: predict the portion of annotators labeling the text as `4-Extrem`.

## Data

For the *trial phase* of subtask 1, we provide a small dataset, containing
* a small labeled dataset containing 'id', 'text', and 'annotations' (annotator ids and the label assigned by them)
* a small unlabeled dataset containing 'id', 'text' and 'annotators' (annotator ids)

For the *development phase* of subtask 1, we provide all participants with the following data:
* the labeled training set containing 'id', 'text', and 'annotations' (annotator ids and the label assigned by them)
* the unlabeled dev set containing 'id', 'text' and 'annotators' (annotator ids)

For the *competition phase* of subtask 1, we provide
* the unlabeled test set containing 'id', 'text' and 'annotators' (annotator ids)
  
All of the five files are in JSONL format (one JSON-serialized object per line) where each object is a dictionary with the following 
fields:

* `id`: a hash that identifies the example
* `text`: the text to classify. The text can contain arbitrary Unicode and new lines 
* `annotations` (only in the labeled dataset): an array of dictionaries which contain the following key/value pairs:
  * `user`: a string in the form "A003" which is an anonymized id for the annotator who assigned the label
  * `label`: the label assigned by the annotator
  * Note that the number of annotations and the specific annotators who assigned labels vary between examples
* `annotators` (only in the unlabeled dataset): an array of annotator ids who labeled the example

You can [download](download.md) the data for each phase as soon as the corresponding phase starts.

## Submission

Your submission must be a file in TSV (tab separated values) format which contains the following columns in any order:

* `id`: the id of the example in the unlabeled dataset for which the predictions are submitted
* `dist_bin_0`: prediction of one value between 0 and 1 (all `dist_bin` values need to add up to 1). 
* `dist_bin_1`: prediction of one value between 0 and 1 (all `dist_bin` values need to add up to 1).
* `dist_multi_0`: prediction of one value between 0 and 1 (all `dist_multi` values need to add up to 1).
* `dist_multi_1`: prediction of one value between 0 and 1 (all `dist_multi` values need to add up to 1).
* `dist_multi_2`: prediction of one value between 0 and 1 (all `dist_multi` values need to add up to 1).
* `dist_multi_3`: prediction of one value between 0 and 1 (all `dist_multi` values need to add up to 1).
* `dist_multi_4`: prediction of one value between 0 and 1 (all `dist_multi` values need to add up to 1).

Note that the way how you derive those values is up to you (as long as the rules for the closed or open tracks are followed):

* you can train several models or a single model to get the predicted distribution
* you can derive the mode-specific training set in any way from the labeled training data
* you can use the information of which annotator assigned the label or ignore that

To submit your predictions to the competition:

* the file MUST have the file name extension `.tsv` 
* the TSV file must get compressed into a ZIP file with extension `.zip`
* the ZIP file should then get uploaded as a submission to the correct competition
* !! Please make sure you submit to the competition that corresponds to the correct subtask (1 or 2) and correct track (Open or Closed)!
* under "My Submissions" make sure to fill out the form and:
  * enter the name of your team which has been registered for the competition
  * give a name to your method 
  * confirm that you have checked that you are indeed submitting to the correct competition for the subtask and track desired
 

**note**: do we provide example submissions?

## Phases

* For the *trial phase*, multiple submissions are allowed for getting to know the problem and the subtask.
* For the *development phase*, multiple submissions are allowed and they serve the purpose of developing and improving the model(s).
* For the *competition phase*, participants may only submit a limited number of times. Please note that only the latest valid submission determines the final task ranking.

## Evaluation

System performance on subtask 2 is evaluated using the Jensen-Shannon distance for both (i) the prediction of the binary distribution, and (ii) the prediction of the multi score distribution. We chose the Jensen-Shannon distance as it is a standard method for measuring the similarity between two probability distributions and it is a proper 
distance metric which is between 0 and 1. It is the square root of the Jensen-Shannon divergence, which is based on the Kullback-Leibler divergence. 

The overall score which is used for ranking the submissions is calculated as the unweighted average between the two JS-distances.


## Submission errors and warnings

Always make sure a phase is selected before trying to upload your submission.

A submission is successful, if it has the submission status 'finished'. 'Failed' submissions can be investigated for error sources by clicking at '?' next to 'failed' and looking at LOGS > scoring logs > stderr. 

If you experience any issue such as a submission file stuck with a "scoring" status, please cancel the submission and try again. In case the problem persists you can contact us using the Forum.

Following a successful submission, you need to refresh the submission page in order to see your score and your result on the leaderboard.

