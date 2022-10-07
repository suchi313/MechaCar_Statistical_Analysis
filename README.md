# MechaCar Statistical Analysis in R

During the course of this module, I utlized the DPLYR library within R. I was able to design a linear model that predicted the MPG of MechaCar prototypes by using key data points such as vehicle length, vehicle weight, ground clearnance, etc. 

## The analysis consisted of the following 4 deliverables:

1. Performing/creating a multiple linear regression analysis that identified and determined which variable in the dataset predicted the MPG of MechaCar Prototypes. 
2. Collecting summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
4. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Resources:
1. Data Source: MechaCar_mpg.csv and Suspension_Coil.csv
2. Data Tools: tidyverse, dplyr, ggplot2 and MechaCarChallenge.RScript.
3. Software: RStudio and R

## Linear Regression to Predict MPG
We designed a linear model that predicted the MPG of the prototypes using both the summary() AND lm() functions. We had to use as mentioned earlier: vehicle length, vehicle weight, spoiler angle, ground clearance, and AWD as independent variables. As shown in the picture below - you can see a summary of the results and outputs.

![linear_regression](https://user-images.githubusercontent.com/102767530/194447883-42d182d4-9825-4326-a727-016f35b7824d.png)

### Highlights - 
1. Vehicle_weeight, spoiler_angle and AWD = all provide NON RANDOM amount of variance. This means, the maximum random variance was provided by ground_clearence and vehicle_length
2. Slope is not equal to 0 because the p-value is LESS than 0 (5.35e-11).
3. The R squared value is 0.7149 or 71.5% ~ 72%. This implies that there's a 72% chance that the predications made from this linear regression model are correct. 

## Summary Statistics on Suspension Coils
To align if the manufacturing process of the suspension coils is consistent - I created 2 data frames with summary statistics about the suspension coil's PSI across ALL manufacturing lots for each lot. The first dataframe showcases the suspension coil's PSI continuous variable across all the lots. 

![total_summary](https://user-images.githubusercontent.com/102767530/194448830-c6ffd6ce-3358-44c5-ad42-926de2cb9870.png)

This second image showcases the LOT summary by individual lot. 

![lot_summary](https://user-images.githubusercontent.com/102767530/194448965-0e879ca1-9505-422a-8e3b-f629e3660894.png)

### Highlights - 
1. As seen, Lot 1 and 2 are nearly identical other than the data in variance and SD. Lot 3 in comparison to lot 1 + 2 has a small mean and noticibaly larger variance and SD.

## T-Tests on Suspension Coils
By using one-sample t-test, we were able to test and see if the manufacting lots collectively + each individual lot were statistically different from the population mean of 1,500lb per square inch. The P-values from single T-Test on PSI values for suspension coils were as follows - 

All  PSI = 0.06028 
Lot 1 PSI= 1
Lot 2 PSI= 0.6072 
Lot 3 PSI= 0.04168 

Only lot 3 is noticably different and potentially even underperforming. All the other lots performed the same to the standard of 1,500 PSI. 
![t_test](https://user-images.githubusercontent.com/102767530/194449940-6d1c568c-8938-4791-bcc8-d10bcc2be05c.png)
![t_test1](https://user-images.githubusercontent.com/102767530/194449942-c9c2d233-204d-4126-9e9b-e410646fd03c.png)
![t_test2](https://user-images.githubusercontent.com/102767530/194449951-9a33ba34-755c-4ddb-9d86-7f8a25c860d3.png)
![t_test3](https://user-images.githubusercontent.com/102767530/194449959-0a746260-480c-4681-a103-dbbbe478deb0.png)

## Study Design: MechaCar vs Competition

As MechaCar will be in dealerships, it's misison critical to ensure that it's performance measures up and potentially outperforms it's compititors. 

Reccommendation: Moving forward, I would like the opportunity to perform a statistical study in order to determine if we accurately predicted values for our key variables by using a linear model and values from cost. 

A study that can be conducted in addition to the one above is an ANOVA test to compare the MechaCar in various categories that customers would be interested in. These categories could include but are not limited to - cost, city, gas efficeny, child safey, general safety rating, seatbelt efficenty, maintence cose. The data needed to perform this test would be the categories mentioned earlier. 
