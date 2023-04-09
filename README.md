
# 1 - Generala

1. Write a function that takes a number of dices and returns all the possible outcomes
for that amount of dice.

2. Write functions that return, given five dice, True or False if we have Straight, Full,
Poker, or Generala.

3. Compute the probabilities that you already computed by hand by counting the
outcomes describing each roll result in the list of all possible hands served (1st roll).

4. Write a function that simulates a roll with n fair dice.

5. Write a function that plays automatically (max 3 rolls), always looking for a Generala
with a greedy strategy (always keeping the most dices of the same kind and rolling
the others) that returns True if we get a Generala and a False otherwise. Which kind
of distribution follows this function results? Explain your reasoning within the
delivered python notebook.

6. Write a function that plays until it gets a Generala, count how many times it had to
play to get it, and return this number. Which kind of distribution follows this function
results? Explain your reasoning within the delivered python notebook.

# 2 - Gene Expression 

Healthy vs Cancer gene expression

We are performing a study on classical cancer marker genes to know if they influence the
proliferation rate of cells. We follow the division time of healthy and cancer cells and
afterward we perform a proteomic study to see these candidate marker genes' expression.

1. Propose a threshold to classify the cells as "healthy" and "cancer" cells. Perform a t-test to
indicate the significance of your conclusions. Explain carefully what a t-test is and the
conclusions that you have drawn.

2. Construct a model (or more than one) in PyMC3 to test the influence of these marker
genes in proliferation. Try to catch which genes influence and which ones do not, which ones
"trigger" the doubling time when some threshold is surpassed, etc. Explain carefully the
model(s) and your conclusions

# 3 - AirBNB Clustering

Airbnb offers public data about its activities. We will focus on the [file listing the available
apartments](http://insideairbnb.com/get-the-data/).

The user will input a city name and the data should be automatically uploaded to the
notebook.

1) We want to make a classifier that allows us to tell the neighborhood where an apartment
could be located, based on its latitude and longitude coordinates. This functionality is
intended to assign neighborhoods to some apartments where the owner forgot to make it.
To test if the classifier is working, train it with 1000 apartments randomly chosen within the
whole file. Test its accuracy for a test set of apartments (you have to choose its size),
comparing the classification with the real neighborhood of the apartments that you are
testing with. Which is the accuracy of your predictions?

2) We want to clusterize the apartments according to their price and room type (1: shared
room, 2: private room, 3: hotel room, 4: entire apartment). Plotting different amounts of
clusters according to these and other features (neighborhood, availability, minimum nights).

a - Choose two cities and some features and draw some conclusions for them.
Example of a conclusion: If we made three clusters we see that we have the cheap ones,
usually shared rooms in neighborhoods like X; the expensive ones, usually entire
apartments in these places, etc.

b - As a heuristical validation, create fake labels based on your clusterization conclusions
(i.e. 1:cheap, 2:medium, 3:expensive) and see how good you are at classifying apartments
left aside for testing as in exercise 1.

# 4 - Path Analysis

## Version 1 (Data Analysis)

In this assignment we will use the sklearn iris data set, widely used in machine learning. You
have a little description here:
https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html

1) Describe the data set

2) Using pyMC3, we want to infer the parameters of the following models:

a) The mean and standard deviation of the distribution of one feature chosen by
you, that we assume as normally distributed.

b) The Petal Width as linear function of the other three features.

3) Clusterize the plants according to its features and analyze the results of the clusters
as indication of the type of plant.

4) Use a random forest classification and express which is the importance of each
feature to infer the type of plant.

5) Analyze the dependence (or independence) of each one of the features within the
data set.

6) If we assign the following numerical values: Setosa=0, Versicolour=1, and
Virginica=2 and we propose the following causal model:
Sepal Length -> Sepal Width -> Plant Type <- Petal Width <- Petal Length

a) Which relation of independence we should expect between Sepal Length and
Petal Length? Check it.

b) And if we condition on Plant type?

c) And if we condition on Petal Width?

The important thing of this work is that you explain your reasoning, document, graphic
and make me understand with your own words.

## Version 2 (Programming)

Problem 1. Program a function that given a causal graph (in matrix form) computes the
basis set of independences to be checked to assert if that graph is a feasible causal
structure.

Problem 2. Program a function that given a basis set and data for all the variables computes
the independences given the data (using Pearson Correlation) and returns True if the
independences are observed. The threshold of correlation to consider independent or
dependent two variables is a parameter of the function.
Give examples with different graphs and artificially generated data for both exercises.

