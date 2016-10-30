# 1 Representation Methods

**[1]** Levy O, & Goldberg Y. (2014). Dependency-Based Word Embeddings. In Proceedings of the 52nd Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers) (pp. 302–308). inproceedings, Baltimore, Maryland: Association for Computational Linguistics. Retrieved from [here](http://www.aclweb.org/anthology/P14-2050.pdf)

    *    generalize skip-gram model to arbitrary contexts
    *    specifically experiment with syntactic contexts derived from dependency parse trees
    *    key insight - seek vector representations, v_w, such that the dot product, v_w * v_c, with the content vector is maximized for pairs that are good associations
    *    article includes a very nice explanation of the mathematics of the skip-gram approach
