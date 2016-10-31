# 1 Representation Methods

## 2014 

**[1]** Levy O, & Goldberg Y. (2014). Dependency-Based Word Embeddings. In Proceedings of the 52nd Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers) (pp. 302–308). inproceedings, Baltimore, Maryland: Association for Computational Linguistics. Retrieved from [here](http://www.aclweb.org/anthology/P14-2050.pdf)

    *    generalize skip-gram model to arbitrary contexts
    *    specifically experiment with syntactic contexts derived from dependency parse trees
    *    key insight - seek vector representations, v_w, such that the dot product, v_w * v_c, with the content vector is maximized for pairs that are good associations
    *    article includes a very nice explanation of the mathematics of the skip-gram approach

# 2 Parsing

## 2011
Socher R, Lin CC, Manning C, & Ng AY (2011). Parsing natural scenes and natural language with recursive neural networks. In Proceedings of the 28th international conference on machine learning (ICML-11) (pp. 129–136). Retrieved from [here](http://machinelearning.wustl.edu/mlpapers/paper_files/ICML2011Socher_125.pdf)

    *    map imgage segments / words into a semantic space using a NNet which are then provided as input to a Recursive NNet (RecNet not to be confused with a Recurrent NNet)
    *    RecNet ouputs scores that (a) indicate if neighboring regions should be merged (higher scores indicate merge), (b) a new representation for the merged region and (c) a class label for the new region
    *    An outcome is therefore the representation of phrases/image regions in a dense vector space
    *    Required training set: (a) parsed text, with labels for phrase type (e.g. noun phrase) (b) segmented images with region labels which are object categories (e.g. building)
    *    The cost function is explicitly penalizes for syntactic and class label margin, i.e. semantic information is only implicitly captured
