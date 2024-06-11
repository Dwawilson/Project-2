# Group 3, Project 2: Will The Ad Be Clicked?
By Dwann Wilson, Kanish Mohan, Kyle Williams, and Marcellus Smith
## Summary
We've used a dataset that simulates user behavior metrics such as their demographics, where the ad was located, and the amount of times they clicked on an ad. We used ML models to determine what factors makes people more inclined to click on an ad.
## Dataset
[Tawade, Jagadish; Kulkarni, Nitiraj (2024), “Dataset: Online Advertisement Click-Through Rates”, Mendeley Data, V1, doi: 10.17632/wrvjmdtjd9.1](https://data.mendeley.com/datasets/wrvjmdtjd9/1)
## Dependencies
* Pandas
* Scikit-Learn

    * train_test_spilt
    * OneHotEncoder
    * OrdinalEncoder
    * StandardScaler
    * PCA
    * KMeans
    * LinearRegression
    * RandomForestClassifier
    * r2_score
    * classification_report

* imblearn

    * SMOTE

# Question 1: What factors make someone more likely to click on an ad?
## Intro
In this project, we focus on predicting click-through rates (CTR) for advertisements using machine learning. Effective advertising relies on understanding audience preferences.
## Code
Our approach involves feature engineering, where we transform raw data by applying techniques like Principal Component Analysis (PCA) for dimensionality reduction and one-hot encoding for categorical features (such as Age and Location). Additionally, we create a new target variable called ‘Ad Encounter’ to indicate ad clicks.
## Conclusion
By separating features from the target variable, we train machine learning models to predict ad success based on factors like Age, Income, and Ad characteristics.

# Question 2: What Regression Model is best at predicting the data?
## Intro
intro
## Code
code
## Conclusion
conclusion
## Sources
sources

# Question 3: Can a Classification model predict if someone clicks on an ad?
## Intro
[According to a blog post from Neil Patel (n.d.)](https://neilpatel.com/blog/what-is-the-optimum-number-of-clicks-before-conversions-start-happening/#:~:text=It%E2%80%99s%20a%20good%20strategy%20to%20directly%20pitch%20your,product%20page%2C%20will%20lead%20to%20a%20website%20conversion.), it takes at least 2 clicks to convert a user into a customer. We can try to use a classification model to predict if an ad is succesful at getting the user to click at least 2 times.
## Code
The code uses a slice of the DataFrame that only contains rows with the amount of clicks being from 0-3. After doing a train-test-split, the X data is scaled and encoded and the y data is the clicks column encoded as "Yes" for rows with 2-3 clicks and "No" for rows with 0-1 clicks. I used the Random Forest Classifier as my model, and I calculated the maximum depth that produces the most accurate results looping through max depths 1-15. The model trained with a max depth of 8 had an accuracy score of 85%, but had no accuracy for determining ads that weren't clicked at least two times. I made several attemps to resample the data, and I when I did it with the SMOTE sampler it produced an accuracy of 81%, but with a higher accuracy for "No" results.
## Conclusion
A classification model can be used to predict if it will convert a user into a customer, but more data is needed to improve the model's ability to differentiate effective ads from non-effective ads.
## Sources
[Patel, N. (n.d.). *What is the optimum number of clicks before conversions start happening?.* NP Digital. LLC](https://neilpatel.com/blog/what-is-the-optimum-number-of-clicks-before-conversions-start-happening/)

# Question 4: What is the most desirable ad?
## Intro
intro
## Code
code
## Conclusion
conclusion
## Sources
sources