Problem Description: Fine tune one LLM on custom dataset 

Dataset Acquisition 

Use a dataset of your choice to finetune an open source model (This is an easy dataset used in many examples) https://huggingface.co/datasets/timdettmers/openassistant-guanaco  

Reformat the data according to the model’s template 

Fine tuning: 

Use PEFT, LoRA or QLoRA for fine tuning as full training of the model isn’t feasible with limited resources.  

Please use free tier of Google Colab 

Reduce the VRAM usage, fine-tune the model in 4-bit precision(use QLoRA) 

QLoRA uses a rank of 64 with a scaling parameter of 16, load the model directly in 4-bit precision using NF4  

Load corresponding tokeniser 

Fine tune the model for 5 epochs 

Check the results on tensorboard or any other visualisation that you deem feasible. 

Plot the evaluation and training loss metrics 

Use gradio to create a small chat application for interfacing with the fine tuned LLM 

Write a method for hyperparameter training to optimise the process 

Compare the training loss 

Save the model 

Push the model to hugging face 

Compare the inferences of the models  

Base line model inference 

Fine tuned model inference 

Deliverable 

Inference results from baseline and fine-tuned model 

Model link to hugging face repo with all the files inside the model card including pytorch.bin, safetensors or shards, tokeniser, config.json 

A jupyter notebook with the outputs saved 
