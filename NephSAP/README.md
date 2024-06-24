# Neph_SAP analyze scripts

This directory contains scripts to analyze the effect of context in improving gpt-4's performance using the Neph_SAP dataset. To view the dataset, visit: https://huggingface.co/datasets/SeanWu25/NEJM-AI_Benchmarking_Medical_Language_Models

The paper for the dataset can be found here: https://arxiv.org/abs/2308.04709

Main takeaways from the results:
1. This is a close dataset and the relationship between context embedding distance and performance improvment is postively correlated (same as MetaICL and different from open dataset)

## List of Files and Directories

### NephSAP.ipynb: 

A notebook containing scripts to conduct train-test split, compute embeddings, prompt for response, evaluate, analyze and visualize the results.


