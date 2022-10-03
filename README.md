# MechaCar_Statistical_Analysis
*Module 15 Challenge*

## Overview: 

*Background and Purpose:*

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Deliverable 1: Linear Regression to Predict MPG

*Linear Regression to Predict MPG*

![Summary of Linear Regression Model](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/LRtopredictMPG.png)


![](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/MPG2.png)


![](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/coefficients.png)


### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle ground clearance and the vehicle length both provided a non-random amount of variance to the MPG values within the data. They both are statistically likely to have a significant effect on the MPG on the MechaCar. 

The rest of the variables (vehile weight, spoiler angle, and all wheel drive) are not indicated as providing a non-random amount of variance to the MPG values. This means that they are not going to signficantly alter the MPG.

### Is the slope of the linear model considered to be zero? Why or why not?

The slope of the linear model is considered to be NOT zero because the p-value that was calculated was 5.35e-11. This is important because the p-value is compared to a set significance level of 0.05%. The resulting p-value was much lower than the assumed significance level, which allows the rejection of the null hypothesis. The null hypothesis was that there was no effect by any of the factors influencing the dependent variable, so once this is rejected, it can be claimed that the slope of linear model is not zero because there was an effect on the dependent variable. 

### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The linear model does predict the MPG of the MechaCar prototypes effectively because the linear model has the critical values for F-distribution alpha equals to 0.05, F = 2.427 < 22.07 , also P-value is5.35e-11 less than 0.05, statistically signically and r-squared value of 0.7149 and. This is equivalent to 71.5% of all the MPG predictions can be determined using the created model. 

## Deliverable 2: Create Visualizations for the Trip Analysis

### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

![Lot Summary](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.png)

![Total Summary](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.png)

The total summary of all the lots shows a variance of 62.29 PSI, which meets the design specifications that requires the variance of the suspension coils to not exceed 100 pounds per square inch. 

The lot summary that is broken up between 1, 2, and 3 offers a bit more insight into the data though. Lot 1 and 2 are both within the 100 PSI design specification because they both have variances of 0.98 and 7.47, respectively. Lot 3 is a very different though, with a variance of 170. This means that lot 3 is having a huge effect on the total lot summary.

## Deliverable 3: T-Tests on Suspension Coils

*T-Test of All the Manufacturing Lots:*

![All Manufacturing Lots](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_suspension_coil.png)

To compare to the calculated T-test, we must assume a population mean of 1500. The mean of the total lot summary is actually 1498.78. As seen by the p-value of 0.06028 > 0.05, which is above our significance level; therefore we must fail to reject the null hypothesis. The mean of the three lots is statistically similar to the presumed population mean of 1500.

![Lot1T-Test](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot_1.png)

Lot 1 actually does have a true sample mean of 1500, which was the presumed mean. The p-value is exactly 1 > 0.05, which is above our significance level; therefore, we fail to reject the null hypothesis. The null hypothesis states that there is no statistical difference between the presumed mean of 1500 and the true sample mean of 1500.

![Lot2T-Test](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot_2.png)

Lot 2 has the sample mean value of 1500.02 and a p-value of 0.61 > 0.05, which is above our significance level; therefore, we fail to reject the null hypothesis in this lot as well. The sample's true mean of 1500.02 and the presumed mean of 1500 are statistically similar. 

![Lot3T-Test](https://github.com/nadiezhdamhb/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot_3.png)

Lot 3 was a much different situation. The sample mean is 1496.14 with a p-value of 0.04 < 0.05, which is below our significance level. In this case we can reject the null hypothesis. This means that the sample mean of 1496.14 and the presumed mean of 1500 are statistically different. 

## Deliverable 4: Design a Study Comparing the MechaCar to the Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

- To compare the performance of the MechaCar against the competition, we have to think about other metrics that would be of interest to a customer, such as cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating. One of metrics we are going to test is highway fuel efficiency.

In your description, address the following questions:
What metric or metrics are you going to test?

- The metric to be part of the test would be 'highway fuel efficiency'. how the vehicle's composition affect fuel usage.

What is the null hypothesis or alternative hypothesis?

H0 = The fuel economy of the MechaCar prototype is not signicantly different that the fuel economy of the equivalent vehicle type of a competitor company.
(The means are equal)

H1 = The fuel economy of the MechaCar prototype is significantly different than the fuel economy of the equivalent vehicle type of a competitor company.
(The means are Not equal)

What statistical test would you use to test the hypothesis? And why?

- I will use T-test (would try two-sample) to perform the hypothesis, to use the p-value comparing with significance level was the common 0.05 percent.

What data is needed to run the statistical test?

- To collect random sample of MechaCar and competitor, the sample size should be n > 30, by using vehicle weight, driving behaviour: rapid acceleration, speeding, driving at incosistent speeds. Also enviromental factors such as vehicle air conditioning and weather. 
