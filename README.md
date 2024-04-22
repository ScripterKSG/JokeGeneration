In this repo, we have notebooks to fine tune three LLMs (Flan T5-base, Mistral-7B-Instruct-v0.1, and BART) to generate comedic punchlines based on an inputted joke starter.
Files tuneT5, tuneMistral, and tuneBart are notebooks that showcase how we utilized PEFT to tune them on the data found within the Reddit Jokes json.

File MakePunchlines is the notebook that loads the best iterations/versions of the tuned models for punchline generation. Witin MakePunchlines is a cell with list structure joke_headers. You can change the strings in joke_headers and run the notebook. The notebook will generate jokes for each model and load them into a dataframe and csv. MakePunchlines also makes a plot of the training losses for each model at the end. There may need to be some directory changing to load the models and logs for the training losses plot.

