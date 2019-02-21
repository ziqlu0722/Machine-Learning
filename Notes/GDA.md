# Generative Models

Gerative Models are density estimation

## Task: Estimate P(y|x)

This Task of generative models is equivelent to: P(x|y)


According to Bayes Rule: P(y|x1, x2, x3..., xd) = P(x1, x2, x3..., xd|y) * P(y) / P(x1, x2, ..., xd)
* P(x1, x2, ..., xd) is the same for all y, not a factor in ranking P(y|x)
* P(y) is prior, from training counts

## How to Calculate P(x1, x2, ..., xd|y)?

