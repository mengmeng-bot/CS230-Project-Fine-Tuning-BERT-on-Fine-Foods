# Fine-tuning BERT on Fine Foods 

Requirements:
 - pip install tensorflow-gpu==1.5.0
 - pip install tensorflow-bert==1.0.1
 
Download the dataset from Kaggle (requires login) 
 - in particular need to download the Reviews.csv file

Running the project

## Option 1: Without additional in-task pretraining
- create the fine-tuning dataset using [create_fine_tuning_dataset.ipynb](create_fine_tuning_dataset.ipynb)
- fine tune a BERT based classifier on the dataset using [model_finetuning.ipynb](model_finetuning.ipynb)

## Option 2: With additional in-task pretraining
- create the fine-tuning dataset using [create_fine_tuning_dataset.ipynb](create_fine_tuning_dataset.ipynb)
- create the pretraining dataset using the same splits as on the fine-tuining task using [create_in_task_pretraining_dataset.ipynb](create_in_task_pretraining_dataset.ipynb)
- pretrain in-task using [model_pretraining.ipynb](model_pretraining.ipynb)
- fine tune a BERT based classifier on the dataset using [model_finetuning.ipynb](model_finetuning.ipynb)
