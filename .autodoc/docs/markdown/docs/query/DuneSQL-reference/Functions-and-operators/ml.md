[View code on GitHub](https://dune.com/docs/query/DuneSQL-reference/Functions-and-operators/ml.md)

The app technical guide provides documentation for the machine learning plugin in the Dune Docs project. The plugin provides machine learning functionality as an aggregation function, enabling users to train Support Vector Machine (SVM) based classifiers and regressors for supervised learning problems. The guide covers the following topics:

- Feature vector: To solve a problem with the machine learning technique, it is necessary to represent the data set with the sequence of pairs of labels and feature vectors. A feature vector is represented as a map-type value, whose key is an index of each feature, so that it can express a sparse vector. The guide provides an example of how to construct the feature from the existing numerical values using the `features()` function.

- Classification: Classification is a type of supervised learning problem to predict the distinct label from the given feature vector. The guide provides an example of how to train a classification model using the `learn_classifier()` function and how to use the trained model to predict the label using the `classify()` function. The trained model can not be saved natively and needs to be passed in the format of a nested query.

- Regression: Regression is another type of supervised learning problem, predicting continuous value, unlike the classification problem. The guide provides an example of how to create a model predicting `sepal_length` from the other 3 features using the `learn_regressor()` function and how to use the trained model to predict the target using the `regress()` function.

The guide also provides a list of machine learning functions available in the plugin, including `features()`, `learn_classifier()`, `learn_libsvm_classifier()`, `classify()`, `learn_regressor()`, `learn_libsvm_regressor()`, and `regress()`. Each function is described in detail, including its input and output parameters. The guide also notes that the machine learning functions are not optimized for distributed processing, and the capability to train large data sets is limited by the execution of the final training on a single instance. 

Overall, the guide provides a comprehensive overview of the machine learning plugin in the Dune Docs project, including how to use the plugin to solve classification and regression problems and the available machine learning functions.
## Questions: 
 1. What is the limitation of the machine learning functions in terms of distributed processing?
- The machine learning functions are not optimized for distributed processing, limiting the capability to train large data sets due to the execution of the final training on a single instance.

2. What type of machine learning problems can be solved using this app?
- This app can solve supervised learning problems, specifically classification and regression problems.

3. What is the algorithm used for training the models internally?
- The models are trained internally using libsvm.