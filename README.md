# The Identification of a Subject by the Acceleration of His Walking

## Overview

This repository contains the results and code related to a study conducted in 2016 titled "The Identification of a Subject by the Acceleration of His Walking." The study was supervised by Shlomo Rozenfeld and carried out by Eyal Gon, Golan Kai, and Kotzer Dan.

## Introduction

Humans have unique walking patterns, akin to fingerprints. This study explores the possibility of identifying individuals based on their walking patterns, leveraging artificial intelligence for enhanced accuracy. While the human eye struggles to distinguish minute differences between two people walking, artificial intelligence simplifies the process.

## Research Method

### Data Collection

We collected three-dimensional acceleration data by attaching a smartphone to subjects' backs, using the phone as a motion sensor.

### Tools and Libraries

Our research utilized the following tools and libraries:

- Python
- Numpy for calculations
- Matplotlib for graphics
- Scikit-learn for Logistic Regression
- Pybrain for the Neural Network and database management

### Data Preprocessing

To facilitate machine learning, we divided each one-minute sample into 2-second segments, providing more examples for the learning process. From each segment, we extracted several features, including maximum and average accelerations and histograms for each axis.

The dataset was split into three groups:

- Training: Used for machine learning
- Validation: Used to measure the machine's error
- Test: Employed to evaluate the best-performing network

### Code Structure

We structured our code into "Auxiliary Functions" to improve readability and facilitate debugging.

### Machine Learning Models

- **Logistic Regression:** We created a Logistic Regression model for each subject, which identified their features and attempted to classify them from the validation group.

- **Artificial Neural Network:** We designed an artificial Neural Network with one hidden layer. The input layer's size equaled the number of selected features, while the output layer matched the number of subjects to be classified. By adjusting the number of neurons in the hidden layer using a "For" loop, we optimized the network.

## Results

While some tests achieved 0% error, we recognize that the program isn't infallible due to the relatively small dataset. Notable results include:

- The best Neural Network, with 44 neurons in the hidden layer, achieved 85% accuracy.
- The best Logistic Regression model, considering three subjects, reached 96.5% success.

## Further Research

We explored the influence of different features on the learning process. Removing the histogram feature from the Neural Network resulted in frequent 0% error with 26 neurons in the middle layer.

We expanded our research from 3 to 9 subjects, excluding the histogram feature. The best network, with 35 neurons in the hidden layer, achieved 42% accuracy.

## Conclusions

Our program demonstrates significant learning capabilities, surpassing the accuracy of random guessing substantially. With a larger database, we anticipate even better success rates.

## Future Uses

We believe that our program has potential applications in various fields, including:

- Identifying walking patterns that may cause physical harm.
- Detecting individuals with stolen phones.
- Recognizing impairment due to alcohol or drugs.

Our work could be applied through a simple phone application, making it accessible to a wide range of users.
