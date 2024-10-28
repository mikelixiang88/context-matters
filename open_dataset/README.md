# Open-form Question Dataset

This dirrectory contains the scripts to perform preparation, prompting, analysis and visualization based on our open-form dataset containing challenging physics questions. Here are a few insights suggested by our results here:

1. The trends in the grading given by different graders can be vastly different
2. Embedding distance between context and questions are highly aligned with perceived relevancy.
3. There is a negative correlation between embedding distance between context and question, and the performance improvement (standardized and aggregated from individual grader) by the context.
4. Harder / More original questions receives worse performance than easy/known questions.



## List of Files and Directories

### Embedding: 

A directory that holds scripts to compute the embedding of questions and contexts via the "text-embedding-3-large" model.
The cosine distance between questions and contexts, and questions and response are calculated.
For embedding of no context, we use a space as placeholder (empty string returns error), this embedding is not meaningful. 
Move files in input_files out, and execute Reformat_data.ipynb, Prep_context.ipynb, generate_embedding.ipynb, and Calculate_distance.ipynb in order to recreate the files in results.

### Answer_generator.ipynb:

A notebook containing scripts to encode the questions and prompt gpt-4 to respond with different context.

### Auto_grader.ipynb:

A notebook containing scripts to prompt gpt-4 to evaluate the response base on ground truth answer.

### embedding_analysis.ipynb:

A notebook containing scripts that analyze the results computed by the scripts inside the Embedding folder. This script visualizes the relationship between different context and embedding distnace, as well as embedding distance and performance improvement.

### standardize_analysis.ipynb

A notebook containing script to visualize the relationship between different context and performance across different graders, difficulty, and originality.

### Faithfulness: 

A directory that holds scripts that repeats the experiment with a different prompt template. The script then measures the faithfulness score of the newly generated response against the original ones as a similiarity measure.


