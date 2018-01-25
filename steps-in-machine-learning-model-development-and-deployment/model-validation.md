#### K-fold cross-validation {#ch07lev2sec24}

K-fold cross-validationis a method of model validation.  It consists of dividing the dataset into  k  subsets of roughly equal size and training  k  models, excluding a different subset each time. The excluded subsets are used as the validation set and the union of all the remaining subsets as the training set.

**For each set of parameters you want to validate, train all k models and calculate the mean error across all k models. Finally, you choose the set of parameters giving you the smallest average error.**

