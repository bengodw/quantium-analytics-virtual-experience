# Quantium Data Analytics Virtual Experience

My submission for this program's tasks:
- Data preparation and customer analytics
- Experimentation and uplift testing

## Dependencies
Language: Python 3.8 \
Packages: pandas, numpy, matplotlib, datetime, scipy.

## Project Overview and Task Insights
This virtual experience program involves analysing chip purchases at supermarkets.
The aim of this project was to evaluate different customers' purchasing behaviours and the performance of trial stores with a new layout to provide insights of customer preferences to the client and a recommendation of whether the trial has been successful.

### Task 1: Data Preparation and Customer Analytics
Files: task-one.ipynb, reads QVI_purchase_behaviour.csv and QVI_transaction_data.xlsx
- Data cleaning: changed the date from integer format to datetime data type, removed irrelevant product types, outliers and duplicates. Identified missing values.
- Created new features such as product brand, size
- Analysed purchase behaviours of different customers, grouped by:
  - LIFESTAGE: customer attribute that identifies whether a customer has a family or not and what point in life they are at
  - MEMBER_TYPE: customer segmentation used to differentiate shoppers by the price point of products they buy and the types of products they buy. It is used to identify whether customers may spend more for quality or brand or whether they will purchase the cheapest options.
- A deeper dive into the Mainstream Young Singles/Couples segment to determine their preferences (chip brand and packet size) over other segments

Insights:
- 3 largest contributors to sales are 1. Budget older families, 2. Mainstream young singles/couples, 3. Mainstream retirees.
- 3 largest customer bases are 1. Mainstream young singles and couples 2. Mainsteam retirees 3. Mainstream older singles and couples.
- All customers buy a little under 2 packets per transaction on average.
- Older families and young families purchase the most packets per customer (makes sense since famlilies have the most people).
- Mainstream young singles/couple are 23% more likely to purchase Tyrells chips than other segments, and 26% more likely to purchase 270g chip packets which are Twisties chips

### Task 2: Experimentation and Uplift Testing
Files: QVI_task2.ipynb, reads QVI_data.csv
- Three stores (77, 86, 88) undergo a new store layout with the trial period in Feb-Apr 2019
- Used the total sales and number of customers metric to generate a combined score to compare the trial and potential control stores with using Pearson correlations and magnitude distances
- Determined if difference in performance of those metrics of the control stores (stores with the highest score) compared to the trial store is significant using hypothesis testing

Insights:
- Control and trial store pairs are:
  - 77 and 233
  - 86 and 155
  - 88 and 237
- All trial stores have a stastistically significant increase in sales and customers (above 95% threshold) during March 2019, compared to the relevant control stores.
- For stores 86 and 77, this increase in sales continues into April. It might be worth looking into why it doesn't happen for store 88, possibly something to do with the implementation of the trial.
- Overall, it seems that the trial did contribute to a meaningful increase in sales.
