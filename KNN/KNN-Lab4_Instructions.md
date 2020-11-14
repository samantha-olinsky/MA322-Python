Lab 4 – Classification using kNN (k nearest-neighbors)


We will be looking at the “Breast Cancer Wisconsin Diagnostic” data set, which is donated by researchers of the University of Wisconsin and includes measurements from digitized images of fine-needle aspirate of a breast mass. The data includes 30 numeric features which measure various characteristics related to shape and size of the mass, and a feature identifying the cancer diagnosis. The diagnosis feature is coded B for “benign” mass and M for “malignant” mass. Each example represents an independent cancer biopsy. In effect, we have 569 labeled examples. We would like to employ a classification algorithm that can learn from the data that we have and predict the diagnosis of new unlabeled examples, i.e., classify undiagnosed breast masses as either benign or malignant. 

Use Python and present all your answers/explanations/visualizations. The data file was recorded in a comma-separated-variable form and is accessible via blackboard. 

1.	Which feature is your target and what type of feature is it? What do we call the process of predicting a target variable of this type?
2. 	How many examples do we have in this data set? What does each example represent here?
3.	Construct a table of frequencies and a separate table of relative frequencies for the target feature. We should have a good mix of examples at each level of our target for our algorithm to work well. Use the info function to quickly peruse the 30 other features. 
4.	The kNN algorithm is ‘scale-variant’, which means that features with larger values will have undue influence on the outcome. I have already ‘Normalized’ the numerical features for you in this data set, you can confirm that if you look at the result of the describe function for the 30 numerical features.

5.	Let’s split the data into a Training set and Testing set. First, we should mix up the examples to protect against any type of ordering in the rows of the data. I have done the mixing for you already. Knowing that they are well mixed, take the first 469 examples for our Training set and the last 100 for our Test set. Create 4 assigned objects here: 

	Tip: These will all require you to subset/extract the original data set, carefully selecting particular rows and columns. You can check your work by printing the new dataframes you create.
Example: If you imported your data set and assigned the name df to it, you can create a new data set, say df_train, that is a subset of df by using df.iloc[  :  ,  :  ] and defining the rows and columns you need. 
For instance,   df_train = df.iloc[3:300,:-2] will subset df and give me only rows with the indexes 3 to 300, with every column except the last 2, and assign the new subsetted data set to the name df_train, while preserving the original dataset, df. 

Training data set without the target feature
Testing data set without the target feature
Training data set that includes ONLY the target feature
Testing data set that includes ONLY the target feature

6.	With the Training and Testing set successfully split into the 4 objects you created in the previous step, you can now use the kNN algorithm to predict the classifications, i.e., the diagnoses of the Testing examples. You need a few items here:
Choose an integer for k, or n_neighbors, close to the square root of the number of examples in the Training data set (remember odd numbers are preferred).
Define model:  model = KNeighborsClassifier(n_neighbors=k).fit(item1fromQ5,item3fromQ5)

7.	Create a Confusion Matrix with the predicted diagnoses of the Test examples and their actual diagnoses. Comment on the performance of our kNN algorithm. How many correct classifications? How many incorrect? Of the incorrectly classified examples which ones do you think are most dangerous in this context?

