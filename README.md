# Bike-Purchases
To create the best dashboards to communicate your analysis, it is important to understand the specific needs and objectives of stakeholders. In this Project, I will dive into the phases of data analysis including:
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
8. Home owner - identifies whether the customer owns a home.
9. Cars - Identifies the number of cars the customers has.
10. Commute Distance - identifies the Distance from the bike company to the customers place of living.
11. Region - Identifies the location of the customer
12. Age - Identifies the age of the customer.
13. Purchased Bike - Identifies whether the customer bought a bike or not.

****<ins>1. ASK</ins>****

This phase of the analysis includes asking the right questions to answer the goals and objectives of your stakeholders.
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
2. Removing duplicates (Data tab --> Remove duplicates). 26 duplicate values were removed leading to remainder of 1001 rows. ![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/83bbe42f-7b95-4669-bd95-416f6c9ea9a9)
3. Checked the data contained in each column to ensure no blanks.

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

   The final table looks like this:![image](https://github.com/zilphar/Bike-Purchases/assets/116642579/1af965f9-7c60-4f49-8fb6-6e58969e3f56)

****<ins>4. ANALYZE</ins>****








   


