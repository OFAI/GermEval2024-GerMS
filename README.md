# GermEval2024-GerMS

This repo contains:

* The public web page sources for the [GermEval2024 GerMS-Detect Shared Task](https://ofai.github.io/GermEval2024-GerMS/)
* Code and other information related to the shared task


## Scorer

The source code for the scorer used in the shared task is in 
[python/scoring.py](python/scoring.py)

The scorer can be tested with the targets and sample submissions for subtasks 1 and 2:

```
# run the scorer for the subtask 1 sample submission
python python/scoring.py --st 1 --reference-dir test/trial/targets/ --submission-dir test/trial/submission-st1-01/

# run the scorer for the subtask 2 sample submission
python python/scoring.py --st 2 --reference-dir test/trial/targets/ --submission-dir test/trial/submission-st2-01/
```


