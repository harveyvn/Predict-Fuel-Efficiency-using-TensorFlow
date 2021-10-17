# Predict Fuel Efficiency using TensorFlow
Use the Auto MPG dataset from UCI Machine Learning Repository to predict the fuel efficiency using a basic regression with TensorFlow.
You can see the live version of my notebook on [Kaggle](https://www.kaggle.com/theblackwood/predict-fuel-efficiency-using-tensorflow/notebook).

This tutorial uses the Auto MPG dataset and demonstrates how to build different ML models to predict the fuel efficiency of the late-1970s and early 1980s automobiles. This description includes attributes like mpg, cylinders, displacement, horsepower, weight, acceleration, model year, origin, and car name.

Some techniques applied in this notebook:
- Correlation map to see how features are correlated with each other and with ```mpg```.
- Split the data into training and test sets with ```scikit-learn```.
- Handle missing values with SimpleImputer by replacing missing values with the mean value and create a new column ```hp```.
- Handle categorical variables by using one-hot encode the values in the column with OneHotEncoder class from ```scikit-learn```. 
- Normalize features that use different scales and ranges by ```tf.keras.layers.Normalization```.

Results:
- A benchmark table compares the performance of different ML models such as linear regression model of every single feature, linear regression of multi features and a deep neural network to decide which one is the best.

![Benchmark Table](https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/benchmark.jpg)
