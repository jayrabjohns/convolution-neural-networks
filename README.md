# Convolution neural networks

A CNN classifier trained on the MNIST handwritten digits dataset, and comparisons of its results to a collection of other models.

Submitted as coursework in my second year at the University of Bath.

See the [notebook](./Practical6.ipynb) for details.

### Summary
```
Validation set accuracies:
Model           Accuracy          Precision          Recall
CNN:            0.991599977016449 0.9916437978921119 0.9914179170675084
Log Reg:        0.933             0.9329380606771278 0.933
G. Naive Bayes:	0.5404            0.7037573128286942 0.5404
Perceptron:     0.9024            0.9026883320200854 0.9024
```

### Comparison
The CNN model performs the best with an accuracy of >99% on the validation set, along with an impressive precision of >99%. Normally I would suspect some overfitting with a score this high, but these numbers are from evaluating on the validation set, which acts as an intermediary test set. This means it's unlikely that this is a result of overfitting.

Both logistic regression and the single layer perceptron classifiers perform well with an accuracy and precision of above 90%.

Naive Bayes, however, performs very badly with by far the lowest accuracy, precision, and recall.

From the confusion matrices, you can see that both logistic regression and the CNN most commonly misclassify 3s as 5s and 9s as 4s, while perceptron and Naive Bayes seem to most commonly misclassify 9s as 7s.

Overall, the CNN seems to be getting fewer predictions horrifically wrong and is more generally consistent in its success. I imagine this is at least partialy because the CNN model has pooling layers, making it more tolerant to image shift.
