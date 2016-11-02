# Biomedical & Healthcare

## 2015

<a name="Lipton2015"></a>Lipton, Z. C., Kale, D. C., Elkan, C., & Wetzell, R. (2015). Learning to Diagnose with LSTM Recurrent Neural Networks. Retrieved from [here](http://arxiv.org/abs/1511.03677)

    *    aims to classify multivariate timeseries data into one of multiple classes using a LSTM RNN - Notes that some sequence models, such as Markov, conditional random fields, and Kalman filters are ill-equipped to learn long-range dependencies
    *    uses 13 frequently but irregularly sampled clinical measures
    *    associated w/ each patient is a subset of 429 diagnosis codes - though only focus on 128 most common
    *    classify each patient w/ 1 or more diagnosis codes
    *    test a target replication strategy for RNN in order to make a prediction at each time step 
    *    population: 10,401 PICU episodes from Children’s Hospital LA. Episodes vary in length from 12 hours to several months
    *    raw data has missing values and variables (ie a given patient may have no values for a given variable)
    *    data resampled to hourly rate taking the mean measurement within the 1 hour window
    *    use forward and back filling to fill gaps. NOTE: Backfilling passes information from future to the past. This will NOT work for prediction. 
    *    for missing variables - impute clinically normal values as defined by clinical experts
    *    used published tables to correct for differences in variables due to age / gender (Fleming 2011, NHBPEP Working Group 2004)
    *    RNN LSTM with memory cells with forget gates (Gers, 2000b) w/out peephole connections (Gers 2003). output layer is a fully connected layer atop last LSTM layer with element-wise sigmoid. Use log loss as the loss function.

# NLP

## See also

[Socher2011](https://github.com/masinoa/datascience-notes/blob/master/nlp/applied.md#Socher2011)
