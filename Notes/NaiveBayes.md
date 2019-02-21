# Naive Bayes

## Concept
Assume: Feature Independence
P(x1, x2, ..., xd|y) = P(x1|y) * P(x2|y) * ... * P(xd|y)

This assumption doesn't really hold, but Naive Bayes still work in many cases, unless the assumption is completely broken


## How to Calculate the Simple Unidimentional Density Function?
### option 1: Model

apply an imposed model, calculate the maximum likelihood parameters for the model
* gaussian, bernoullim, binomial, exponential
* mixture of distributions

### option 2: Histogram
bucket/cluster/bin and count feature values in each bucket/..., and convert counts into probability

## But there are some defects with Naive Bayes

### problem 1: constant feature
if xj is constant, then some estimates is unusable
solutions:
  1. control the parameters
  2. smoothing, convert the counts into probabilities
  3. feature selection, exclude this feature

### problem 2: zero probability
This situation is common for sparse features, e.g. document data
solution: smoothing


## Two Ways of Smoothing:
M: # of observations
N: # of features
ti: # of observations for the ith feature

P(i): original probability = ti / M

1. Laplace
>> (ti + 1) / (ti + 1)/ (M + N)
  
2. Background + Foreground

>> lambda * P(i) + (1-lambda) * Q(i)
   Q(i): Sumation of tij/Mij over j experiments
         from prior knowledge or preivous experiments
