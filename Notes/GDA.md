# Generative Models

Gerative Models are density estimation of each y.

## Task: Estimate P(y|x)

This Task of generative models is equivelent to: P(x|y)

According to Bayes Rule: P(y|x1, x2, x3..., xd) = P(x1, x2, x3..., xd|y) * P(y) / P(x1, x2, ..., xd)
* P(x1, x2, ..., xd) is the same for all y, not a factor in ranking P(y|x)
* P(y) is prior, from training counts

Below is a cited paragraph from [source link](https://towardsdatascience.com/gaussian-discriminant-analysis-an-example-of-generative-learning-algorithms-2e336ba7aa5c) talkes about the difference between discriminative and generative algorithms

>Generative Learning Algorithms: 
>In Linear Regression and Logistic Regression both we modelled conditional distribution of y given x

>Algorithms that model p(y|x) directly from the training set are called **discriminative algorithms. 

>There can be a different approach to the same problem, consider the same binary classification problem where we want learn to distinguish between two classes, class A (y=1) and class B (y=0) based on some features. Now we take all the examples of label A and try to learn the features and build a model for class A. Then we take all the examples labeled B and try to learn it’s features and build a separate model for class B. Finally to classify a new element, we match it against each model and see which one fits better (generate high value for probability). In this approach we try to model p(x|y) and p(y) as oppose to p(y|x) we did earlier, it’s called **Generative Learning Algorithms.

>Once we learn the model p(y) and p(x|y) using training set, we use Bayes Rule to derive the p(y|x) 

### *All in all, generative approch is to model p(x|y) and p(y) to estimate p(y|x) indirectly based on Bayes Rule, while discriminative algorithm is to model p(y|x) directly

## How to Calculate P(x1, x2, ..., xd|y)?

- Option1: Assume Feature Independence - Naive Bayes
- Option2: Model (restrict the joint distribution) - GDA(gaussian)/EM(mixture)
  - typically with a well known parameterized form
  - estimate the parameters of the imposed model
- Option3: Mix, Bend, Tweak Option 1 and 2 - Bayesian Network/Graphical Model
  - don't fully factorize by independence like Naive Bayes
  - e.g. p(x1|y) * P(x2, x3|y) * P(x4|y)...
  
  
## GDA
### Get Theta that Maximizes the loglikelihood of Data Points (best fits the data)
assumption: data points are independent


