# Graph-basedSummarizer
Graph-based Biomedical Text Summarizer

1. Download the source code of the graph-based biomedical text summarizer.
2. Extract the zip file.
3. Download the BERT repository from https://github.com/google-research/bert, and copy the files to the BERT directory already available with the summarizer.
4. Download a BioBERT pretrained model from https://github.com/naver/biobert-pretrained, and copy the files to the BERT directory already available with the summarizer.
5. Copy your input document (preferably a txt file) to the INPUT directory already available with the summarizer.
6. Run the following script:
     - python Summarizer.py -i INPUT_FILE_NAME -o OUTPUT_FILE_NAME -c COMPRESSION_RATE -k TOP_K_SIMILARITY -r RANKING_ALGORITHM
7. Five parameters must be specified when running the script:
     - INPUT_FILE_NAME is the name of input file already copied to the INPUT directory.
     - OUTPUT_FILE_NAME is the name of output file containing the summary that will be created in the OUTPUT directory.
     - COMPRESSION_RATE specifies the size of summary and takes a value in the range (0, 1).
     - TOP_K_SIMILARITY specifies the top K percent of similarity values between sentences that will be used to construct the edges of the graph.
     - RSNKING_ALGORITHM specifies the graph ranking algorithm and takes a value from (pr, hits, ppf)
   
8. After finishing the summarization process, the summary can be found in the OUTPUT directory already available with the summarizer.

<hr>
<b>Note:</b>
A newer version of the summarizer that works with Word2vec and GloVe embeddings will be uploaded by the end of September 2019.
