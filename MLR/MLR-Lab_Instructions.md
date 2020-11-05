Lab 3 – Prediction using Multiple Regression 

Insurance companies make money by collecting more in yearly premiums than they spend on medical care for their beneficiaries. Insurers invest a great deal to develop models that attempt to predict medical charges beneficiaries will incur. Medical expenses are notorious for being difficult to estimate because the most costly conditions are rare and seemingly random. Nevertheless, there are patterns that emerge for certain segments of the population. For instance, lung cancer is more likely among smokers than non-smokers, and heart disease may be more likely among the obese. Our overarching goal will be to use patient data from the past calendar year in order to predict the cost of new patients and thereby use this information to determine suitable yearly premiums. 

Use Python and present all your answers/explanations/visualizations in a text document, using a consistent font. The data file was recorded in comma-separated-variable form in file “insurance.csv”. 

1. Which feature is your target and what type of feature is it? What general family of methods have we learned to predict this type of feature? 
2. Which are your potential independent features? What types of variables are each of these? If a variable is categorical, note its categories. Hint: How can we display all the categories of a feature? Look back at your EDA notes.
3. How many examples do we have in this data set? What does each example represent here? 
4. Construct a scatterplot matrix of the numerical features in this data set. 
5. Calculate r, the Pearson’s correlation coefficient, for every pair of numerical features in this data. A correlation matrix should do the trick. Describe the direction and strength of a few of the strong relationships in this data. Does this agree with what you learned from your scatterplot matrix? 
6. Use a linear model function to fit a MLR model on this data using age, children, bmi, sex, and smoker as independent features. Report the regression coefficients and write the equation in **Ŷ = b<sub>0</sub> + b<sub>1</sub>X<sub>1</sub> + b<sub>2</sub>X<sub>2</sub> + … + b<sub>k</sub>X<sub>k</sub>** form. Don’t use y and x, instead use the appropriate feature names with the corresponding coefficients. Describe one of the partial slopes in the equation to show you understand what this means. 
7. Report R2  for the model you created in Q6, and interpret it. 
8. Create a new MLR model the same as Q6 excluding sex. Compare the new R2 to the R2 from the larger model in Q6. Did we need the larger model from Q6 or did the smaller model you created here have as much explaining power? Hint: compare R2 from the two models. 
9. Use the regression model you learned from Q8 to predict the charges for a new patient applying for health insurance who is 22 years old, a non-smoker, has no children, and has a bmi of 30. Compare that to the prediction for a smoker with all other information the same.
