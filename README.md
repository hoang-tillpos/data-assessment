We a design cloud insights system for multifranchise to sell their pizzas in the following channels:
- external onsite POS with an SQL DB  from onsite server
  - data feed agent can be built with onsite server to pull the data from SQL DB   
- external online ordering with webhook notifications triggered from onsite server, and shift totalling APIs from their cloud endpoints
- external coprporate catering management system with SQL DB, and bulk data exports generated from onsite server
  - data feed agent can be built with onsite server to pull the data from SQL DB  
 
The software and schemas are all the same, but they are all installed in 1000 physical sites.

As a data engineer, you will design the data ingestion including, schemas, pipelines, environment setup and  testing.

Bonus points: ability to design and refine queries for business needs. 

We are looking for a data engineer to build a data warehouse and build the following dashboard for the business:

- Consumer behaviour: what time of day for each merchant segment where the orders mostly be made?
- Labour preparation: how busy would each merchant restaurant be at certain point in time?
- Operations: Reconcile the orders with the previous day/shifts to alert of any cross-system or human errors.
- Revenue: who are the high value customers, and who are the highly repeated customers?
- Revenue: what are the products which generate the most revenues?
- Risk management: could we ensure allergies are not incorrectly considerred, especially for catering? perhaps through live notification of failed allergies
- Business planning: analyse cumulated revenue trends by product types, time of day, week of year?

Timeline:
- 15 minutes: Analyse the data and set up environment and questions on the assessment
- 45 minutes: onsite technical excercise.
- 60 minutes: technical assessment  and general interiew questions


Tasks in order of importance:
- Data setup: set up a test SQL DB, test endpoints for data ingestion and testing
- Data pipelines: use ANY tool of choice like SQL/dbt/pandas/mapreduce to transform the data to meet the business needs
- Data Warehouse: design interim schemas for business applications and data warehouse
