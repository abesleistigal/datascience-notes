# General

## 2015
<a name="LeCun2015"></a> LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. Nature, 521(7553), 436–444. Retrieved from  [here](http://www.nature.com/nature/journal/v521/n7553/full/nature14539.html)

    *    Convulotional NNets
         *    dominant approach for recognition & detection tasks - see refs 4, 58, 59, 63-65
         *    word vector representations are now widely used in NLP - see refs 14, 17, 72-76
         *    use dropout for regularization - see ref 62
    *    Recurrent NNets
         *    advances in architecture and training - see refs 79-82
         *    predicting next character or word in a sequence - see refs 75, 83
         *    LSTM addresses difficulty maintaining “long” memory - see refs 78,79
         *    recent proposals to extend memory 
              *    Neural Turing Machine - see ref 88
              *    Associative memory - see ref 89
    *    The future
         *    systems that combine deep learning & reinforcement learning for classification - see ref 99
         *    systems that use RNNs to understand sentences or whole docs - see ref 76, 86

## 2014
<a name="Langkvist"></a> [1] M. Längkvist, L. Karlsson, A. Loutfi, A review of unsupervised feature learning and deep learning for time-series modeling, Pattern Recognit. Lett. 42 (2014) 11–24. Retrieved from [here](http://www.sciencedirect.com/science/article/pii/S0167865514000221)

    *    Characteristics of time-series data that are challenging
         *    noisy
         *    high dimensionality 
         *    no guarantee that the sensor signal contains information necessary to identify target outcome
         *    dependence on previous events could require prohibitive input size
         *    non-stationary processes - i.e. statistical moments change over time 
    *    Unsupervised feature learning & deep learning methods that have been applied
         *    Restricted Boltzmann Machine - standard RBM does not account for time dependence
         *    conditional RBM - modificaiton of RBM that uses auto-regressive weights to model short-term temporal structure
         *    Auto-encoder NNet - standard AE does not account for time dependence
         *    Time-Delay NNet - accounts for time sturcture using convolutions on overlapping input windows
         *    Recurrent neural networks - temporal structure built in via self links in hidden units that connects previous output to current input
    *    Deep learning network: 
    > The goal of a deep network is to build features at the lower layers that will disentangle
    > the factors of variation in the input data and then combine these representations at 
    > higher layers
