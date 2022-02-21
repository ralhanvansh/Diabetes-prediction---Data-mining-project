# DiabetesPrediction-DM-Project
      
# Table of Contents:
1. Introduction
2. Purpose of the project
3. Current stage of research/Current Implementation 4. Difference between your work and past research 5. Experiments & Results
6. Conclusion
7. References papers

# Introduction:<br/>
Diabetes is an acute disease related to the metabolism of the body that causes high blood sugar, where the body lacks the amount of insulin it requires to function or can’t effectively use the insulin it already has. <br/>
There are three main types of diabetes:<br/>

a. Type 1 Diabetes: Doctors don’t know exactly what causes type 1 diabetes. For some reason, the immune system mistakenly attacks and destroys insulin-producing beta cells in the pancreas.[1]<br/>

b. Type 2 Diabetes: Type 2 diabetes stems from a combination of genetics and lifestyle factors. Being overweight or obese increases your risk too. Carrying extra weight, especially in your belly, makes your cells more resistant to the effects of insulin on your blood sugar.[1]<br/>

c. GestationalDiabetes:Gestationaldiabetesistheresultofhormonalchanges during pregnancy. The placenta produces hormones that make a pregnant woman’s cells less sensitive to the effects of insulin. This can cause high blood sugar during pregnancy. [1]<br/>

These types of diseases affect the quality of life and are the leading cause of death in the adult population across the globe. Much research is being conducted for early prediction. It is projected that in the near future, more than 600 million patients with diabetes will exist around the globe and half of the population will be undiagnosed. Therefore to minimize such tragedy, a sufficient amount of data is being gathered by researchers so as to learn from the observed data. The implementation of data-mining techniques in the selected datasets was useful for extracting valuable information and predicting early symptoms.<br/>
    
# Purpose of the project:
In this dataset, we want to predict whether a diagnosis will be positive or negative based on the reported symptoms. In the end, we can see the predictions that our model has made. With the results, based on the symptoms and other attributes like an age we can determine whether the person is diagnosed positive or negative for diabetes.

# Experiments and Results
Our implementation of this project has been segregated into two different sections: <br/>

1. Data Preprocessing and Visualizations<br/>
2. Train and testing the model<br/>

Data Preprocessing and Visualizations: In this section, we look at information about our dataset and use data manipulation which gives us an overview of the rows and columns, as well as the data types of our columns. We also made the actual model using Logistic Regression and included libraries like matplotlib and seaborn to show the graphical representation of our data in different cases. Below are the implementation steps:
1. Load Necessary libraries and datasets.
2. Display the top 5 rows to get an idea of the data in the dataset.
3. Used various built-in data manipulation methods like describe, shape
and IsNull().sum() to check for null values in the dataset.
4. Then we defined a method to check if there are any ‘?’ values in the
dataset.
If found one, we have logic in place to replace those values with null values.
5. Then to get a better understanding of the data we are generating different bar graphs which include a graph to display the count of patients based on gender. In our dataset, there are 328 males and 192 females, or 63.08% and 36.92% respectively.
6. We have converted the column values into Boolean values which will make our data analysis easy to do the computation in the next steps.
7. Various Density graphs have been plotted to show the distribution of
age based on all genders and diagnoses, distribution of Age by Gender and various other plots. Of the 320 positive cases, 45.94% are male, and 54.06% are female. We'll see how this affects our logistic
regression model in the future.
8. Reaching the end of our data visualization stage, we have
implemented some heatmaps to get an idea of how they correlate to
each other.
9. After grouping and combining all the data, we have implemented a
bar graph to demonstrate Reported Symptoms grouped together for all symptoms segregated by Gender.


Train and test the model: In this section, we'll train our model. We’ve created classes and methods that abstract the code to make the logic easier to read and understand. Below are the implementation steps:
1. Initially, all the required libraries are imported.
2. Starting with loading the data, then the columns which are objects are converted into categorical columns with the exception of ‘Age,' which is of type integer.
3. Now, the age column is grouped like 0–9, 10–19, 20–29, 30–39...and so on (e.g. 10s, 20s, 30s...).
4. After grouping, the age grouped columns are converted to binarycolumns and our old ‘age’ column is dropped.
5. For the model, we take our target as ‘class’ and our features as our remaining columns (gender, age bin, and all the reported symptoms).
6. We then split the data into training and test sets with train_test_split and made the actual model using LogisticRegression.
7. Then we made some of the helper functions (build evaluation df and graph log performance), which will provide a Pandas DataFrame for us to see our predictions.
8. For model training, we select our data to pass into train_test_split. ‘X’ is our feature column and ‘y’ is the target column. Then our training and test datasets (X_train, X_test, y_train, y_test) are created.
9. We then create our model. Then we fit the model to our test data with the model.fit(X_train, y_train).
10. Then we called model.predict_proba(X_test) which returns a 2-dimensional array of the probability of each data point being a positive or negative diagnosis. This will return the actual positive/negative (0 or 1) prediction for each data point.
11. Now that we have predictions, to know if we can trust our model we call model.score(X_test, y_test). which returns our R-squared score. 
12. In the current state of our model, we have an R-squared score of 0.9134615384615384.
13. With 1 being the best outcome, our current score tell us if our data is fit quite well to our regression line.
14. Using our helper function, we graph the predictions that our model has made.
15. Using a confusion matrix we can see how many true positives, false positives, false negatives, and true negatives the model predicted.
16. Using the above numbers we calculate precision, accuracy, and recall. We used sklearn functions for calculations.
17. At last, we will be able to determine which gender had more incorrect predictions.


<br/>
Conclusion:

Data mining techniques are invaluable in diabetic diagnosis. Its capability to predict the disease early plays a vital role in the treatment. In this research paper, a few existing classification methods for medical diagnosis of diabetes patients have been discussed based on their gender, symptoms, class etc. From this project, we learned to detect the presence of diabetes using various attributes such as age, gender, obesity, fatigueness, genetics, etc. We applied data manipulation techniques to convert the attributes to desired data type and different python libraries to plot the graphs, which gave us an accuracy score of 91.3%. In the second file, we conducted data training and made models using logistics regression.

The drawback of this study is that a structured dataset has been used but in future researches, unstructured data can also be considered, and these methods can also be used to predict other medical domains such as different types of cancer, psoriasis, and Parkinson's disease. Along with the selected attributes, other characteristics such as physical inactivity, family history of diabetes, and smoking habit, will also be considered in the future for the diagnosis of diabetes.

