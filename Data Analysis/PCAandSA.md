---
layout: page
title: Sensitivity Analysis
permalink: /Sensitivity Analysis/
---

# Sensitivity Analysis
A collection of resources on PCA and sensitivity analysis.

## PCA
Principal component analysis (PCA) is a statistical technique that is used to analyze the variations in a dataset. 
It does this by transforming the data into a new set of variables, called principal components, which are a set of 
uncorrelated variables that capture the maximum possible amount of variation in the original dataset. PCA is often 
used as a dimensionality reduction technique, to reduce the number of variables in a dataset while still retaining 
as much of the original information as possible. This can be useful for data visualization, for example, or for 
building predictive models using machine learning algorithms. In summary, PCA is a technique for finding the most 
important underlying patterns in a dataset.

PCA on its own is a general technique that can be applied to any dataset as method to reduce the dimensionality of your data. However, there have been some papers using it
for sensitivity analysis in DEM simulations. The first section of resources below is for general PCA, and the second section
for using PCA for sensitivity analysis in DEM simulations.

**General PCA:**

The first few sections of [this article](https://www.cs.princeton.edu/picasso/mats/PCA-Tutorial-Intuition_jp.pdf) are 
an excellent short introduction to get your head around what PCA does. The rest of the paper goes into the maths behind
PCA, which you can look into if you are interested. I would recommend starting with just the first few sections.

[This article](https://towardsdatascience.com/a-one-stop-shop-for-principal-component-analysis-5582fb7e0a9c) provides a 
more thorough introduction to PCA and is a highly recommended read.

To implement PCA in Python, you can use the decomposition library from scikit-learn. There are many articles online that
provide a guide on how to do this but [this article](https://www.jcchouinard.com/pca-with-python/) is the one I used.

Add Dan Weston article

**Using PCA for sensitivity analysis in DEM simulations:**

PCA can be used on a sensitivity matrix developed from the derivatives of Newton's second law of motion to identify the 
main contributors to the principal components. This tells us how influential each variable is and thus the sensitivity.
[This paper](https://link.springer.com/article/10.1007/s40571-015-0056-5) details the process of generating the 
sensitivity matrix and using PCA.

## HDMR Sensitivity Analysis

Sensitivity analysis is a technique used to evaluate how the uncertainty in the input variables of a model or system, 
such as a financial model or a simulation, affects the uncertainty in the outputs. In other words, sensitivity analysis 
helps to identify which input variables have the greatest impact on the outputs of a model, and how sensitive the 
outputs are to changes in those variables. This is useful for identifying the key drivers of uncertainty in a model, 
and for understanding which inputs are the most important to the model's predictions. Sensitivity analysis is often 
used in a variety of fields, including finance, engineering, and environmental modeling, to help make better decisions 
by taking into account the uncertainty in the inputs to a model.

HDMR analysis is quite complicated (especially for an engineer like me) but luckily there is a powerful python package 
called [SALib](https://salib.readthedocs.io/en/latest/) that can do all the hard work for us. The SALib documents cover
how to set up a HDMR sensitivity problem and how to input your data.

There are many versions of HDMR sensitivity analysis but the one used by SALib is the RS-HDMR method that is detailed in
this [paper](https://pubs.acs.org/doi/pdf/10.1021/jp9096919). SALib also implements many other sensitivity analysis
methods if you are interested in trying them out.

This [paper](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.140.7406&rep=rep1&type=pdf) is also an interesting read a good source for HDMR. It covers the cut-HDMR and RS-HDMR methods concepts and 
alos provides some applications of where they are used.