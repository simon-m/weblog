Title: Classification metrics
Date: 2017-11-25 18:55
Modified: 2017-11-25 18:55
Category: Machine learning
Tags: Machine learning, Classification metrics, Precision, Sensitivity, Confusion matrix, Predictive value
Authors: Simon-M
Summary: A sample of the existing classification metrics with their interpretation.


I never seem to remember these basic measures so I made a quick reference.
Of course this is a very incomplete list. A very nice reference is wikipedia's
page about the [confusion matrix](https://en.wikipedia.org/wiki/Confusion_matrix).

Let \\(P\\) and \\(N\\) represent the real positive and negatives and
\\(\\tilde{P}\\) and \\(\\tilde{N}\\) be the predicted positive and negatives.
The following confusion matrix will be our reference:

|                   | \\(P\\) | \\(N\\) |         |
|-------------------|:-------:|:-------:|---------|
| \\( \\tilde P \\) | TP = a  |  FP = b | = a + b |
| \\( \\tilde N \\) | FN = c  |  TN = d | = c + d |
|                   | = a + c | = b + d |         |

## Sensitivity, true positive rate, recall, probability of detection
\\[Sens = \\frac{TP}{P} = \\frac{a}{a+c}\\]
Probability that real positives are predicted as positive: \\(\\mathcal{P}(\\tilde{P} | P)\\).
Intrinsic to the test / classifier.

## Specificity, true negative rate
\\[Sens = \\frac{TN}{N} = \\frac{d}{b+d}\\]
Probability that true negatives are predicted as negatives: \\(\\mathcal{P}(\\tilde{N} | N)\\).
Intrinsic to the test / classifier.

## Positive predictive value, precision:
\\[Sens = \\frac{TP}{\\tilde{P}} = \\frac{a}{a+b}\\]
Probability that postitive predictions are real positives:
\\(\\mathcal{P}(P | \\tilde{P})\\).
Not intrinsic to the test / classifier: a large \\(P\\) compared to \\(N\\) will make
\\(a\\) larger than \\(b\\) independently from the test / classifier ability.

Negative predictive value, precision (note: depends on \\(P\\)):
\\[Sens = \\frac{TN}{\\tilde{N}} = \\frac{d}{c+d}\\]
Probability that negative predictions are real negatives:
\\(\\mathcal{P}(N | \\tilde{N})\\).
Not intrinsic to the test / classifier; also depends on \\(P\\) and \\(N\\) as
illustrated above.


# References

- [https://en.wikipedia.org/wiki/Sensitivity_and_specificity](https://en.wikipedia.org/wiki/Sensitivity_and_specificity)
- [https://en.wikipedia.org/wiki/Positive_and_negative_predictive_values](https://en.wikipedia.org/wiki/Positive_and_negative_predictive_values)
- [https://en.wikipedia.org/wiki/Confusion_matrix](https://en.wikipedia.org/wiki/Confusion_matrix)
