# Steps to reproduce

## Step 1
Download dataset **Version 1.0 [526.6MB]** from (https://www.sri.inf.ethz.ch/py150)

## Step 2
to install requirements run 
``` 
pip install -r requirements.txt
``` 
## Step 3
to generate new trees according to the paper run 
```
python generate_new_trees.py -i /PATH/TO/py150/DATASET/python100k_train.json -o /PATH/TO/OUTPUT/FILE/new_python100k_train.json
```
## Step 4
to generate vocabulary according to the paper run
```
python generate_vocab.py -i /PATH/TO/FILE/new_python100k_train.json -o /PATH/TO/OUTPUT/FILE/new_python100k_train.pkl -t ast
```
## Step 5
to generate dataset according to the each model
* trav_trans_plus
```
python models/trav_trans_plus/dataset.py -a /PATH/TO/INPUT/FILE/step3.json -o /PATH/TO/OUTPUT/FILE/step5.txt
```
* trav_trans
```
python models/trav_trans/dataset.py -a /PATH/TO/FILE/step.json -o /PATH/TO/OUTPUT/FILE/step.txt
```
# Step 6
to generate ast ids according to the README.md
```
python models/trav_trans/generate_ast_ids -a /PATH/TO/FILE/step3.json -o /PATH/TO/OUTPUT/FILE/step6.txt
```