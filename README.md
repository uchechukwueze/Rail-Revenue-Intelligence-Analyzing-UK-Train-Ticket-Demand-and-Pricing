
<img width="2502" height="1059" alt="image16" src="https://github.com/user-attachments/assets/1cf51ee5-f812-4c7e-b8f8-690308806fa7" />

# Rail Revenue Intelligence: Analyzing UK Train Ticket Demand and Pricing
This project analyzes mock UK National Rail ticket data from January to April 2024 to uncover patterns in train ticket demand, pricing behavior, route performance, payment methods, delays, cancellations, and peak travel activity.

## Project Overview

This project analyzes mock UK National Rail ticket data from **January to April 2024** to uncover patterns in train ticket demand, pricing behavior, route performance, payment methods, delays, cancellations, and peak travel activity.

The goal of this project is to help train operators better understand how passengers travel, what ticket types they prefer, which stations and routes drive the most activity, and where operational improvements can be made to improve revenue, scheduling, and customer experience.

---

## Business Problem

UK train operators handle thousands of passenger journeys daily. However, without clear insight into ticket demand, pricing behavior, route performance, payment methods, and delay patterns, it becomes difficult to make effective operational and commercial decisions.

This project seeks to answer key business questions such as:

* Which stations generate the highest passenger activity?
* What ticket types are most preferred by passengers?
* How does ticket price vary by ticket class, ticket type, and time of day?
* Which routes are the most popular?
* When are train rides most in demand?
* What are the major causes of delays and cancellations?
* How can train operators improve scheduling, pricing, and service reliability?

---

## Dataset Description

The dataset contains mock train ticket records for National Rail journeys in the UK between **January and April 2024**.

The dataset includes information such as:

* Ticket type
* Ticket class
* Ticket price
* Payment method
* Departure station
* Arrival destination
* Departure time
* Arrival time
* Journey status
* Reason for delay
* Purchase time and date

---

## Tools Used

The project was completed using Python and key data analytics libraries:

* **Python** — core analysis
* **Pandas** — data cleaning and manipulation
* **NumPy** — numerical computation
* **Matplotlib** — visualization
* **Seaborn** — statistical visualization
* **Jupyter Notebook** — analysis documentation

---

## Data Cleaning and Preparation

Before analysis, the dataset required cleaning and preparation to ensure reliable insights.

Key cleaning steps included:

* Converted date and time columns into proper datetime format
* Created new features such as `Hour_of_day`, `Day_of_week`, and `Route`
* Cleaned and standardized relevant categorical columns
* Filled missing delay reasons with `"No reason stated"`
* Checked ticket price distribution and travel patterns
* Prepared the dataset for univariate, bivariate, and time-based analysis

A major data quality issue observed was the large number of missing values in the delay reason column. These were recorded as missing/null values and later filled as `"No reason stated"` to preserve the records while still highlighting the limitation.

---

## Key Findings

### 1. Ticket Price Distribution

Train ticket prices are **right-skewed**, with most ticket prices concentrated between **0 and 50** per ride. This suggests that most passengers purchase relatively affordable tickets, while a smaller number of high-priced tickets increase the overall spread.
<img width="2345" height="1267" alt="image4" src="https://github.com/user-attachments/assets/03cf18e7-8ec6-4199-bb07-4529da4077b3" />

---

### 2. Station Performance

**Manchester Piccadilly** recorded the highest number of train trips, followed by **London Euston**. The least active station was **Bristol Temple Meads**, indicating lower passenger movement compared to the top-performing stations.
<img width="2480" height="1084" alt="image5" src="https://github.com/user-attachments/assets/802fb5c2-2cd5-46c3-9a90-e56ea83586c4" />

---

### 3. Payment Method Preference

Over **61% of payments** were made through **credit card**, making it the dominant payment method. Contactless payment also recorded strong usage, showing that passengers prefer fast and digital payment options.
![Uploading image7.png…]()
<img width="687" height="629" alt="image6" src="https://github.com/user-attachments/assets/e8256a9e-e3ca-484b-b89b-3d37d24f37a5" />

---

### 4. Ticket Type Demand

**Advance tickets** were the most demanded ticket type, followed by **Off-Peak** tickets. **Anytime tickets** recorded the lowest demand, suggesting that many passengers are price-sensitive and prefer cheaper planned travel options over flexible but expensive tickets.
<img width="2637" height="1309" alt="image8" src="https://github.com/user-attachments/assets/10bc73a7-54b3-44a5-bc0a-77a8bee0b0a9" />

---

### 5. Delay and Cancellation Performance

Most train rides arrived on time, which is a positive sign for operational performance. Only about **7.2% of trips were delayed**, while around **6% were cancelled**.

However, after accounting for missing delay reasons, **weather** and **signal failure** appeared as major contributors to delays. This suggests that operators need stronger disruption monitoring, better signal maintenance, and improved reporting of delay causes.
<img width="2201" height="933" alt="image9" src="https://github.com/user-attachments/assets/dd6c534d-3c06-4745-8d67-45ad001cc03c" />

---

### 6. Most Popular Routes

The most popular route was:

**Manchester Piccadilly → Liverpool Lime Street**

The second most popular route was:

**London Euston → Birmingham New Street**

These high-demand routes should be prioritized for capacity planning, service reliability, and customer experience improvements.
<img width="2681" height="1240" alt="image10" src="https://github.com/user-attachments/assets/c67a70fe-da89-4c6c-a351-d4cdb2e1b8b4" />

---

### 7. Peak Travel Times

Trip demand is strongly concentrated around two major commute periods: **morning rush hour** and **evening rush hour**.

The highest demand occurs around:

* **6 AM** with over 3,100 trips
* **6 PM** with over 3,100 trips

Demand remains high between **6 AM and 8 AM**, drops after 9 AM, and rises again from **4 PM to 6 PM**. This shows that train activity is strongly driven by work and commuter travel patterns.
<img width="1386" height="1059" alt="image12" src="https://github.com/user-attachments/assets/2d526fd1-c097-479b-a477-0d5daa53cbbe" />
<img width="1415" height="1059" alt="image11" src="https://github.com/user-attachments/assets/32490580-7d53-4a7c-8406-0cf9abe3a376" />


---

### 8. Ticket Class and Ticket Type Pricing

First Class tickets are consistently more expensive than Standard tickets across all ticket types.

**Anytime tickets** have the highest average price in both classes, showing that ticket flexibility comes at a premium. **Advance tickets** are the cheapest option, confirming the cost advantage of early booking.

Overall, ticket price is strongly influenced by both **ticket class** and **ticket type**, with **First Class Anytime** being the most expensive and **Standard Advance** being the cheapest.
<img width="1834" height="429" alt="image13" src="https://github.com/user-attachments/assets/f41a08ec-4a0d-4f70-b3bf-1a86631966ae" />
<img width="2142" height="880" alt="image14" src="https://github.com/user-attachments/assets/80eeed34-13f3-40d9-98ad-0991baf5b30b" />

---

### 9. Price Variation by Time of Day

Average ticket prices vary noticeably across the day. The strongest price spike occurs around **8 AM**, where the average ticket price rises to about **£62**.

This suggests that morning rush-hour travel attracts higher fares, possibly due to stronger demand, more Anytime ticket purchases, or a higher share of First Class travel.

Prices are relatively moderate across most other hours, while lower average prices appear during off-peak periods such as **10 AM** and **9 PM**.
<img width="2376" height="1173" alt="image15" src="https://github.com/user-attachments/assets/75ffc53c-a61b-4dd8-b174-8c7350ea54fd" />
<img width="2502" height="1059" alt="image16" src="https://github.com/user-attachments/assets/66eb49a1-440a-4837-8e20-422ee91ec42c" />

---

## Business Recommendations

### 1. Improve Peak-Hour Capacity and Scheduling

Since trip demand peaks strongly around **6 AM and 6 PM**, train operators should increase train availability, carriage capacity, and station support during these periods.

High-demand routes such as **Manchester Piccadilly to Liverpool Lime Street** and **London Euston to Birmingham New Street** should receive closer scheduling attention to reduce congestion and improve passenger flow.

---

### 2. Strengthen Delay Prevention and Service Reliability

Although most trips arrive on time, delays and cancellations still affect customer experience. Since weather and signal failures are major delay drivers, operators should invest in:

* Better signal maintenance
* Real-time disruption monitoring
* Weather-related contingency planning
* Clearer delay reporting systems

The large number of `"No reason stated"` delay records should also be reduced so operators can better understand and address the real causes of disruption.

---

### 3. Optimize Pricing and Ticket Strategy

Advance tickets are highly demanded, showing that passengers value cheaper early-booking options. Operators should continue promoting Advance fares while using smarter peak/off-peak pricing to balance revenue and affordability.

Since prices peak around **8 AM**, operators should monitor morning rush-hour pricing carefully to avoid discouraging passengers while still protecting revenue. First Class and Anytime tickets can remain premium products, but pricing should be reviewed regularly to ensure it reflects demand, flexibility, and customer willingness to pay.

---

## Conclusion

This project shows how train ticket data can provide valuable business intelligence for rail operators.

The analysis revealed that UK train rides are generally performing well, with most trips arriving on time. However, it also uncovered important opportunities around peak-hour scheduling, delay prevention, route planning, and pricing strategy.

By using data to understand when passengers travel, what tickets they buy, which routes are busiest, and what causes disruptions, rail operators can make better decisions that improve both revenue performance and passenger experience.

---
## Author

**Uchechukwu Eze**
Data Analyst | Data Scientist
GitHub: `uchechukwueze`
