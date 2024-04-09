# Submission Instructions
## How to participate

For the development phase of subtask 1, we provide all participants with the following data:
* the labeled training set containing 'id', 'text', and 'annotations'
* the unlabeled dev set containing 'id' and 'annotations'

You can download the data [add-link](link-tbd)

**note**: do we provide example submissions?

**Goal** of subtask 1 is to solve 4 binary classification tasks on the data and to predict the majority label.

For each submission:
* save your predictions to a separate csv file. The file needs to contain the following columns:
  * 'id': the unique ID of each text, as specified in the dev/test data
  * 'bin_maj': predict 1 if a majority of annotators assigned non-0 (scores 1 - 4), predict 0 if a majority of annotators assigned 0
  * 'bin_one': predict 1 if at least one annotator assigned non-0, 0 otherwise
  * 'bin_all': predict 1 if all annotators assigned non-0
  * 'multi_maj': predict the majority label if there is one
  * 'disagree_bin': predict 1 if there is disagreement between annotators on 0 vs non-0
* compress this csv file into a zip file.
* under My Submissions, fill out the submission form and submit the zip file.

**note**: do we want the data in .csv format?

For the Development Phase, multiple submissions are allowed and they serve the purpose of developing the model.

For the Test Phase, participants may only submit two times, to allow for a mistake in the first submission. Please note that only the latest valid submission determines the final task ranking.

**note**: for EDOS, they restricted the submission in the test phase to 2. Do we want that as well?

## Evaluation

### Evaluation Data

For the Development Phase, systems will be evaluated on the development data labels. For the Test Phase, systems will be evaluated on the test labels. The development data is available [add link](add-link). The test sets will be available as soon as the corresponding test phase starts.

### Evaluation Metrics

TBD

## Submission errors

A submission is successful, if it has the submission status 'finished'. 'Failed' submissions can be investigated for error sources by clicking at '?' next to 'failed' and looking at LOGS > scoring logs > stderr. 
 

