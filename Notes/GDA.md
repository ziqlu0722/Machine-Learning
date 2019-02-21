# Generative Models

Gerative Models are density estimation

## Task: Estimate P(y|x)

This Task of generative models is equivelent to: P(x|y)


According to Bayes Rule: P(y|x1, x2, x3..., xd) = P(x1, x2, x3..., xd|y) * P(y) / P(x1, x2, ..., xd)
* P(x1, x2, ..., xd) is the same for all y, not a factor in ranking P(y|x)
* P(y) is prior, from training counts

## How to Calculate P(x1, x2, ..., xd|y)?

- Option1: Assume Feature Independence - Naive Bayes
- Option2: Model (restrict the joint distribution) - GDA(gaussian)/EM(mixture)
  - typically with a well known parameterized form
  - estimate the parameters of the imposed model
- Option3: Mix, Bend, Tweak Option 1 and 2 - Bayesian Network/Graphical Model
  - don't fully factorize by independence like Naive Bayes
  - e.g. p(x1|y) * P(x2, x3|y) * P(x4|y)...
  
  
## GDA
### Get Theta that Maximizes the Log likelihood of Data Points


