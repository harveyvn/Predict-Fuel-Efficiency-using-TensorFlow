# Predict Fuel Efficiency using TensorFlow
Use the Auto MPG dataset from UCI Machine Learning Repository to predict the fuel efficiency using a basic regression with TensorFlow.
A live version of this notebook is available on [Kaggle](https://www.kaggle.com/theblackwood/predict-fuel-efficiency-using-tensorflow/notebook).

This tutorial uses the Auto MPG dataset and demonstrates how to build different ML models to predict the fuel efficiency of the late-1970s and early 1980s automobiles. This description includes attributes like mpg, cylinders, displacement, horsepower, weight, acceleration, model year, origin, and car name.

![Dataset Preview](https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/dataset.jpg)

Some techniques applied in this notebook:
- Transforming the targets with Box-Cox transformation before learning any linear regression models. Below are before and after pictures of a target transformation.

<img src="https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/before.jpg" width="425"/> <img src="https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/after.jpg" width="425"/> 
- Correlation map to see how features are correlated with each other, especially with ```mpg```.
- Split the data into training and test sets with ```scikit-learn```.
- Handle missing values with Simple Imputer by replacing missing values with the mean value and create a new column ```hp```.
- Handle low cardinality categorical variable by One-Hot Encoder class from ```scikit-learn```. 
![Preview](https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/one_hot_encode.jpg)

- Handle high cardinality categorical variable by Target Encoder. 
![Preview](https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/target_encode.jpg)

- Normalize features that use different scales and ranges by ```tf.keras.layers.Normalization```.
- Implement few ML models by tensorflow and keras.

As a result, a final benchmark table compares the achievement of different ML models such as linear regression model of every single feature, linear regression of multi-features, and a deep neural network in the mean_absolute_error metric.

It also illustrates significant enhancements in performance for the horsepower model, the linear regression of multi-features and the deep neural network compared to the tutorial of TensorFlow (0.47 and 3.63, 0.35 and 2.5, 0.23 and 1.7 respectively).

<p align="center">
  <img src="https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/benchmark.jpg" alt="Benchmark Table"/>
  <img src="https://raw.githubusercontent.com/harveyvn/Predict-Fuel-Efficiency-using-TensorFlow/main/assets/benchmark1.jpg" alt="Benchmark Table Tutorial"/>
</p>

