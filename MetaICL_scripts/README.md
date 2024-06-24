# MetaICL analyze scripts

This directory contains scripts to analyze the effect of context in improving gpt-4's performance using the MetaICL dataset. To download and view the dataset, visit: https://github.com/facebookresearch/MetaICL/tree/main.

Main takeaways from the results:
1. Context with same task demonstrations in each task has smaller embedding distance with the question than context with different task demonstrations.
2. This is a close dataset and the relationship between context embedding distance and performance improvment is postively correlated (different from open dataset)

## List of Files and Directories

### Data_preparation.ipynb: 

A notebook containing scripts to encode the conduct the train_test split and compute the embeddings using "text-embedding-3-large". The train data are used for demonstrations in the context only and the test data are used in the evaluation.

### Inference_and_analysis.ipynb:

A notebook containing scripts to prompt gpt-4 to answer with different context and evaluate them, also conduct analysis and visualization between the relationship between embedding distnace, context types, and performance.
