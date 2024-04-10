# GermEval2024 GerMS - Subtask 2

For the development phase of subtask 1, we provide all participants with the following data:
* the labeled training set containing 'id', 'text', and 'annotations'
* the unlabeled dev set containing 'id' and 'annotations'

You can download the data [add-link](link-tbd)

**note**: do we provide example submissions?

**Goal** of this subtask are to predict both (i) the binary distribution ('dist_bin'), and (ii) the multi score distribution ('dist_multi'):
  * dist_bin: predict the percentage of annotators choosing sexist ('dist_bin_1') and not sexist ('dist_bin_0')
  * dist_multi: predict the percentage of annotators for each possible label, so a list of 5 values [0,1] for the scores 0 ('dist_multi_0'), 1 ('dist_multi_1'), 2 ('dist_multi_2'), 3 ('dist_multi_3'), 4 ('dist_multi_4')

Both values of 'dist_bin' need to add up to 1 and all 5 values of 'dist_multi' need to add up to 1.

For each submission:
* save your predictions to a separate csv file. The file needs to contain the following columns:
  * 'id': the unique ID of each text, as specified in the dev/test data
  * 'dist_bin_0'
  * 'dist_bin_1'
  * 'dist_multi_0'
  * 'dist_multi_1'
  * 'dist_multi_2'
  * 'dist_multi_3'
  * 'dist_multi_4'
* compress this csv file into a zip file.
* under My Submissions, fill out the submission form and submit the zip file.

**note**: do we want submissions as a .csv file or as a .json file?

For the Development Phase, multiple submissions are allowed and they serve the purpose of developing the model.

For the Test Phase, participants may only submit two times, to allow for a mistake in the first submission. Please note that only the latest valid submission determines the final task ranking.

**note**: for EDOS, they restricted the submission in the test phase to 2. Do we want that as well?

## Submission errors

A submission is successful, if it has the submission status 'finished'. 'Failed' submissions can be investigated for error sources by clicking at '?' next to 'failed' and looking at LOGS > scoring logs > stderr. 


## Evaluation

### Evaluation Data

For the Development Phase, systems will be evaluated on the development data labels. For the Test Phase, systems will be evaluated on the test labels. The development data is available [add link](add-link). The test sets will be available as soon as the corresponding test phase starts.

### Evaluation Metrics

System performance on subtask 2 (both the open and the closed track) is evaluated using the Jensen-Shannon distance for both (i) the prediction of the binary distribution, and (ii) the prediction of the multi score distribution. We chose the Jensen-Shannon distance as it is a standard method for measuring
the similarity between two probability distributions. It is the square root of the Jensen-Shannon divergence, which is based on the Kullback-Leibler divergence, but is symmetric and always has a finite value.

We compute the Jensen-Shannon distance using scipy's spatial distance function. The full evaluation script on CodaBench is available on GitHub [add-link](add-link).

**note**: do we publish the evaluation script when the competition starts or when it has ended?
