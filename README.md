## LLMs in Humor Generation.

In this repository, we have notebooks to fine tune three LLMs (**Flan T5-base, Mistral-7B-Instruct-v0.1, and BART**) to generate comedic punchlines based on an inputted joke starter.
Files **tuneT5, tuneMistral, and tuneBart** are notebooks that showcase how we utilized PEFT to tune them on the data found within the Reddit Jokes json. You will need a Hugging Face key to load and run Mistral.

Note that the output shown by these notebooks may not reflect the final model versions used or presented in our paper. We experiemented with several different parameters and dataset preprocessing techniques; we changed the parameters in each cell back to the best parameters but did not rerun the entire notebook with them. We presented only the best results in our paper.

File **MakePunchlines** is the notebook that loads the best iterations/versions of the tuned models for punchline generation. Witin MakePunchlines is a cell with list structure joke_headers. You can change the strings in joke_headers and run the notebook. The notebook will generate jokes for each model and load them into a dataframe and csv. MakePunchlines also makes a plot of the training losses for each model at the end. There may need to be some directory changing to load the models and logs for the training losses plot. 

Due to the size of the model configurations, we were unable to upload them to github. Hence, they were stored externally in a Google Drive. To use the fine-tuned models and access the training logs in the **MakePunchlines** notebook, see

[**Google Drive Folder with all Model Checkpoints**](https://drive.google.com/drive/folders/1NVtKfN_jmsumBkP2It_XhCPaacA9rzB3?usp=drive_link)

### Optimal model versions/checkpoints

- **Flan T5-base**: `/content/drive/MyDrive/Models/google/flan-t5-basev3/checkpoint-1400`
- **Mistral-7B-Instruct-v0.1**: `/content/drive/MyDrive/Models/mistralai/Mistral-7B-Instruct-v0.1/Mistral-7B-Instruct-v0.1v1`
- **BART**: `/content/drive/MyDrive/Models/facebook/bart-basev3/checkpoint-1400`


### Cited code sources

- [Stack Overflow: Export TensorBoard with PyTorch data into CSV with Python](https://stackoverflow.com/questions/71239557/export-tensorboard-with-pytorch-data-into-csv-with-python)
- [Medium: Mistral 7B Fine-Tuning - A Step-by-Step Guide](https://gathnex.medium.com/mistral-7b-fine-tuning-a-step-by-step-guide-52122cdbeca8)
- [Medium: Full Guide to Finetuning T5 for Text2Text and Building a Demo with Streamlit](https://medium.com/nlplanet/a-full-guide-to-finetuning-t5-for-text2text-and-building-a-demo-with-streamlit-c72009631887)
- [Hugging Face Documentation: Transformers Training](https://huggingface.co/docs/transformers/en/training)
