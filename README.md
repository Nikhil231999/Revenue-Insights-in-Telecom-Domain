# Revenue-Insights-in-Telecom-Domain

## Problem statement

AtliQo is one of the leading telecom providers in India and launched its 5G plans in May 2022 along with other telecom providers.
However, the management noticed a decline in their active users and revenue growth post 5G launch in May 2022. AtliQo’s business director requested their analytics team to provide a comparison report of KPIs between pre and post-periods of the 5G launch. The management is keen to compare the performance between these periods and get insights that would enable them to make informed decisions to recover their active user rate and other key metrics. They also wonder if they can optimize their internet plans to get more active users. 

[Live Dashboard Link](https://www.novypro.com/project/nikhil-rane--3)

## Tech Stack Used 

- SQL
- PowerBi Desktop
- Excel
- DAX language

## Insights
- Average Revenue decreased by 0.14 Cr post-5G launch 
- Average Revenue % is negative for Kolkata, Chandigarh, Hyderabad, Ahmedabad, Chennai, Delhi
- Average Revenue in the month of march was 27.36 Cr in the month of august it increased to 27.94 Cr
- Active Users decreased by 1.16 Lakhs post-5G launch 
- Active Users are increased only in Chennai and Lucknow 
- Unsubscribe Users are increased by 13.24 Lakhs Post-5G launch 
- Unsubscribe Users are decreased only in Mumbai for the rest of the cities it's increased and maximum for Lucknow 
- Average Revenue Per User increased by 21.02
- Average Revenue Per User decreased for Chennai and Kolkata for the rest of the cities ARPU increased
- Smart Recharge Pack (2GB / Day Combo For 3 months) generated maximum revenue which is 419.93 Cr - 
- Ms % is lower for Hyderabad and Delhi maximum for Gurgaon 
- in the month of June Ms % is the lowest of all i.e :- 18.7%

## Dataset 

1. dim_cities
2. dim_date
3. dim_plan
4. fact_atliqo_metrics
5. fact_market_share
6. fact_plan_revenue

### ***Column Description for dim_cities:***
1. city_code: This column represents the unique code given for each city.
2. city_name: This column represents the name of the city corresponding to the city code.

### ***Column Description for dim_date:***
1. date: This column represents the starting date of each month. 
2. month_name: This column represents the month names in abbreviated form(Example: Jan, Feb, Mar, etc). We have months starting from January to September except for May.
3. before/after_5g: This column represents the unique category based on the month. We have 2 categories, Before 5G and After 5G. January to April comes represents the period before 5G implementation and June to September represents periods after 5G implementation.
4. time_period: This column represents the unique sequence number ranging from 1 to 4. These time Periods are used to make respective months comparisons before and after 5G implementation (Example: Jan vs Jun, Feb vs Jul, Mar vs Aug and Apr vs Sep)

### ***Column Description for dim_plan:***
1. plan: This column represents the various internet plans provided by the Atliqo company to the users. 
2. plan_description: This column represents the brief description about the internet plan.

### ***Column Description for fact_atliqo_metrics:***
1. date: This column represents the starting date of each month.
2. city_code: This column represents the unique pincode code given for each city.
3. company: This column represents the company name for which the data is provided. In this dataset it's only Atliqo. 
4. atliqo_revenue_crores: This column represents the revenue that Atliqo got on that particular month in that city_code in crores(unit of currency in India - 1Crore = 10 Million) from the internet users. 
5. arpu: This column represents the average revenue per user. That means on average how much revenue Atliqo generated on single user for a given time period.
6. active_users_lakhs: This column represents the number of active users who are using Atliqo's service on that particular month in that city_code in lakhs(unit of currency in India - 1 Lakh = 100,000).
7. unsubscribed_users_lakhs: This column represents the number of unsubscribed users who unsubscribed from Atliqo on that particular month in that city_code in lakhs(unit of currency in India - 1 Lakh = 100,000). 


### ***Column Description for fact_market_share:***
1. date: This column represents the starting date of each month.
2. city_code: This column represents the unique code given for each city.
3. tmv_city_crores: This column represents the total market value of the city in that month in crores(unit of currency in India) from the internet users. 
4. company: This column represents the different competitor names in the telecom industry [Atliqo, Britel, DADAFONE, PIO, Others].
5. ms_pct: This column represents the percentage of market share gained by respective company from the total market value(tmv_city) on that particular month in that city-code. 


### ***Column Description for fact_plan_revenue:***
1. date: This column represents the starting date of each month.
2. city_code: This column represents the unique code given for each city.
3. plans: This column represents the various internet plans provided by the Atliqo company to the users.
4. plan_revenue_crores: This column represents the revenue that Atliqo got from that respective plan on that particular month in that city_code in crores (unit of currency in India - 1Crore = 10 Million).




































 
