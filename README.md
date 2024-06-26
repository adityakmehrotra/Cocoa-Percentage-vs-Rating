# Cacao-Percentage-vs-Rating
Using Machine Learning and Analysis to determine the relationship between the cacao percentage of a type of chocolate and its objective rating.

## Introduction

A universally popular treat, chocolate is available in a variety of forms ranging from beverages, pastries, ice creams, and of course, the standard chocolate bar. In the United States alone, an estimated average of 2.8 billion pounds of chocolate are consumed each year! Milk chocolate is the American fan favorite, with a usual cacao percentage range of 10-55%, followed by Dark Chocolate, with a cacao percentage of at least 55% and above. Between these two popular types of chocolate, cacao percentage helps distinguish the sweeter and lighter tastes of the Milk Chocolate from the richer, more bittersweet taste of Dark Chocolate. Simply put, cacao percentage is the ratio between actual cacao product from cacao butter, liquor, and powder and filler ingredients like vanilla, milk, and other added flavors. Generally, a higher cacao percentage denotes a more intense taste and higher price point, implying that it is of higher quality. Given this information, is it fair to say that higher quality chocolate yields higher ratings? Our study explored whether cacao percentage has a large influence on chocolate ratings in addition to using cacao percentage as a predictor for such chocolate ratings.

### Thesis

While higher cacao percentage is predicted to lead to a lower chocolate rating, there does not appear to be a strong relationship between those two variables.

## Background

### Dataset Information

This dataset includes 2,600 ratings of plain (non-flavored) chocolate bars produced by chocolate manufacturers around the world. The ratings are conducted by the Manhattan Chocolate society, who conduct research on chocolate production in order to produce innovative, high quality chocolate.

In the original Chocolate dataset, 7 variables are mentioned: REF (manufacturing number), Company (Manufacturer) Name, Company Location, Review Date, Country of Bean Origin, Specific Bean Origin or Bar Name, Cacao Percentage, Ingredients, Most Memorable Characteristics, and Rating. For the purposes of our study, we will consider 2 of the 7 variables: **Cacao Percentage, and Rating.**

#### Data Collection

##### Rating Column

Each row in the dataset represents one rating for one brand of chocolate bar. Ratings were conducted by members of the Manhattan Chocolate Society, comprising of chocolate authors, makes, and experts--people involved in the chocolate industry for an extensive amount of years. Ratings were conducted on a five point scale:

**1.0 - 1.9: Unpleasant**

**2.0 - 2.9: Disappointing** 

**3.0 - 3.49: Recommended**

**3.5 - 3.9: Highly Recommended**

**4.0 - 5.0 : Outstanding**

To determine the rating, the below factors were considered:

**Flavor:** How intense the cacao tastes (mild-moderate-strong), the roast of the chocolate,       dominant ingredients (cacao, sugar, butter) or if the ingredients are balanced, the             profile (floral, fruity, herby, smokey notes), and bitterness (mild-moderate-strong)

**Texture:** a higher quality chocolate will have a creamier, more even consistency, whereas       a lower quality chocolate will be more gritty, waxy, and dry

**Aftermelt:** the lasting experience/taste of the chocolate after it has melted in your mouth. A higher quality chocolate will have a longer lasting pleasant flavor, whereas lower quality chocolate not have as long lasting of an aftertaste and possibly leave an astringent, or acidic by-product.

##### Cacao Percentage

Cacao percentage present in each chocolate bar was given by the manufacturer of that chocolate bar. The Manhattan Chocolate Society reviews chocolate from companies that are transparent about their production process.

### Possible Counfounding Factors
Since all the ratings of the chocolate bars were performed by members of the Manhattan Chocolate Society, their ratings are in part influenced by each member's subjective taste standards. Thus,
the results of this study are only application to members of the society and not representative of the general population.

### Our Objective
In the rest of the report, we will analyze the relationship between cacao percentage and chocolate ratings using the provided dataset. Our primary question is whether the cacao percentage significantly influences the chocolate ratings. We will explore graphical representations, statistical analyses, and draw inferences based on the data.

## Analysis

To measure the relationship between cacao percentage and chocolate ratings, a simple linear model was constructed. 

<img width="914" alt="Screenshot 2024-04-11 at 3 39 39 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/05a05a59-8570-455c-b175-c6947c5d82b7">

**Null hypothesis**: The percentage of cacao in a chocolate bar does not affect its ratings, the slope of the linear regression model will be 0.

$H_0: \beta_1 = 0$ 

**Alternative hypothesis** The percentage of cacao in a chocolate bar does affect its ratings, the slope of the linear regression model will not be 0.

$H_a: \beta_1 \neq 0$

According to the linear model summary, the **p-value is 1.935e-13**. 

Following the linear regression model, our least-squares regression line is:

> $Y_i = 4.010169  +  -0.011334X_i%$

The slope is **$\beta_1$ = -0.011334**; for every 1 percentage point increase in cacao percentage, the rating decreases by -0.011334. The intercept is **$\beta_0$ = 4.010169**.


The graph below models the relation between cacao percentage and chocolate rating using linear regression:

<img width="686" alt="Screenshot 2024-04-11 at 3 42 54 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/ed9ccc33-7281-4f8d-bd1c-cb40576f36ca">


This graph displays the predicted ratings using linear regression using with cacao percentage as the predictor. At 50%, 75%, and 90% cacao percentage, a red, orange, and purple dot marks their predicted rating:

<img width="683" alt="Screenshot 2024-04-11 at 3 42 56 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/60302638-6153-487b-9464-54d345fe44ab">


**Confidence Interval**

The 95% confidence interval for our slope is: 

<img width="912" alt="Screenshot 2024-04-11 at 3 46 55 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/b232adfd-310b-4f17-ba60-c1147531a231">


We are 95% confident that the true slope lies between -0.01434028 and -0.008326993.

**Correlation Coefficient**

The correlation coefficient for cacao percentage and ratings is calculated to measure the strength and direction of the linear relationship.

<img width="913" alt="Screenshot 2024-04-11 at 3 46 57 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/a10f5a8f-fc16-4784-bc83-cbc1c7b7e9e3">


The negative sign indicates an inverse relationship between cacao percentage and rating– as cacao percentage increases, the rating seems to decrease. However, the magnitude of the correlation coefficient is only 0.14, suggesting that cacao percentage is not a strong predictor of a chocolate’s rating.

**Validity of the Linear Regression**

When predicting chocolate ratings from cacao percentage, is linear regression an accurate way to model the data? The residual plot below offers insight into whether linear regression is a good measure of the relationship between cacao percentage and chocolate ratings:

<img width="917" alt="Screenshot 2024-04-11 at 3 46 48 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/c5aaf13f-e7f6-4c2a-b805-6d8922988a70">


<img width="684" alt="Screenshot 2024-04-11 at 3 46 49 PM (2)" src="https://github.com/adityakmehrotra/Cocoa-Percentage-vs-Rating/assets/24847438/dd11303a-d42c-4306-8130-a8aae8923718">


When judging off of the residuals, it appears that this is not a bad linear regression model, there is relatively consistent distribution and spacing of points on either side of the line at 0.


**Assumptions for Linear Regression**

The residual plot suggest evidence that the homoscedasiticity and linearity assumption has been met. However, the Q-Q plot suggests that we may not be able to assume normality. 

## Discussion

>Through our analysis, a p-value of 1.935e-13 was obtained. Since the p-value is below the alpha level of 0.05, this finding is statisticially significant and we reject the null hypothesis. our findings conclude that cacao percentage does affect chocolate rating. Using a linear regression model, it is predicted that for every 1 percentage point increase in cacao percentage, rating will decrease by 0.01134 ($\beta_1$ = -0.011334). Based on our 95% confidence interval of -0.01434028 to -0.008326993,  we are  95% confident that the true slope lies between these two values. The correlation coefficient between cacao percentage and chocolate rating is -0.14, indicating a weak inverse linear relationship between the two. Contradictory to our initial question, our results state that higher cacao percentage actually leads to lower ratings.

### Shortcomings of Our Analysis
Since the ratings of chocolate are in part due to the personal taste preferences of each judge, our analysis could not account for this possible confounding factor. In addition, other variables we did not analyze such as the 'notable characteristics' column and ingredients could have affected chocolate ratings in addition to cacao percentage. It is also important to note that different types of cacao beans are used depending on the location of chocolate manufactuer. Even then, different harvesting and bean roasting processes affect the cacao taste and quality and thus the overall taste of the chocolate bar. These are not reflected in the dataset. These shortcomings pave the way for future questions to analyze.

### Potential Future Directions
**Questions:**

How might the climate of the regions affect bean production and thus bean quality?

How can the location of the chocolate company or bean origin have a significant impact on ratings?

How might different types of cacao beans affect chocolate bar rating?
    
**New data to collect to refine our understanding:**

The ratio of the ingredients listed for each bar could be collected to better understand the effect of ingredients and their added amount on ratings for chocolate taste. It would also be interesting to collect the price of each chocolate bar and examine if more expensive chocolate receives higher ratings. One more factor could be the type of bean used for chocolate– forastero, criollo, and trinitario are the most commonly used types of bean in the chocolate tried by the Manhattan Chocolate Society. Further exploration of our question could include seeing how the combination of bean type and cacao percentage affects the rating. 
    

### References

Source of Data:
https://flavorsofcacao.com/chocolate_database.html

Introduction:
https://theochocolate.com/blog/understanding-cocoa-percentages/

### Last Updated
12/13/2023
