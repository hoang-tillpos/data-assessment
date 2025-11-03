We a design cloud insights system for multifranchise to sell their pizzas in the following channels:
- external onsite POS with an SQL DB  from onsite server
  - data feed agent can be built with onsite server to pull the data from SQL DB   
- external online ordering with webhook notifications triggered from onsite server, and shift totalling APIs from their cloud endpoints
- external coprporate catering management system with SQL DB, and bulk data exports generated from onsite server
  - data feed agent can be built with onsite server to pull the data from SQL DB  
 
sample-querries.txt
Demonstrates example SQL queries or analytical questions to be answered using the integrated data—such as customer behavior trends, sales summaries, or product revenue analysis.

Data Files
online-feed.json
Contains raw transaction or order data from online ordering channels. Typically includes order IDs, timestamps, item details, and customer data from real-time webhook feeds.

online-sale-summary.json
A summarized or aggregated version of online-feed.json. It may include daily or shift-based sales totals, average order values, and performance metrics for online transactions.

pizza-sales-catering-export.csv
Represents bulk exported data from the corporate catering management system. The CSV could include catering order details such as event IDs, customer names, dates, ordered items, quantities, and total revenue.

POS (Point-of-Sale) SQL Data
pos-sql/
A directory containing structured CSV files representing different database tables for the onsite POS system.


The software, data upload agents, and schemas are all the same, but they are all physically installed in 1000 physical sites.

As a data engineer, you will design the data ingestion technology, schemas, pipelines, environment setup and  testing.

Bonus points: ability to design and refine queries for business needs. 

Timeline:
- 15 minutes: Analyse the data and set up environment and questions on the assessment
- 45 minutes: onsite technical excercise.
- 60 minutes: technical assessment  and general interiew questions


Tasks in order of importance:
- Data setup: set up a test SQL DB, test endpoints for data ingestion and testing
- Data pipelines: use ANY tool of choice like SQL/dbt/pandas/mapreduce to transform the data to meet the business needs
- Data Warehouse: design interim schemas for business applications and data warehouse


We are looking for a data engineer to build a data warehouse and build the following web-app dashboard for the businesses:

- Consumer behaviour: what time of day for each merchant segment where the orders mostly be made?
- Labour preparation: how busy would each merchant restaurant be at certain point in time?
- Operations: Reconcile the orders with the previous day/shifts to alert of any cross-system or human errors.
- Revenue: who are the high value customers, and who are the highly repeated customers?
- Revenue: what are the products which generate the most revenues?
- Risk management: could we ensure allergies are not incorrectly considerred, especially for catering? perhaps through live notification of failed allergies
- Business planning: analyse cumulated revenue trends by product types, time of day, week of year?
