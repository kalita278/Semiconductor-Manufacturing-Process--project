# Semiconductor-Manufacturing-Process--project


**DOMAIN:** Semiconductor manufacturing process

**CONTEXT:** A complex modern semiconductor manufacturing process is normally under constant surveillance via the monitoring of
signals/variables collected from sensors and or process measurement points. However, not all of these signals are equally valuable in a
specific monitoring system. The measured signals contain a combination of useful information, irrelevant information as well as noise.
Engineers typically have a much larger number of signals than are actually required. If we consider each type of signal as a feature, then
feature selection may be applied to identify the most relevant signals. The Process Engineers may then use these signals to determine key
factors contributing to yield excursions downstream in the process. This will enable an increase in process throughput, decreased time to
learning and reduce the per unit production costs. These signals can be used as features to predict the yield type. And by analysing and
trying out different combinations of features, essential signals that are impacting the yield type can be identified.
 
**DATA DESCRIPTION:**
The data consists of 1567 datapoints each with 591 features.
The dataset presented in this case represents a selection of such features where each example represents a single production entity with
associated measured features and the labels represent a simple pass/fail yield for in house line testing. Target column “ –1” corresponds to
a pass and “1” corresponds to a fail and the data time stamp is for that specific test point.

**PROJECT OBJECTIVE:** We will build a classifier to predict the Pass/Fail yield of a particular process entity and analyse whether all the
features are required to build the model or not.

**DATA EXPLORATION AND DATA CLEANING:**

Created a single file with all the relevant variables and perform the necessary data quality checks and cleaning. In data cleaning, identified the missing values/unexpected values in the dataset and since the number of missing values is very less, replaced the missing values with mean. Also, identified the outliers in the dataset and replaced the outliers with mean. Make sure that the data types of the variables are appropriate as required for our analysis (Here, converted all the categorical variable data types to category and continuous variable data types to int or float).


**DATA ANALYSIS:**

Checked the distribution of data for the continuous (histogram charts) and categorical (pie charts) variables. Performed uni-variate, bivariate, and multivariate analysis of the dataset, for example, 5-point summary of the continuous variable,scatter plot, correlation matrix plot, and boxplot to detect outliers.

**DATA PREPROCESSING:**

Here, removed the unwanted/irrelevant independent variable/feature based on the above analysis from the dataset. Also, scaled the independent variable using standard scaler and since the dimension of the data is very high, so applied principal component analysis (PCA) to reduce the dimension of the data.

**MODEL BUILDING, EVALUATION AND IMPROVEMENT:**

Used k nearest neighbour, logistic regression, support vector machine (SVM), random forest, and Ada boost algorithm to predict whether semiconductor yield status and evaluate the model using confusion metrix, accuracy score, recall score, precision score and f1 score. Further tunned the models using GridsearchCV and compared all the models to find the best model. Also used cross-validation technique to reduce overfitting.

**Finalize svm as the final model and achieved an accuracy of 100%.**
