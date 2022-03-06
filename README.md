# IR Project Description

This is Group 14's repository for the Python code used to obtain the results found in the paper. The data used in this project has to be downloaded through the [TREC 2019 Deep Learning Track](https://microsoft.github.io/msmarco/TREC-Deep-Learning-2019.html) page. To execute the code, download the ipython notebook and execute the code in order. Make sure PyTerrier is installed with the following console command:

``
pip install python-terrier
``

``
pip install fastrank
``

``
pip install lightgbm
``

``
pip install --upgrade git+https://github.com/terrierteam/pyterrier_doc2query.git
``

Once these libraries are installed,  the notebook can be used in order to obtain the results described in the paper. <br/>
We present the results in the following table:<br/>
qe=query expansion<br/>
d2q=doc2query (index created from corpus expanded with doc2query)

| Method | NDCG | NDCG@10 | MAP | MRT|
|:------:|:----:|:-------:|:---:|:---:|
|BM25 baseline|0.6047|0.5388|0.3354|140.6|
|BM25-qe(Bo1)|0.6420|0.5681|0.3849|260.5|
|BM25-qe(RM3|0.6483|0.5640|0.3951|420.8|
|BM25-d2q|0.6398|0.5900|0.3652|206.1|
|BM25-qe(Bo1)+d2q|waiting|waiting|waiting|waiting|
|BM25-qe(RM3)+d2q|0.6787|0.6151|0.4213|461.3|
|CoordinateAscent|0.3710|0.3119|0.2679|193.2|
|LambdaMART|0.3479|0.2816|0.2402|196.1|


Below you can find the statistics of the indexes created from the corpus (msmarco document ranking dataset)
and the one created by first expanding the corpus documents using doc2query:

| Measure | Index | Index(doc2query) |
|:-------:|:-----:|:----------------------|
|  #docs  | 3213835 | 3213835 |
| #terms  | 16168096 | 29718814 |
|#postings| 905088837 | 1074683429 |
| #tokens | 2204592607 | 2916542609 |
|build time| 98 min | 116 min |
