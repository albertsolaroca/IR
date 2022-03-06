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

Once these libraries are installed, open the notebook and execute the code in order to see the results obtained in the paper. We present the results in the following table:

| Method | NDCG | NDCG@10 | MAP | MRT|
|:------:|:----:|:-------:|:---:|:---:|
|BM25 baseline|0.6047|0.5388|0.3354|140.6|
