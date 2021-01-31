# Well-Begun-Is-Half-Done

## Datasets and Pre-processing
The Multi-News data can be found in the "Multi-News dataset" directory, which contains the original dataset in "multi-news-original", and 
the pre-processed versions of the dataset truncated at 500 tokens ("multi-news-original-src-cleaned-no-newlinechar-word_tokenizer_500"), and 
at 1000 tokens ("multi-news-original-src-cleaned-no-newlinechar-word_tokenizer_1000"). The pre-processing is performed by the 
"\[1\]Pre-processing Multi-News.ipynb" notebook, which also contains additional details and comments. 


## Models Implementation
The code for this paper is adapted from the publicly available code of [Fabbri et al. (2019)](https://github.com/Alex-Fabbri/Multi-News). We have made slight 
adjustments to some of the OpenNMT files in order to fix minor bugs, or adapt the code for our purposes. The code is located in the "Models code" 
directory. It contains a directory for each of the models used, namely Hi-MAP, Transformer, TextRank, and LexRank. Also, there is a YAML file 
with the Anaconda virtual environment packages and their corresponding versions used.

## Results
The ROUGE scores are calculated with the use of the pyrouge Python package, which is a wrapper of the ROUGE 1.5.5 Perl implementation. Pyrouge 
expects the data in a specific format - each input is in a separate file in a directory named "model_summaries", and each system-generated summary 
is in a separate file in a directory named "system_summaries". The notebook "\[2\]Format files and directories for ROUGE.ipynb" formats all the 
outputs from the models in this way, so that pyrouge can be executed via a short python script. All of the relevant files for the ROUGE calculation
are in the "Results\ROUGE" directory, organized by the model-truncation combinations.
