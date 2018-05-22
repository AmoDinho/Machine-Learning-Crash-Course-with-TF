# FRAMING

## What is Supervised Machine Learning?

input is feed to a model to make valuable predictions on never seen before data.

#### Labels

Is something we try and predict, usually a y variable. Eg: Future price of petrol

#### Features

Are the input variables, ie x var in linear reg. Features can range from x1-xn


**Labeled Data set**
  labeled examples: {features, label}: (x, y)

Think of the following:

housingMedianAge
(feature)
totalRooms
(feature)
totalBedrooms
(feature)
medianHouseValue
(label)


**Unlabeled Dataset**


  unlabeled examples: {features, ?}: (x, ?)
Here is an example:

housingMedianAge
(feature)
totalRooms
(feature)
totalBedrooms
(feature)

## Models

**Define the relationship between features and label:**

Two stages of a models life are Training - show the model labeled examples and make it learn the relationships between features and label.

__Inference__ - applying the trained model to unlabeled examples.  

##### Regression vs. classification

Regression models predict continuous values [What is the value of somethin] while classification predicts discrete values [Either 0 or 1]