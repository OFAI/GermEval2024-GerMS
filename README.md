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

## LICENSES

All program code in this repo is licensed under the [Apache 2.0 License terms](https://www.apache.org/licenses/LICENSE-2.0)

All data files in this repo are licensed under a [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en) license.

