In this repo, we have notebooks to fine tune three LLMs (Flan T5-base, Mistral-7B-Instruct-v0.1, and BART) to generate comedic punchlines based on an inputted joke starter.
Files tuneT5, tuneMistral, and tuneBart are notebooks that showcase how we utilized PEFT to tune them on the data found within the Reddit Jokes json.

File MakePunchlines is the notebook that loads the best iterations/versions of the tuned models for punchline generation. Witin MakePunchlines is a cell with list structure joke_headers. You can change the strings in joke_headers and run the notebook. The notebook will generate jokes for each model and load them into a dataframe and csv. MakePunchlines also makes a plot of the training losses for each model at the end. There may need to be some directory changing to load the models and logs for the training losses plot. 

Folder Models contains the several different versions of each model that we tested and manually tuned. Make Punchlines should reference the best version of each: 

Models/google/flan-t5-basev3/checkpoint-1400

Models/mistralai/Mistral-7B-Instruct-v0.1/Mistral-7B-Instruct-v0.1v1

Models/facebook/bart-basev3/checkpoint-1400


