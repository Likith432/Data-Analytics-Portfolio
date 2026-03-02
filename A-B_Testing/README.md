## A/B Testing Report: Facebook vs. AdWords Campaign Performance Analysis

### Business Problem
As a marketing agency, our primary objective is to maximize the return on investment (ROI) for our clients' advertising campaigns. We have conducted two ad campaigns, one on Facebook and the other on AdWords, and we need to determine which platform yields better results in terms of clicks, conversions, and overall cost-effectiveness. By identifying the most effective platform, we can allocate our resources more efficiently and optimize our advertising strategies to deliver better outcomes for our clients.

### Research Question
Which ad platform is more effective in terms of conversions, clicks, and overall cost-effectiveness?

### Methodology
Our analysis involved a comprehensive examination of daily campaign data for both Facebook and AdWords throughout 2019. The methodology encompassed several key steps:

1.  **Data Overview and Cleaning**: Initial inspection of the dataset, including data types and basic statistics, followed by conversion of relevant columns (e.g., Date, Cost, Rate) to appropriate formats.
2.  **Distribution Analysis**: Visualization of the distribution of ad clicks and ad conversions for both platforms using histograms to understand their spread and frequency.
3.  **Comparison of Conversion Categories**: Categorization of daily conversions ('less than 6', '6 - 10', '10 - 15', 'more than 15') for both platforms and a comparative bar chart to illustrate the frequency of days within each category.
4.  **Correlation Analysis**: Calculation of Pearson correlation coefficients between ad clicks and ad conversions for each platform to quantify the strength and direction of their linear relationship.
5.  **Hypothesis Testing**: A two-sample independent t-test to compare the mean conversions between Facebook and AdWords, with the null hypothesis being that there is no difference or AdWords conversions are greater than or equal to Facebook conversions.
6.  **Linear Regression (Facebook)**: Development of a linear regression model to predict Facebook Ad Conversions based on Facebook Ad Clicks, and evaluation of its accuracy using R2 score and Mean Squared Error.
7.  **Time-based Analysis (Facebook)**: Extraction of month and weekday information from the 'Date' column to analyze weekly and monthly conversion patterns using bar and line charts.
8.  **Monthly Cost Per Conversion (Facebook)**: Calculation and visualization of the monthly Cost Per Conversion (CPC) to understand cost-effectiveness trends over time.
9.  **Cointegration Testing**: Application of a cointegration test between Facebook advertising spend and Facebook ad conversions to determine if a long-term equilibrium relationship exists.

### Key Findings

#### Campaign Comparison (Facebook vs. AdWords)

*   **Distribution of Clicks and Conversions**: Histograms for both Facebook and AdWords ad clicks and conversions generally showed a somewhat symmetrical shape, indicating that values are relatively evenly distributed without extreme outliers. This suggests a consistent range of daily performance.
    *   <img width="1229" height="547" alt="image" src="https://github.com/user-attachments/assets/2a6babb1-885b-4907-bcbd-0d6a7e34d2cc" />
    *   <img width="1229" height="547" alt="image" src="https://github.com/user-attachments/assets/19d35e3b-3025-47b0-a2c6-a158b142e08e" />


*   **Frequency of Daily Conversions by Category**: 
    *   Facebook exhibited significantly more days with higher conversions, particularly in the '10 - 15' and 'more than 15' categories (189 and 47 days, respectively). 
    *   AdWords, in contrast, primarily had days in the 'less than 6' (156 days) and '6 - 10' (209 days) conversion categories, with no days exceeding 10 conversions. This stark difference highlights Facebook's superior ability to drive higher-volume conversions.
    *   <img width="1238" height="549" alt="image" src="https://github.com/user-attachments/assets/ed0adb19-05d3-474c-8035-718f6e0b0762" />


*   **Correlation between Ad Clicks and Ad Conversions**: 
    *   **Facebook**: A strong positive correlation coefficient of **0.87** was observed between Facebook Ad Clicks and Facebook Ad Conversions. This implies that increased clicks on Facebook ads are highly predictive of increased conversions, suggesting Facebook is very effective at converting interest into action.
    *   **AdWords**: A moderate positive correlation coefficient of **0.45** was found for AdWords Ad Clicks and Ad Conversions. While clicks do lead to conversions, the relationship is not as strong as Facebook, indicating other factors might influence AdWords conversion effectiveness.
    *   <img width="1229" height="547" alt="image" src="https://github.com/user-attachments/assets/f3a8b606-e58e-4b8f-bb53-7e3004e914d4" />


*   **Hypothesis Test for Mean Conversions**: 
    *   **Mean Conversions**: Facebook averaged 11.74 conversions per day, while AdWords averaged 5.98 conversions per day.
    *   **T-statistic**: 32.88
    *   **P-value**: 9.35e-134
    *   **Conclusion**: With a p-value significantly less than 0.05, we **reject the null hypothesis**. This provides strong statistical evidence that the number of conversions from Facebook is significantly greater than from AdWords.

#### Facebook Campaign Specific Analysis

*   **Linear Regression Model for Facebook Ad Conversions**: 
    *   **Accuracy (R2 Score)**: 76.35%
    *   **Mean Squared Error (MSE)**: 2.02
    *   **Implications**: The model demonstrates a reasonably good predictive power, indicating that Facebook Ad Clicks can effectively predict Facebook Ad Conversions. For example, 50 clicks are expected to yield 13 conversions, while 80 clicks are expected to yield 19.31 conversions. This model is valuable for setting realistic conversion goals and optimizing ad spend.
    *   <img width="687" height="525" alt="image" src="https://github.com/user-attachments/assets/ab572eee-71da-436d-8663-c754b9860eab" />


*   **Weekly Conversions**: Conversions remained relatively consistent throughout the week. However, **Mondays and Tuesdays consistently showed the highest conversion rates**, suggesting increased user engagement at the beginning of the workweek.
    *   <img width="676" height="451" alt="image" src="https://github.com/user-attachments/assets/b7c4c217-18a7-40e2-b5da-ff7b18f3051e" />


*   **Monthly Conversions**: The monthly trend indicated an overall upward trajectory in conversions throughout the year. However, **February, April, May, June, August, and November experienced noticeable declines** in conversions compared to adjacent months, possibly due to seasonal factors or campaign adjustments.
    *   <img width="676" height="451" alt="image" src="https://github.com/user-attachments/assets/1ab51ff6-8af1-4e60-9e10-08a8802363f7" />


*   **Monthly Cost Per Conversion (CPC)**: The CPC fluctuated but remained relatively stable. **May and November recorded the lowest CPC values**, indicating more cost-effective conversion periods. **February had the highest CPC**, suggesting higher advertising costs or lower efficiency during that month.
    *   <img width="671" height="451" alt="image" src="https://github.com/user-attachments/assets/c25221ad-da2f-4db9-b5cd-e3f0eebb2f20" />

*   **Cointegration Test**: 
    *   **Cointegration test score**: -14.755
    *   **P-value**: 2.13e-26
    *   **Significance**: With a p-value less than 0.05, we **reject the null hypothesis**. This indicates a long-term equilibrium relationship between Facebook advertising spend and conversions, implying that changes in spend have a stable, proportional impact on conversions over time.

### Overall Conclusion and Recommendations

Based on the comprehensive analysis, the **Facebook ad platform is significantly more effective** in terms of conversions, clicks, and overall cost-effectiveness compared to AdWords.

*   **Superior Conversion Volume**: Facebook consistently delivers a higher volume of conversions, with more high-conversion days and a significantly higher mean conversion rate.
*   **Stronger Click-to-Conversion Relationship**: The strong correlation and predictive power of clicks on conversions for Facebook indicate its efficiency in converting initial interest into desired actions.
*   **Cost-Effectiveness Potential**: While CPC fluctuates, identifying periods like May and November with lower CPC offers opportunities for optimized budget allocation.
*   **Stable ROI**: The cointegration between ad spend and conversions on Facebook suggests a reliable return on investment over the long term.
