# Stroke-Prediction

### Abstract 


Analysis on Stroke Prediction Dataset involves exploring and analyzing the various factors that may contribute to the likelihood of a person experiencing a stroke.
The dataset normally contains details about a person's age, ID, gender, smoking status, hypertension, heart disease, marital status, kind of job or place of residence, average blood sugar level, BMI, and status for strokes, among other things. Researchers can find correlations and patterns in data through data analysis that may help in forecasting the risk of stroke. To acquire a deeper knowledge of each piece of data and how they relate to one another, this analysis involved exploratory data and analysis (EDA) utilizing R and RStudio. To further help illustrate the patterns and trends in the data, data visualization tools like charts, graphs, scatter plots, and heat maps may be employed.  This Stroke prediction dataset data analysis is a useful tool for understanding the risk factors.
![image](https://github.com/drashtip7/Stroke-Prediction/assets/74112283/3df931c4-67f2-48bf-9384-0f02c17a24a4)

### Problem Definition :

The main objective of this study is to conduct a thorough investigation and correctly identify the variable that, in dependence on the input parameters provided in the Stroke Prediction Dataset, has the largest impact and influence on patients who are likely to experience a stroke.

### Goals of Project :
The goal of this  Stroke Prediction is to determine which conditions, lifestyle or habit such as smoking, heart disease, hypertension and How does level consumption of glucose impact on stroke risk.
![image](https://github.com/drashtip7/Stroke-Prediction/assets/74112283/cc318816-01e0-470f-9ff6-d3957068c627)


### Conclusion
So in this mini-project, we saw some of the factors that might result in strokes. Where Age was highly correlated followed by hypertension, heart disease, avg glucose level, and ever married.
XGBClassifier was a knight who performed well. There are outliers in some variable, reason behind why I kept it as it is because these things are either depends on other factors and there are possibilities of having such kind of records. For example, BMI can be high and still no stroke as a person is young or he does not have any heart disease. If you have any doubt or suggestion please comment it down. I would love to learn new things.
We first explored which variables are correlated with ‘stroke’ using the correlation plot, mosaic plots, and barplots. We found that ‘Residence_type’, ‘work_type’, and ‘gender’ are not very correlated with ‘stroke’, so we decided to exclude them when constructing models for classifying ‘stroke’.
For building the classifier, we first tried PCA with linear regression. Out of seven variables, we need the first five principal components to explain a total of 80 percent of the variation of the data. Since we failed to explain the total variation using less than 3 principal components, we conclude that our features either have non-linear relationships or low degree of dependence. The training accuracy of the linear model we built using first five principal components is 73 percent, which was not satisfying.
Next, we chose to use clustering techniques for classification. We built a dendrogram using complete-linkage with k being 10, and we colored the leaves by ‘stroke’. We found that most clusters align well with stroke in the dataset but there are some exceptions. Most of the clusters like the three clusters on the left have either stroke or no stroke dominating while the cluster on the right has no clear domination of stroke.
Finally, we used decision tree to classify our data. The model generated continuous rules to classify data. Rules include whether age  is less than 57, whether average glucose level is less than 96, whether bmi is lower than 39. Each leaf it produces corresponds to a probability of having or not having stroke. Then we test the performance of our decision tree by building the confusion matrix. With predicted and actual results, we get the accuracy of our classifier using decision tree model is 78.6%.
Therefore, decision tree seems to be the kind of model suitable for predicting whether one has stroke or not.
![image](https://github.com/drashtip7/Stroke-Prediction/assets/74112283/d8ae09b1-c01c-48d2-8182-fe15b25a9eb2)
