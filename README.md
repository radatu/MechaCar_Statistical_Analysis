# MechaCar_Statistical_Analysis_Ch_16
D1—Linear Regression to Predict MPG/D2—Part 2: Create Visualizations for the Trip Analysis/D3—Part 3: T-Tests on Suspension Coils/Part 4: Design a Study Comparing the MechaCar to the Competition

# Data Analysis Report
The following report analyzes data related to different aspects of vehicles, such as length, weight, spoiler angle, ground clearance, all-wheel drive (AWD), and miles per gallon (mpg). The data set consists of 40 observations.

## Deliverable 1—Linear Regression to Predict MPG
The linear regression analysis was performed on the MechaCar dataset to predict the mpg values. From the output of the analysis, we can see that the variables/coefficients that provided a non-random amount of variance to the mpg values are the vehicle length and the ground clearance, as they both have a significant p-value of less than 0.05.

The slope of the linear model is not considered to be zero because the p-value of the overall regression analysis is 5.35e-11, which is much less than the significance level of 0.05. This indicates that there is enough evidence to reject the null hypothesis, which states that the slope is zero.

The linear model predicts the mpg of MechaCar prototypes effectively to some extent, as the R-squared value is 0.7149, which means that approximately 71.49% of the variability in the mpg values can be explained by the linear model. However, there may be other factors not included in the model that also affect the mpg values. Therefore, the model may not be able to predict the mpg values accurately in all scenarios.

### Summary Statistics
The following table presents the summary statistics of the data set:

Feature	Minimum	Maximum	Mean	Standard Deviation
vehicle_length	12.000	20.000	14.95896	1.377958
vehicle_weight	2000.0	10000.0	5961.419	1964.603
spoiler_angle	0.0	90.0	51.86831	26.959870
ground_clearance	0.0	18.0	12.49142	3.311456
AWD	0.0	1.0	0.475000	0.505736
mpg	10.000	80.000	34.42208	14.341995
Some observations that can be made based on these statistics are:

Vehicle length ranges from 12.000 to 20.000, with an average length of 14.95896.
Vehicle weight ranges from 2000.0 to 10000.0, with an average weight of 5961.419.
Spoiler angle ranges from 0.0 to 90.0, with an average angle of 51.86831.
Ground clearance ranges from 0.0 to 18.0, with an average clearance of 12.49142.
AWD is a binary variable that ranges from 0 to 1, with an average of 0.475.
Miles per gallon ranges from 10.000 to 80.000, with an average of 34.42208.
Correlation Analysis
The following table presents the correlation coefficients between the features:

vehicle_length	vehicle_weight	spoiler_angle	ground_clearance	AWD	mpg
vehicle_length	1.000000	0.758465	-0.109846	0.376443	-0.057777	-0.370678
vehicle_weight	0.758465	1.000000	-0.103848	0.264069	0.128217	-0.554837
spoiler_angle	-0.109846	-0.103848	1.000000	-0.016172	0.168491	0.160664
ground_clearance	0.376443	0.264069	-0.016172	1.000000	-0.189628	-0.583510
AWD	-0.057777	0.128217	0.168491	-0.189628	1.000000	0.349835
mpg	-0.370678	-0.554837	0.160664	-0.583510	0.	


## Deliverable 2—Suspension Coil Trip Analysis
For the MechaCar Suspension_Coil.csv dataset, the summary statistics table shows that the overall manufacturing process for the suspension coils appears to be consistent, with a mean PSI of 1498.78, median PSI of 1500, variance of 62.29356, and standard deviation of 7.892627.

However, when looking at the manufacturing lots individually, there are some notable differences. Lot 1 appears to be the most consistent, with a mean PSI of 1500, median PSI of 1500, variance of 0.9795918, and standard deviation of 0.9897433. There are virtually no outliers for Lot 1.

Lot 2 has a slightly higher mean PSI of 1500.20, but a higher variance of 7.4693878 and standard deviation of 2.7330181. There is one outlier for Lot 2 below the range.

Lot 3 has the most variation, with a mean PSI of 1496.14, median PSI of 1498.5, variance of 170.2861224, and standard deviation of 13.0493725. There are many outliers for Lot 3 both well above and well below the range of expected values.

Overall, the summary statistics suggest that Lot 1 has the most consistent manufacturing process, while Lot 3 has the most variation and should be further investigated.

## Summary Statistics
In summary, the total_summary dataframe shows that the variance of the suspension coils across all manufacturing lots is 76.23459 PSI, which is below the design specification of 100 PSI. However, when looking at each lot individually, it becomes clear that Lot 3 has a much higher variance of 170.2861224 PSI, which exceeds the design specification. Lot 1 and Lot 2 both have variances of 0.9795918 PSI and 7.4693878 PSI, respectively, which are both below the design specification. Therefore, it can be concluded that the current manufacturing data meets the design specification for Lot 1 and Lot 2, but not for Lot 3.

   /Rplot_Suspension_Coils_Full_group_PSI.png
   /Rplot_Suspension_Coils_PSI_by_Lot.png.png

## Deliverable 3—Summary Statistics on Suspension Coils:

The t-test results show that the PSI across all manufacturing lots is not statistically different from the population mean of 1,500 pounds per square inch, with a p-value of 0.06028, which is above the significance level of 0.05. However, when looking at each lot individually, we find that Lot 1 and Lot 2 have p-values above the significance level, indicating that the PSI for these two lots is not statistically different from the population mean of 1,500 pounds per square inch. On the other hand, Lot 3 has a p-value below the significance level, indicating that the PSI for this lot is statistically different from the population mean of 1,500 pounds per square inch.

Overall, the manufacturing process appears to be consistent with the design specifications for the MechaCar suspension coils, as the PSI values are not significantly different from the population mean for all manufacturing lots combined and for two of the three lots individually. However, there may be some issues with the manufacturing process for Lot 3, as its PSI values are significantly different from the population mean.

Screenshots of the t-test results for all manufacturing lots and each lot individually are included below:

   t-test-all-lots 

t-test-lot1

t-test-lot2

t-test-lot3

## Deliverable 4—Study Design: MechaCar vs Competition
To compare the performance of MechaCar vehicles against other manufacturers, a statistical study can be designed to examine the cost and fuel efficiency of MechaCar vehicles in comparison to its competitors. The following are the details of the study design:

Metric: The metrics that will be tested in this study are the cost and fuel efficiency of MechaCar vehicles compared to those of its competitors. The study will focus on the fuel efficiency of the vehicles on both city and highway roads, as well as the cost of the vehicles.

Null Hypothesis: MechaCar vehicles have the same cost and fuel efficiency as its competitors.

Alternative Hypothesis: MechaCar vehicles have a different cost and fuel efficiency compared to its competitors.

Statistical Test: A two-sample t-test will be conducted to test the hypothesis. The two-sample t-test will help to determine whether there is a significant difference between the mean cost and fuel efficiency of MechaCar vehicles compared to those of its competitors. The t-test is appropriate because it can determine if there is a significant difference between the means of two independent groups.

Data Needed: The data that is needed for the study will be the cost and fuel efficiency of MechaCar vehicles and its competitors. The data can be obtained from various sources such as official manufacturer websites or independent testing organizations. Additionally, the sample size and distribution of data should be considered in the statistical analysis. It's important to have a large enough sample size to ensure the results are representative of the population. Additionally, the data should be normally distributed to ensure the validity of the t-test.

Overall, this statistical study will provide valuable insights into how MechaCar vehicles perform in comparison to its competitors. By examining the cost and fuel efficiency of the vehicles, consumers can make more informed decisions when purchasing a car, while MechaCar can use the results to improve their products and marketing strategies.
