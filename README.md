# Supplemental Nutrition Assistance Program (SNAP) Performance Evaluation from 2016-2018 in Hennepin County, MN

## Background 
![Capture4](https://user-images.githubusercontent.com/76879882/103466892-004fa580-4d0f-11eb-84f9-5b967f73444e.PNG)

Supplemental Nutrition Assistance Program, or SNAP for short, is a federal program that provides nutrition benefits to supplement the food budget of needy families so they can purchase healthy food and move towards self-sufficiency. Besides its effect on combating food insecurity, it also serves as one of the most effective ways to stimulate local economics, where each dollar in SNAP benefits generates $1.79 in economic activity. 

Statistics show that 1 in 8 Minnesotans is affected by hunger or faced with some level of food insecurity. They either do not have enough food to eat, or they have to sacrifice their nutrition needs because of a low budget. So far, SNAP has reached out to 7% households and 400, 101 individuals on a monthly basis, but there are people still struggling to fulfill their nutrition needs, either because they are unaware of SNAP or need help filling their applications. In order to best assist Hennepin County to target eligible person, we first need to evaluate SNAP Performance.

## Problem Definition
Historically, Hennepin County has been using internal metrics such as “how fast the process of an application” to define success, and focused mainly on people who are already in the program. With the lack of a consistent success measurement, Hennepin County struggles to identify and target people that suffer from food insecurity. In order to understand the gap between people that are eligible for SNAP and those who are already in the program, we decide to come up with two performance metrics on Census Tract level. One is the penetration rate, defined as the number of enrolled divided by number of eligible; the other is the number of people that are missing out from SNAP. With these two success measurements, we further analyze any disparities across geographics and demographics, and provide actionable insights to improve SNAP uptake. 

## Methodologies 
We decide to calculate SNAP penetration rates per tract first, and based on that we do a clustering analysis on demographics such as ages, races and gender etc, where
demographics information is selected based on the significance of its relationship with penetration rates using linear regression. Same applies to number of people missing out from SNAP.

### Estimate number of people that are eligible for SNAP
To calculate SANP penetration rates per tract, we need to first estimate the number of eligible people per tract. Since SNAP eligibility is defined on a household level where 
different household sizes correspond to different income thresholds, we decide to estimate the number of eligible households and translate eligible households into eligible people. For example, if a 4-person household is eligible, then we would say all people in that household, a total of 4, are eligible for SNAP. We assume that income distribution per household size and per tract follows a T-Distribution, with median income as the mean and standard deviation can be calculated from margin of error (std = moe * sqrt(sample size) / z-score). Using cumulative density function for T-Distribution and the corresponding income threshold per household size, we can find out the percentage of houses with household income less than the SNAP income threshold. Using the percentage times number of houses and number of people per houses, we can esitmate the number of people that are eligible for SNAP. 

### Estimate SNAP enrollment 
Since people on average stay on SNAP for about 3 months, we decide to use a rolling 3-month window to estimate SNAP enrollement. 

## Data Source 
![Capture1](https://user-images.githubusercontent.com/76879882/103465788-8c100480-4d04-11eb-8a9f-c82bccebe488.PNG)

## Insights and Recommendations 
### Overview 
![Capture3](https://user-images.githubusercontent.com/76879882/103466678-9a621e80-4d0c-11eb-8b27-d34f8b81c6ea.PNG)

### Tracts to focus on 
![Capture2](https://user-images.githubusercontent.com/76879882/103466437-d5635280-4d0a-11eb-90ff-8c6c29b96f3a.PNG)

### Age Group to focus on 
Further investigation shows that seniors (age 65+) have a higher proportion in those focused tracts listed above. Data shows that 3 out 5 seniors are missing out on SNAP benefits in the US. Therefore, we believe besides focusing on tracts that have low penetration rates and high miss-out number, we also recommend Hennepin County provide extra help to seniors. We assume many seniors might not be aware of SNAP benefits, hence, we recommend putting out ads on radios since U.S. adults aged 50-64 listen to almost 15 hours of radio a week while adults 65+ listened to about 12 hours of radio weekly. Content can have an emphasis on medical expense deduction that would lower the income threshold for SNAP (only 16% utilize that), so that seniors can have a clue of whether they are eligible or not. Besides. we believe applications in paper format might not be accessible to seniors and many seniors struggle to apply online. we recommend mailing applications to seniors and putting paper application forms in places which are easily accessible to seniors, such as hospitals and SNAP eligible stores. 






