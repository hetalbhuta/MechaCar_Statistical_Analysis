# MechaCar_Statistical_Analysis
## Project Overview
This project involves the use of statistics and hypothesis testing to analyze a series of datasets from the automotive industry.
All the statistical analysis and visualizations is written in the R programming language.
## Linear Regression to Predict MPG
 1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
Vehicle weight, spoiler angle & AWD provided a non-random amount of variance. The two variables that had the most amount of random variance are ground clearance and vehicle length.
 2. Is the slope of the linear model considered to be zero? Why or why not?
Our slope is not zero just be looking at the p-value, which is less than 0.05.
 3.	Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
Our R-squared value is 71%, which means roughly ~71% of the time the model will predict mpg values correctly. There are probably other factors that were not captured in the dataset that contribute to the mpg variability of the MechaCar prototypes.
## Summary Statistics on Suspension Coils,
 1.	The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
 2. Lot 1 and Lot 2 are both within design specifications and have nearly the same exact mean and median. Lot 3 shows the most variance and exceeds the manufacturers specs.
## T-Tests on Suspension Coils
1.	Lot 1 and Lot 3 the PSI values are not different from the population mean. However, lot 2 the p-value is .347 which means there is evidence that the suspension coil is different from the population mean. All t-tests can be seen below:
## Across all lots:
### Lot 1
![image](https://user-images.githubusercontent.com/86137857/138008390-ef3738c6-9edb-4b0f-b998-de86b7ca07d0.png)

###  Lot 2:
![image](https://user-images.githubusercontent.com/86137857/138008446-2bb5f7e5-1ee9-4104-b778-674fb590ed10.png)

###  Lot 3:
![image](https://user-images.githubusercontent.com/86137857/138008470-b8d74877-cacf-4dff-b8fc-0aec6dac0647.png)


###  Lot 4:
![image](https://user-images.githubusercontent.com/86137857/138008525-f6c226e4-f66e-4c44-9b6e-70f221eb62d0.png)

# Study Design: MechaCar vs Competition
To compare the performance of the MechaCar prototype against the vehicles from the competition, we will perform a statistical analysis based on the following metrics:
 1. the "0 to 60 mph" time,
 2. the braking distance,
 3. the fuel economy (mpg),
 4. the power,
 5. the safety rating.

In our case the null hypothesis would be each performance metrics is statistically similar between the MechaCar prototype and all vehicle from the other manufacturers.
We would use a one-way ANOVA test. This test is used to compare the means of a continuous numerical variable across several groups. So in this analysis we would compare the means for each metric across the different manufacturers.

To perform the test, we would need data of MechaCar vehicles and its competition, all gathered in a single data frame where each metric is a column.
The data could be scraped from vehicle data APIs such as scrapinghub.com/data-api-vehicle or carqueryapi.com.


