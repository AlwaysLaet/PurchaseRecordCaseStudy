# Purchase Records: Generated Data Case Study

## Introduction

We provide three tables `data/purchases.csv`, `data/customers.csv`, `data/products.csv`, which can be used to practice several topics in data wrangling, discussed below. We also provide the jupyter notebook containing the scripts for data generation, for those interested.  

## Where to Wrangle

The data tables are set up in a way where each question below can be answered, but likely needs to pull techniques from merging on specific, but differently named keys; merging on a time variable which has different granularties across tables; pivoting from wide to long format; and calculating certain marketting specific values which are useful in practice, such as recency, frequency, and total amount spent (customer by customer). 

**We will assume that "present" is Jan 1, 2020 at 0800.**

### List of questions to practice 
#### Basic Exploration

  - Which years are represented in these data?
  - How many unique customers are represented in these data?
  - How many unique products are represented in these data?
  - Which product was the most expensive during the earliest quarter represented? Which product was the most expensive during the latest quarter represented?

#### Wrangling

  - Create a new table with index `CUST_ID` and columns  `RECENCY`, `FREQUENCY`, and `TOTAL_VALUE` where each row is indexed by a unique customer id, followed by measurements of that customer's recency, frequency, and total (purchase) value over the years represented in the data.
  - Create a new table with index `CUST_ID` and columns `AVG_TIME_DELTA`, `RECENT_LAG`, and `RECENCY` where each row is indexed by a unique customer id, followed by measurements of that customers average time span between purchases (or left as a missing value if only one purchase by customer), the span between the most recent two purchases of that customer; and again, the span between "present" and the most recent purchase of the customer.

#### Actionable Insights and Discussion

In this section, there are some wrangling questions which require explicit answers. However, for each of these, please also write out your thoughts on the following: In what way might this information help the retailer act in order to potentially improve their sales, and what other information might be beneficial to collect so that the insights are likely better, more tailored, or otherwise more informative?

  - Based on recency, frequency, and total value per customer, are there any segmentations you might make within the customer base which could be useful for the retailer to observe?
  - For the retailer, order the states by activity (number of purchases). 
  - For the most active state, which postal code is most active, if any?
  - Which products are bringing in the most revenue?
  - Which products are being sold the most and least frequently?
 
## Where not to Wrangle

While we encourage using these data to play around with the time feature, the generation of data was not done with an intention to include seasonality nor trend, and therefore may not play as a great example for forcasting type explorations. This is not to say one should eschew such an exploration, but the fruit may not be plentiful in that direction.

