# Feature-Selection-Techniques-with-Breast-Cancer-Dataset
This project investigates different techniques for feature selection utilizing filter, wrapper and embedded methods to increase the descriptive nature of the features and reduce the space of the feature vector

**Dataset**

http://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+%28diagnostic%29

**Explaratory Data Analysis**

![image](https://user-images.githubusercontent.com/69100847/178135953-68941da7-9113-4a24-b6bd-940d89a96014.png)


**Checking datatypes**

![image](https://user-images.githubusercontent.com/69100847/178135642-504ae499-2892-47a8-84f5-8d6542158161.png)


**Checking Null Methods**

![image](https://user-images.githubusercontent.com/69100847/178135661-888cc8aa-602a-4902-bd58-15dc7f146f28.png)


**Checking the diagnosis feature (dependent variable)**

![image](https://user-images.githubusercontent.com/69100847/178135697-ea0ce97c-f7fe-47af-9f37-c66bbea02d25.png)


**Changing the diagnois value to lie between 0 and 1**

![image](https://user-images.githubusercontent.com/69100847/178135717-1692bfc7-040d-4136-958c-10e12e48d2c5.png)


**Training a RandomForestClassifier and using different evaluation metrics**

![image](https://user-images.githubusercontent.com/69100847/178135748-318dbad0-0a23-449b-956b-f41574e7a41c.png)


**Plotting the correlation matrix (heat map)**

![image](https://user-images.githubusercontent.com/69100847/178135761-f0e641aa-6cd5-467e-ba93-11d10a8bd21e.png)

**Filter Methods**

1- Statistical pearson Test (Used for numerical features and numerical target)

2- Anova f_test: used for numerical features and categorical target

3- Chi squared: used for categorical features and categorical target

- Using correlation with regard to the target variable is called supervised feature selection

- Calculating the correlation for one variable at a time is called univariate feature selection


**Pearson Method**

![image](https://user-images.githubusercontent.com/69100847/178136148-20d267b6-9166-40e0-86bc-e7cec95f4b2f.png)

**Setting Threshold for Correlation Value**

![image](https://user-images.githubusercontent.com/69100847/178136413-177e1cbb-5849-4793-ab42-b6356746637a.png)

**Collecting Features with Correlation Value graater than 0.2**

![image](https://user-images.githubusercontent.com/69100847/178136438-2818e90f-3d7b-4990-8364-29adf51b49eb.png)

**Evaluating Model on New Selected Features**

![image](https://user-images.githubusercontent.com/69100847/178136460-f1ac0a4b-e49d-46a3-97da-09f66bd7a105.png)

- It can be seen that the RandomForestClassifier model performed better after selecting the strongest correlation variables

**Correlation between features (Unsupervised Feature Selection)**

![image](https://user-images.githubusercontent.com/69100847/178136788-3bd3f88b-bd9d-402e-bb79-c8578624da6f.png)

- it can be seen from the above heat map the strong correlation that exists in the features presented

**Removing The Redundant Features**

![image](https://user-images.githubusercontent.com/69100847/178136704-3358e4a8-26be-41c6-ba6e-6b826e4f313c.png)

- It can be seen from the results that removing the redundant features doesn't lead to any performance degradation as they don't provide any useful information

**Univariate Selection with SciKit Learn**

- We will use Anova F test to select the 20 most important features as shown below

![image](https://user-images.githubusercontent.com/69100847/178138494-cf915539-0168-4362-b9d7-7ddd627464f4.png)

**Wrapper Methods**

- Wrapper Methods use models to calculate how many features to be selected.
- Forward selection adds features until model ceases to improve.
- Backward selection removes features until model performance degrades
- Recursive Feature Elimination: Kind of Backward selection but it removes features based on their importance

Below is a snippet of the code used to implement recursive feature elimination as follows

![image](https://user-images.githubusercontent.com/69100847/178138613-83c6c2cd-e516-46fa-9fe6-f83bc80a5b80.png)

**Results**

This project explored different techniques for feature selection with the Breast Cancer Data. The table below summarizes the results from the project

![image](https://user-images.githubusercontent.com/69100847/178138694-60d9cf17-d728-4e18-82e4-2e116392b2e4.png)



