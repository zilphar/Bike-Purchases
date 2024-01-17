# Bike-Purchases

Bike purchase is an analysis that will provide insights on the different customer segments and their Bike purchase patterns. The analysis will be valuable to the business which is seeking to understand their customers and shape their market and sales through strategic and informed decision making. 

To be able to communicate an analysis, it is important to understand the specific needs and objectives of stakeholders. In this Project, I will dive into the phases of data analysis including:
1. ASK
2. PREPARE
3. PROCESS
4. ANALYZE
5. SHARE 

**Overview of the Dataset**

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/cc65c36f-b8bf-4ad6-abd7-704158a2656b)

The Table has 1027 rows and 13 columns. Data contained in each column:

1. ID - This is the primary key that identifies each of the customers. 
2. Marital status - Identifies the status of the customers either married or single.
3. Gender - Identifies either female or male customers.
4. Income - The earnings of each customer.
5. Children - Identifies the number of children the customers have.
6. Education - Identifies the level of education the customer has reached.
7. Occupation - Identifies the occupation of the customer.
8. Home owner - Identifies whether the customer owns a home.
9. Cars - Identifies the number of cars the customers has.
10. Commute Distance - Identifies how long te customer commute distance is.
11. Region - Identifies the location of the customer
12. Age - Identifies the age of the customer.
13. Purchased Bike - Identifies whether the customer bought a bike or not.

****<ins>1. ASK</ins>****

This phase of the analysis includes asking the right questions to answer the goals and objectives of your stakeholders.

In this phase we get to ask **What is the purpose of the analysis?** and **what are the expectations of the stakeholders?**. 

*#The purpose of this analysis is to derive the trends of Bike purchases in different customer demographics.*

*#The stakeholders in this case is the ****<ins>Sales Team</ins>**** which focuses on directly engaging customers and achieving sales targets. They are also interested in customer demographics and purchasing patterns and an analysis of this dataset will give them an overwiew of how sales have been happening in different customer demographics.* 

In this dataset we get to answer the following questions concerning *key performance indicators(KPI)*:

1. What is the percentage of people who purchased a bike?
2. Is there a correlation between income levels,age, and commute distance and the likelihood of purchasing a bike?
3. What types of occupations are more likely to result in bike purchases?
4. Is there a correlation between education levels, and bike purchases?

****<ins>2. PREPARE</ins>****

Preparing phase includes identifying the data that is required to answer the stakeholder questions. In this case we have the *"Bike Purchase"* dataset to work with. 

****<ins>3. PROCESS</ins>****

The process phase includes cleaning and transforming the data to ensure intergrity. 
1. Freezing the first row which contains the column headers and bolding it. 
2. Removing duplicates (Data tab --> Remove duplicates). 26 duplicate values were removed leading to remainder of 1001 rows.

    ![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/83bbe42f-7b95-4669-bd95-416f6c9ea9a9)
4. Checked the data contained in each column to ensure no blanks.

   The naming convention for the *"Marital Status"* and the *"Gender"* column are a possibility of confusion. Changed the naming to:

   Marital status: M to Married, and S to Single.
   
   Gender: F to Female, and M to Male.

   The currency in the *"Income"* column has two zeros. To make it more presentable and easy to visualize in charts, I removed the number of zeros.

   In the *"Commute Distance"* column, the "10+ miles" which is the largest distance lies as the second in the list.

   ![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/42b2074d-ddbc-4b78-8f07-2e010dbb047f)

   I renamed the values using *"find and replace"* to "More than 10 Miles". Renaming it corrects the list.

   ![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/7507c866-7fa1-44a2-a36f-238d8f386378)

5. As for the "Age column", I created another "Age bracket" Column for easy representation of the age brackets where the customers lie.

   I did this using the Nested IF formula in excel: **=IF(L2>54, "Old age", IF(L2>30, "Middle age", IF(L2<31, "Young age"))).** 
   This grouped the customers with age **55 and above as Old age**, **31 to 54 years as Middle age**, and **30 years and below as Young age.**

   The final table looks like this with 1000 rows and 14 columns:

   ![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/1af965f9-7c60-4f49-8fb6-6e58969e3f56)

****<ins>4. ANALYZE</ins>****

The analyze stage of the analysis includes using the cleaned and transformed data to draw conclusions that are data driven. 

The dashboard after the analysis looks like this: 

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/a38cfcc0-6416-4177-933d-eb86b6376515)

The maximum customer income calculated using =MAX() = $170,000 

The minimum customer income =MIN() = $10,000

The average customer income =AVERAGE() = $ 56,360 

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/34f59f05-3ec7-47b2-987c-a3965bd1f34d)


**Breaking down the Dashboard** 

*The dashboard answers ***The four questions*** of the stakeholders.*

From the analysis, **The title of the dashboard** indicates what the analysis is about. After that is the main visualizations that aligns with the objectives of the stakeholders. 

The left side contains slicers which act as filters for the visualizations. *For example let say you want to view the visualizations analytics for only female customers, then that will include pressing on the **Female** part of the **Gender** slicer.* 



****<ins>5. SHARE</ins>****

The share phase of analysis includes intepreting and communicating results to stakeholders to make data driven decisions. 

Our stakeholders are the sales team so let's breakdown the results/insights we have gathered from the analysis by answering the four questions. 


**1. What is the percentage of people who purchased a bike?** 

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/61572ab1-2dc4-4058-be35-f99ceef7977f)

48% of the customers which equals 481 customers whose data was collected purchased a bike while 52% of them did not purchase. 

This can be considered a positive sign especially if the company is planning to increase bike sales. The purchase rate indicates a notable demand for bikes by customers. If there are effective marketing startegies in the company to capitalize this demand, then this is particulary positive. 

**2. Is there a correlation between income levels,age, and commute distance and the likelihood of purchasing a bike?** 

***Income Levels***

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/d172da75-da39-42df-8ca9-0fa60d40ce56)

When Income levels are high for both Genders, the likelihood of a bike purchase is seen to be high. This could be as a result of the availability of disposable income, lifestyle or brand recognition. 

High income individuals have more disposable income allowing them to allocate funds to leisure activities. Biking is not only a form of exercise but also a leisure activity that appeals to those with an active lifestyle. High-income individuals may be more inclined to invest in activities that contribute to their well-being and enjoyment.They also place greater emphasis on brand reputation, and product quality, and the overall biking experience. They may be more willing to invest in well-known brands or specialized bikes that offer superior performance.

***Age***

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/62433673-5fc5-4061-8a45-e69a9ef094c2)

Middle age customers (31 to 54 years) have the highest likelihood of purchasing Bikes leading with a total of 383 purchases. The young age customers (below 30 years) are less likely to purchases a bike lagging with a total of 39 purchases. 

This can be explained using income and financial stability, and purchase behaviors. Middle-aged customers often have higher income levels and greater financial stability compared to younger customers who might still be in the early stages of their careers. The ability to afford purchases, such as bikes, is often tied to financial standing. Also, Younger individuals, particularly those in their early career stages, may have demanding work schedules and time commitments that limit their engagement in recreational activities. Middle-aged individuals, who may have achieved a more stable work-life balance, could have more time for hobbies like biking.

***Commute Distance***

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/8c41f24c-c6bd-45c3-8567-22af0795be87)

Customers who have a shorter commute distance (0 to 1 Miles) have a high likelihood of purchasing a bike. They lead with 200 Bike purchases. 

Practically biking is seen as a convenient, and eco friendly mode of transportation for short distances. Customers with commutes that are 0 to 1 Mile away may find Biking to be convenient and efficient way to travel. 

**3. What types of occupations are more likely to result in bike purchases?**

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/abfcce4f-09ba-4258-951e-e0fcac6f3a3e)

Professional Occupations are more likely to to result in bike purchases (150 purchases) followed by skilled manual occupations (115 Bike purchases). 

This can be explained by using either lifestyle or the health and fitness conciousness. For example Professionals often work in urban settings where biking infrastructure is more developed. Urban environments with bike lanes, bike-sharing programs, and a general emphasis on sustainable transportation can encourage professionals to choose biking for commuting. Also, Professionals may place a higher emphasis on health and fitness as part of their lifestyle. Biking offers an opportunity for physical exercise, and professionals may be more inclined to integrate such activities into their daily routines.

**4. Is there a correlation between education levels, and bike purchases?**

![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/0908e621-133a-4823-9a97-521716a89a6e)

Customers with a Bachelors have the highest likelihood of purchasing a bike (169 Bike Purchases) followed by partial college customers (119 Bike Purchases). 

This can be explained in the context of disposable income and health and wellness conciousness. For example customers with higher educational attainment, such as those with a Bachelor's degree, may have greater economic capacity. They may be more financially stable and have disposable income to allocate to non-essential purchases, including recreational items like bikes.

****Recommendations****

1. The Bike company should implement targeted marketing campaigns tailored to the preferences and needs of these segments, such as professionals, individuals with higher education levels, and those with shorter    commute distances. Develop promotional strategies that highlight the benefits of biking aligned with the identified preferences. Highlight how biking contributes to an active and healthy lifestyle, promotes     environmental sustainability, and offers a convenient and enjoyable mode of transportation. Develop content that resonates with the values and priorities of the identified customer segments to create a          compelling narrative around bike ownership.

2. Acknowledge the economic considerations of customers with varying income levels. Implement flexible financing options, installment plans, or special promotions to make bikes more accessible to a broader        range of customers. Communicate these financing options prominently in marketing materials to address affordability concerns and encourage purchasing decisions.

3. There is need for more data also which should include the Dates for the sales to be able to derive insights on the performnce of sales through a period span. This would be good for the sales team to identify    which days, months, or year had the best impact on sales and why or the ones with least sales and why. Gaining this information is useful to the team to identify potential areas that need growth and how         they can strategize to improve on sales during those times. 

4. *Also feedback from the customers would be much needed. This would allow the sales team to understand why customers from different segmentations prefer their Bikes. Getting this information would cut off         making assumptions as to why customers prefer their Bikes. Giving out questionnaires or asking the customer directly when they make a purchase would allow the sales team to get the reasons for better            planning.*

****Conclusion****

Working on this project has helped build my problem solving and critical thinking skills. Being able to work with data all through from knowing the expectations of the stakeholders to giving recommendations has been one great experience which has build my confidence on working with data. 

*I have been able to ask the right questions to understand the objectives, clean and transform the data to ensure integrity, analyze it to draw insights, share the derived insights that match with the expectations of the stakeholders and give recommendations.* 




























   


