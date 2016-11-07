# Unsupervised

## 2011
<a name="Masci2011"></a> J. Masci, U. Meier, D. Cire\csan, J. Schmidhuber, Stacked convolutional auto-encoders for hierarchical feature extraction, in: Int. Conf. Artif. Neural Networks, 2011: pp. 52–59. Retrieved from [here](http://link.springer.com/chapter/10.1007%2F978-3-642-21735-7_7)

    *    Introduces __convolutional auto-encoder__, a hierachical unsupervised feature extractor
    *    Focus specifically on denoising auto-encoder implementaiton, though this is not a necessary constraint
    *    Unlike a fully connected auto-encoder which learn global features, the aim of a Conv-AE is to learn localized features that repeat themselves
    *    Key insight: encoder / decoder weights are fully dependent, specifically the decoder weights are taken as the flip over both dimensions of the encoder weights but with possibly different bias
    *    Implements a max-pooling layer to down-sample (forces a sparse encoded representation) the convolution output
