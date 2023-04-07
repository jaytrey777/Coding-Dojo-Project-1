<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230511260-8e4ed48a-e65b-4b11-876e-35ee484ab605.png">
</p>

# Food Sales Predictions
`Jason R. Tracey`

### Explanation

## Data Source
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset, there were 8523 rows and 12 columns.

## Data Dictionary

<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230511855-fced9278-a1e2-4389-8a01-e96291b48eff.png">
</p>
</n> 

## To prepare this data, the data was cleaned, and the following processes were performed:

### Exploratory Data Analysis
    - During the exploratory data analysis, histograms and boxplots were visualized for relevant numeric and 
      categorical datatype columns. 
    - Also, a heat map was used to show the correlations between the data. 
    - This gave a good baseline for all of the numeric and categorical columns for univariate data.
    
    
### Exploratory Visuals    
<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230512634-caccc7af-2827-4064-b041-5c9e8db5faee.png">
</p>  
</p> 


This histogram shows that over 1400 stores were established in 1985, but there were less than 600 established in 1998. There were also no stores established between 1988 and 1997, but there were a litte over 900 stores established all of the other years.    

<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230512851-bbc55ef3-84b8-4dc4-9654-ba21093895c4.png">
</p> 

This box plot shows that the median price of the items is a little less than $150 where the majority of the prices are between $90 and $190. The max pirce is around $260 and the minimum price is around $30.

### Expanatory Data Analysis
    - To visualize the data for explantory purposes, two bargraphs and two scatterplots were chosen.
    - The bar graphs were chosen to show how sales related to categorical data and scatterplots were 
      chosen to show how sales relates to numerical data.
    - Finally, three of the graphs have a hue to help distinguish more informatino abour the data.


### Explanatory Visuals
<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230515525-575e2eee-1a4e-44a3-82e7-594217a1b0c0.png">
</p> 
</p> 

This barchart shows that the most sold item is starchy foods and the least is other types of food. It also shows that the type of food does not influence sales a lot as there is not one category that is a far and away leader.

</p> 
<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230515733-6710d28e-86bd-4988-8af4-06eb52191178.png">
</p> 
</p> 
This Scatter Plot shows there is no direct correlation between the visibility of items in outlets and the sales of the item. It seems people buy what they need no matter the price or how visible the item is.

<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230515972-e0d52039-5b14-4c03-a293-6dc7ce38cca3.png">
</p> 

This Scatter Plot shows that there is a small positive correlation between the outlet sales and the price of items. There is also not a strong correlation betweeen the fat content and the price or sales.

<p align = "center"> 
<img src = "https://user-images.githubusercontent.com/20051049/230515995-4ab42ef7-a3b4-4e67-8f5e-c4c121c6a207.png">
</p> 

This Bar Graph shows that the store that was established in 1985 is Tier 3 and has the most sales and the one established in 1984 is a Tier 1 store and has the least sales.


### Maching Learning Using the Following Models:
    - Linear Regression Model
    - Decision Tree Regressor Model
    - Bagged Tree Regressor Model
    - Random Forest Regressor Model

### Models Evaluated & Results
<p align = "center"> 
<img width="878" alt="image" src="https://user-images.githubusercontent.com/20051049/230536078-df4f749b-ee00-4754-a58d-bff0d41a4499.png">
</p> 

- The Final Untuned Model Chosen was a `Random Forest Regressor Model` .
- For the testing set on the model, `56.04%` of the variance in y was explained by x. 
- The Mean Absolute Error was off by about `$765.43`.
- The Mean Squared Error was `$1,212,852.26`.
- The Root Mean Squared Error had a calculation of `$1101.30`
 
Based on these current model metrics, I would use the Random Forest Model. It has the second best R-Squared and Root Mean Squared Error values but has the lowest Mean Absolute Error and Mean Squared Error values. The R Squared and RMSE values are only second by a small margin. The Random Forest Model will not be able to account 0.09% of variance as the Linear Regression Model, but will give you predictions that are $46.26 tigher to actual values on average.

### Tuned Model & Results
<p align = "center"> 
<img src ="https://user-images.githubusercontent.com/20051049/230536460-bf7004f6-dccd-4539-96c4-395f5769fb4c.png">
</p> 

- Based on these tuned model metrics, the Tuned Random Forest Model has the best metrics in all the Testing categories when using 140 estimators and a Max depth of 5.
- The Tuned Random Forest Model will be able to account for 60.31% of variance in y as explained by x.
- The Mean Average Error was off by about $728.24
- The Mean Squared Error was $1,095,017.80
- The Root Mean Squared Error had a calculation of $1046.43

Using this model to make predictions about the sales for different grocery stores would not be very reliable. Considering the metrics from how the model performed, the model is underfit to the data. The model performed similarly on the training data and testing data, suggesting a bias with respect to the R-Squared values being around 60% for both the testing and training. There may be different models out there that will perform better to this data set.
