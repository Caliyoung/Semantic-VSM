# Semantic-VSM
This repository contains source code for implementing a modified Vector Space Model for retrieving documents based on their semantic relatedness to user queries. The repository includes a small corpus that has Wikipedia and some other files. The files are selected on different themes for simulating and testing the rudimentary concepts of semantic retrieval. Two main folders are in this repository. One holds the implementation resources for the modified VSM and some analysis of its performance. The other folder holds resources for the implementation of the classical VSM on the same dataset. This is done to show the different retrieval capabilities of the two models. Documents are ranked differently by the two models; since the classical model is only capable of  lexical retrievability, our model transforms it into a semantic retrieval model. 

Inside the Modified VSM folder, there are three Python files; each file is an implementation simulated and analysed for a specific query. The queries were formulated to assess the general retrievability of the model and to assess how the techniques employed account for retrieving documents. The same is done in the Classical VSM folder. The results of the two models are compared to establish that modified VSM achieves semantic retrieval of documents while the Classical VSM performs only lexical matches of terms.

It is highly recommended that the codes should be run on Jupyter Notebook. This is because the codes are organised under topics showing the math behind the codes, so that understanding the flow of the code and what each part is doing becomes much easier to follow. 

# Abstract
In this research, we present a modified Vector Space Model which focuses on the semantic relevance of words for retrieving documents. The modified VSM resolves the problem of the classical model performing only lexical matching of query terms to document terms for retrievals. This problem also restricts the classical model from retrieving documents that do not have an exact match of query terms even if they are semantically relevant to the query. In the modified model, we introduced a Query Relevance Update technique, which pads the original query set with semantically relevant document terms for optimised semantic retrieval results. The modified model also includes a novel tf-p which replaces the tf-idf technique of the classical VSM, which is used to compute the Term Frequency Weights. The replacement of the tf-idf resolves the problem of the classical model pinalising terms that occur across documents with the assumption that they are stop words, which in practice, there are usually such words which carry relevant semantic information for documents’ retrieval. We also extended the cosine similarity function with a proportionality weight p_qd, which moderates biases for high frequency of terms in longer documents. The p_qd  ensures that the frequency of query terms, including the updated ones, are accounted for in proportionality with document size for the overall ranking of documents. The simulated results reveal that, the modified VSM does achieve semantic retrieval of documents beyond lexical matching of query and document terms. 
