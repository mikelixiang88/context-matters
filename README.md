# Why sometimes in-context learning fails? 

This work explores the challenges inherent to Large Language Models (LLMs) like GPT-4, particularly their propensity for hallucinations, logic mistakes, and incorrect conclusions when answering complex questions. We analyze the effectiveness of different context in improving LLM's performance in different tasks. Our analysis takes place in three different datasets, two of them are from existing closed-form dataset and one from our orignal open-form dataset.

Please note that unlike close-form questions, the open-form questions does not have standard form answers, and are evaluated by our graders manually. A sample interface used by our graders can be found at this link: http://quantumgpt.science:8080/?PROLIFIC_PID=testuser

## Some Insights from our results (More details in each folder)

### Open vs Close: 

Our results reveal that the relationship between embedding distnace of context and performance improvement by context is completely reversed in open-form dataset and closed-form datasets.

### Difficulty and Originality Matters:

Results in our open dataset reveals that gpt-4's response to medium/hard questions and paraphased/orignal questions achieve worse performance than easy/known questions.

### Embedding aligns with perceived relevancy

In the open-form dataset, the embedding distnace between context is highly aligned with the perceived relevancy of context, ie relevant context has smaller distance with question than irrelevant ones.

In both of the closed-form datasets, the context with same task demonstrations have smaller distnace than context with different task demonstrations.


## List of Directories

Each directory contains a seperate README file to explain the different files for processing

### open_dataset: 

This directory contains scripts to analyze results form our original dataset containing difficult physics questions. For each question in the dataset, we promopt gpt-4 with four different levels of context: no_context, irrelevant_context, vague_context, and relevant context. This is an open-form dataset and the results are evaluated by our graders.

### MetaICL_scripts: 

This directory contains scripts to analyze results form the MetaICL dataset. For each question in the dataset, we promopt gpt-4 with three different levels of context: no_context, different_task_demostration, and same_task_demonstration. This is a closed-form dataset and the results are evaluated by code automatically.

### NephSAP: 

This directory contains scripts to analyze results form the NephSAP dataset. For each question in the dataset, we promopt gpt-4 with three different levels of context: no_context, different_task_demostration, and same_task_demonstration. This is a closed-form dataset and the results are evaluated by code automatically.


## Questions

Check our working paper, "Context Matters: Data-Efficient Augmentation of Large Language Models for Scientific Applications" at https://arxiv.org/abs/2312.07069

