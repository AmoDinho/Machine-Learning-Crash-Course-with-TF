# Feature Crosses: Encoding Nonlinearity

![Image](images/screenshot-developers.google.com-2018.05.08-14-29-37.png)


# Feature Crosses: Crossing One-Hot Vectors


country:usa AND language:spanish

binned_latitude = [0, 0, 0, 1, 0]   binned_longitude = [0, 1, 0, 0, 0]

binned_latitude X binned_longitude

Different cities in California have markedly different housing prices. Suppose you must create a model to predict housing prices. Which of the following sets of features or feature crosses could learn city-specific relationships between roomsPerPerson and housing price?

One feature cross:
[binned latitude X binned longitude X binned roomsPerPerson]
Crossing binned latitude with binned longitude enables the model to learn city-specific effects of roomsPerPerson. Binning prevents a change in latitude producing the same result as a change in longitude. Depending on the granularity of the bins, this feature cross could learn city-specific or neighborhood-specific or even block-specific effects.

# Regularization for Simplicity
Regularization helps us reduce overfitting and penalize complexity. 

### L₂ Regularization


We now aim to minimize loss + complexity (structural risk minimization). There are two common ways of thinking about model complexity:

As a function of weights of all the features of the model.
a function of the total number of features with nonzero weights.



![Image](images/l.png)
This is how we define a model with its weights.

#### Lambda

Doing L2 Regularization effects the model in the following:
moves weights toward 0
moves mean to weight of 0 as normal distribution. 

Then choosing a lambda value, the goal is to strike the right balance between simplicity and training-data fit:

If your lambda value is too high, your model will be simple, but you run the risk of underfittingyour data. Your model won't learn enough about the training data to make useful predictions.

If your lambda value is too low, your model will be more complex, and you run the risk of overfitting your data. Your model will learn too much about the particularities of the training data, and won't be able to generalize to new data.
Note: Setting lambda to zero removes regularization completely. In this case, training focuses exclusively on minimizing loss, which poses the highest possible overfitting risk.



###### Check your understanding:
Imagine a linear model with 100 input features:
10 are highly informative.
90 are non-informative.
Assume that all features have values between -1 and 1. Which of the following statements are true?


**Answer**
L2 regularization may cause the model to learn a moderate weight for some non-informative features.
Surprisingly, this can happen when a non-informative feature happens to be correlated with the label. In this case, the model incorrectly gives such non-informative features some of the "credit" that should have gone to informative features.

__Second Question__:
Imagine a linear model with two strongly correlated features; that is, these two features are nearly identical copies of one another but one feature contains a small amount of random noise. If we train this model with L2 regularization, what will happen to the weights for these two features?

**Answer** 

Both features will have roughly equal, moderate weights.
L2 regularization will force the features towards roughly equivalent weights that are approximately half of what they would have been had only one of the two features been in the model