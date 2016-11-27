# Biomedical & Healthcare
## 2016
<a name="BeaulieuJones2016"></a>B.K. Beaulieu-Jones, C.S. Greene, Semi-supervised learning of the electronic health record for phenotype stratification, J. Biomed. Inform. 64 (2016) 168–178. Retrieved from [here](http://www.sciencedirect.com/science/article/pii/S153204641630140X) 
code available [here](https://github.com/greenelab/DAPS)

    *    applied denoising autoencoder to simulated EHR data.
    *    also applied to ALS data obtained from Pooled Resource Open-Access ALS Clinical Trials database
		 *     ALS data contains a mix of demographic information, diagnosis history, family history, treatment history, vital sign readings, medications, laboratory values
         *     categorical variables were converted to 1-hot encodings
         *     repeated or temporal measurements were encoded as the mean, min, max, count, stdev, and slope accross each repeat
         *     measurement scales were standardized and input features were normalized to be between 0 and 1 
    *    demonstrated that unsupervised learning by the DA generated distinguishable clusters analagous to population subtypes
    *    classifiers built on the DA output required significatnly fewer labeled examples to achieve optimal performance as compared to classifiers given raw input 
    *    modification to handle missing data: 
	     *     created a missingness vector, M, for each input with value 1 for elements where data is present, 0 otherwise
         *     input sample, x, and reconstructed output, z, were multiplied by M
         *     cross entropy error was divided by the sum of M
         *     eliminates need for imputation 

<a name="choi2016"</a>E. Choi, M.T. Bahadori, E. Searles, C. Coffey, J. Sun, Multi-layer Representation Learning for Medical Concepts, (2016). Retrieved from [here](http://arxiv.org/abs/1602.05568)

    *    objective is to develop dense vector representations of medical concept codes that encode latent information not represented in one-hot coding
    *    challenges assoicated with learning electronic health record (EHR) data representations:
         *    EHR data structured as visits that are temporally ordered but each visit consists of an unordered set of medical codes
         *    there is a desire to make representations interpretable
         *    necessity to scale to large EHR data sets
    *    authors propose Med2Vec algorithm to learn code and visit level representations
         *    demonstrated on two datasets of 3 million and 5.5 million visits
         *    use a multi-layer perceptron architecure with ReLU
              *     output visit layer is trained to predict visit representations for a surrounding context window
              *     intermediate hidden layer is trained to construct code-level representations using skip-gram method
              *     apply a non-negative weight constraint to form a non-negative matrix that allows interpretable features by finding the top k codes that have the largest values for the ith coordinate
              *     generates code representations that are close (by consine similarity) to related concepts 

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

## 2013
<a name="Lasko2013"></a>Lasko, T. A., Denny, J. C., & Levy, M. A. (2013). Computational Phenotype Discovery Using Unsupervised Feature Learning over Noisy, Sparse, and Irregular Clinical Data. PLoS ONE, 8(6), e66341. Retrieved from [here](http://dx.doi.org/10.1371/journal.pone.0066341)

    *    uses Gaussian process (GP) regression to transform raw sparse data into continuous longitudinal data for clinical measurements of uric acid levels 
         *    raw data has irregular points in time separated by interval ranging from hours to years
         *    GP represents a probability density P(f(t)) over a space of arbitrary continuous functions. Thus it is better at capturing non-linear data patterns than the mixed-effects linear regression approach we’re using for Audiogram data
    *    used auto encoder network for unsupervised feature learning over longitudinal serum uric acid measurments
    *    demonstrated learned features useful for classifier that distinguished between gout and leukemia

# NLP
## See also

[Socher2011](https://github.com/masinoa/datascience-notes/blob/master/nlp/theoretical.md#Socher2011)

[Santos2014](https://github.com/masinoa/datascience-notes/blob/master/nlp/theoretical.md#Santos2014)
