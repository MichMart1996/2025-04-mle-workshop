# MLE Course 2025-04
## Day 1
- Create a folder named day_1
- in the console run cd day_1 to change the current directory to be day_1
- run uv init --python 3.10
- run uv sync

### let's install the dependencies
- run uv add scikit-learn==1.2.2 pandas pyarrow
- run uv add --dev jupyter seaborn
- run uv add numpy==1.26.4 to fix the issue with sklearn

### let's convert the notebooks to a script
- uv run jupyter nbconvert --to=script notebooks/duration-prediction.ipynb

### let's make the script nicer
see the git commits for the intermediate steps:
- remove top level statements
- make function parameterized

Create a file called Makefile and insert content.
Now we can run training via make train

### add tests
- run uv add pytest
- create a tests folder
- in the test folder create a file test_train.py
- in the folders duration_prediction and tests create empty files named __init__.py
- run pytest
