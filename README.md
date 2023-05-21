# DSC-520-final-project
#Credit Card Fraud Project

---
title: "Credit Card Fraud Project"
author: "Michael Pacheco Github username: Deeps"
date: "2023-05-21"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```


# Introduction

The proliferation of electronic transactions and the ubiquitous adoption of credit cards have resulted in a concerning surge in instances of credit card fraud. The constant evolution of fraudulent tactics employed by individuals seeking to exploit weaknesses in payment systems has prompted the need for the implementation of advanced strategies aimed at identifying and thwarting fraudulent activities. The issue of credit card fraud has emerged as a notable apprehension for financial organizations and individuals holding credit cards across the globe. The rapid evolution of technology has led to a corresponding evolution in the methods utilized by fraudulent actors to exploit vulnerabilities in financial institutions, rendering conventional fraud detection approaches inadequate. The discipline of data science presents a potentially fruitful approach to efficiently identify and forestall instances of credit card fraud. The issue under consideration is complex and has multiple aspects. 

The occurrence of fraudulent activities poses a significant financial risk to financial institutions, leading to a decrease in customer confidence and an upsurge in operational expenses. In contrast, cardholders assume the liability for any transactions that are not authorized and the possibility of harm to their credit scores. The need for the creation of advanced and aggressive fraud detection systems arises from the increasing prevalence and complexity of scams. The salience of this issue resides in its prospective influence on both the financial sector and consumers as a whole. The detection and prevention of credit card fraud is crucial for financial institutions in order to protect their wealth and credibility. Additionally, cardholders can benefit from increased security and a sense of reassurance when engaging in transactions. Addressing credit card fraud is a crucial aspect of promoting the security of the financial environment, which in turn enhances confidence and reliability among all relevant parties.

# Research Questions

There some research questions which as listed below:

### 1.

To what extent does credit card fraud occur in the contemporary financial environment, and what are the corresponding monetary damages experienced by both lenders and cardholders with data exploration?

### 2.

What are the prevalent categories and configurations of credit card fraud, and the way do they undergo transformation over the course of time?

### 3.

What are the constraints of conventional rule-based methodologies and current fraud detection systems in precisely detecting deceitful transactions?

### 4.

What are the potential applications of machine learning and data science methodologies in enhancing the precision and efficacy of credit card fraud identification?

### 5.

What are the optimal feature engineering methodologies for extracting pertinent insights from credit card transactional data to distinguish between bona fide and deceitful transactions?

### 6.	

What are the most effective machine learning algorithms and models for detecting credit card fraud, taking into account metrics such as accuracy, precision, recall, and computation effectiveness?

### 7.	

What are the potential methods for incorporating real-time monitoring and anomaly detection methodologies into current credit card fraud detection systems to expeditiously detect and address potential instances of fraudulent behavior?

The principal aim of this research piece is to tackle the issue of detecting credit card fraud through the utilization of data science methodologies. Our objective is to create a reliable model that can precisely detect fraudulent transactions by utilizing extensive datasets and sophisticated machine-learning algorithms.

# Proposed Approach

The methodology employed for tackling the issue of credit card fraud detection entails a thorough examination of past credit card transaction data, utilizing sophisticated data science methodologies and machine learning computation. Exploratory data analysis will be performed to obtain a comprehensive understanding of the features and trends exhibited by both valid and fraudulent transactions. Through the identification of constraints inherent in extant fraud detection systems, we aim to devise innovative models and methodologies that enhance the precision and efficacy of fraud detection. In order to investigate the research inquiries, a range of machine learning techniques will be utilized, including decision trees, random forests, logistic regression, and artificial neural networks. These methods will be employed to construct predictive models that can effectively classify payments made with credit cards as either genuine or fraudulent. The study will also explore the efficacy of feature extraction methodologies, such as anomaly detection, clustering, and reduced dimensionality, in extracting significant features from transactional data.

In addition, our investigation will delve into the incorporation of instantaneous monitoring mechanisms capable of an ongoing examination of incoming transactions, with the aim of detecting any potentially dubious activities in real-time. The adoption of a proactive approach will empower financial institutions to promptly undertake measures to avert or alleviate prospective losses arising from fraudulent transactions. Our objective is to develop a comprehensive framework for detecting credit card fraud that integrates multiple approaches to improve the precision, effectiveness, and promptness of identifying and thwarting fraudulent transactions.

# How Proposed approach addresses credit card fraud transaction problem

Our approach addresses the problem of credit card fraud by leveraging advanced data science techniques and machine learning algorithms to improve the accuracy and efficiency of fraud detection. Firstly, through exploratory data analysis, we gain a deep understanding of the characteristics and patterns associated with both legitimate and fraudulent credit card transactions. This analysis helps us identify the limitations of existing fraud detection systems and the need for more sophisticated approaches. Secondly, we employ various machine learning algorithms, such as logistic regression, decision trees, random forests, and neural networks, to build predictive models capable of accurately classifying credit card transactions as legitimate or fraudulent. These models utilize historical transaction data and learn from patterns and features associated with fraudulent transactions. By training these models on large datasets, we enhance their ability to identify complex and evolving fraud patterns.

Thirdly, we focus on feature engineering techniques to extract meaningful information from credit card transaction data. We explore anomaly detection, clustering, and dimensionality reduction methods to highlight relevant features that differentiate legitimate transactions from fraudulent ones. By incorporating these engineered features into our models, we increase their discriminative power and improve their overall performance. Additionally, we recognize the importance of real-time monitoring and timely detection of fraudulent activities. Therefore, we investigate the integration of real-time monitoring systems that continuously analyze incoming transactions and identify suspicious activities in real-time. This enables financial institutions to take immediate action to prevent or mitigate potential losses due to fraudulent transactions.

By combining these approaches, our framework provides a comprehensive solution to credit card fraud detection. It enhances the accuracy of identifying fraudulent transactions, improves the efficiency of the detection process, and enables proactive measures to be taken in real-time. Ultimately, our approach aims to protect both financial institutions and cardholders from financial losses and maintain the integrity of the credit card payment ecosystem.


# Dataset

Three dataset from Kaggle platform are considered for this prediction. The frist dataset link is (https://www.kaggle.com/datasets/vineetdumir/credit-card-fraud-detection) and the detail of the dataset 1 is given below. It have 691920 rows of  15 variables. The attributes data types are also listed. The target varibale in it 'Is.Fraud'. Outcoem shows that there ar eno missing vlaues in it as well. This information is related to the fraudulent transactions of the various users and along with card and with the duration. 

````{r}
#import the data set 1
df1 <- read.csv("ccf2.csv")

# structure of the data
str(df1)

# Missing values

print(colSums(is.na(df1)))
```
 The dataset 2 link is https://www.kaggle.com/datasets/emilysmithh/credit-card-fraud-detection . There are total 975036 rows and  22 parameters. The findings shows that there no missing vlaues in it. The data types are also listed here. This dataset consist of the transaction time, date and amount as per various merchants. Moreover, various locations of the users are also listed. 
 
 
````{r}
#import the data set 2
df2 <- read.csv("Data.csv")

# structure of the data
str(df2)

# Missing values

print(colSums(is.na(df2)))
```

Dataset 3 link is https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud. This dataset is about o have the 284807 rows and 31 attributes. This infomration is related to the users various amount and component analysis. Furthermore the target outcome for this vairbale is 'class'. 


````{r}
#import the data set 3
df3 <- read.csv("creditcard.csv")

# structure of the data
str(df3)

# Missing values

print(colSums(is.na(df3)))
```

# Required Packages

The above analysis will utilized the following packages for data visulization and data modeling purposes. 

```{r}
#library(tidyverse) for data analysis
#library(caret) used for data modeling
#library(data.table) usef for reading dataset
#library(randomForest) used to apply the random forest model
#library(xgboost) used to apply the boosting model
#library(tidymodels) used for modeling
#library(ggplot2) used for data visulization

```

# Required Plots and Figures

Various kinds of plots and tables can be utilized to demonstrate the outcomes of the study's inquiries in the examination of the detection of credit card fraud. The following are instances:

Bar plots are a graphical representation that can effectively display the incidence or count of distinct category variables. An illustrative representation, such as a bar plot, can be generated to exhibit the count of deceitful and legitimate transactions.

Histograms are a valuable tool for representing the pattern of distribution of continuous numbers in a visual manner. These histograms can be generated in order to investigate the variation in either transaction values or times spent on transactions.

Box plots offer a graphical depiction of the dispersion, central tendency, and extreme values of a given variable, through the display of its quartiles, median, and outliers. The proportions of transaction sums for fraud and non-fraudulent purchases can be compared using them.

Scatter plots are a useful tool for visualizing the correlation between two variables that are continuous in nature. Scatter plots can be utilized to investigate the correlation between the value of the transaction and transactions the ages.

The confusion matrix is a tabular representation that exhibits the efficacy of a classification model. The aforementioned information refers to true positives, true negatives, false positives, and false negatives. This table may serve as a tool for assessing the efficacy of one's fraud detection algorithm.

The ROC (Receiver Operating Characteristic) curve is a graphical representation that illustrates the efficacy of the binary classifier across various classification boundaries. This sentence exemplifies the compromise that exists between the rate of correctly identified positive instances and the rate of falsely identified positive instances. The utilization of the area under the receiver operating characteristic (ROC) curve, commonly referred to as AUC, is a viable method for evaluating the efficacy of one's fraud detection model.

Summary tables are a useful tool for presenting essential statistical data and metrics that pertain to one's research inquiries. An illustrative instance involves the generation of a tabular representation that exhibits the mean transaction value for both fraudulent and non-fraudulent interactions, or the accuracy and recollection metrics of the detection of fraud framework.

# Questions for future steps

Such important questionss are listed here:

There are several questions which are related to future steps which are listed below:

### 1

Upon obtaining the datasets, what methods will be employed to explore and preprocess the data? What methodologies do you intend to employ for managing absent data, anomalies, and disparities between genuine and deceitful transactions?

### 2

In the context of credit card transactional data, what particular features are intended to be extracted through the process of feature engineering? What methods will be employed to manipulate and optimize these characteristics in order to increase the distinguishing ability of the prognostic models?

### 3

What methodologies will be employed to evaluate and contrast their performance?

### 4

The process of training and evaluating models is a crucial aspect of the modeling process. Can you elaborate on your approach to this process? Do you plan to employ cross-validation methodologies, such as k-fold cross-validation, in the future for evaluating the overall performance of the approach?
### 5

The present inquiry pertains to the exploration of methodologies that can be employed to integrate real-time monitoring and identification of anomalies into the fraud detection system. What measures will be implemented to guarantee prompt identification and reaction to possible occurrences of fraudulent conduct?

### 6

What methodology will you employ to assess the efficacy of your comprehensive fraud detection system? Would you be performing experiments and simulations to evaluate the efficacy of credit card fraud detection and prevention measures?

### 7

What ethical issues will be considered during the research process? What measures will be implemented to mitigate privacy concerns and promote responsible data usage within the credit card fraud identification framework?

### 8

What are the possible constraints or drawbacks that may arise from the implementation of the approach you have suggested? What strategies can be employed to overcome these constraints, and what potential areas of investigation can be pursued to enhance the efficacy of fraud with credit cards?

### 9

What are the potential challenges and factors that need to be taken into account during the implementation phase?



