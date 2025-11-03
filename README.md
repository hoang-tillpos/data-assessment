# Cloud Insights System for Multi-Franchise Pizza Sales

## Overview

We are designing a **Cloud Insights System** for a multi-franchise business that sells pizzas through the following channels:

- **External Onsite POS** with an SQL database hosted on an onsite server  
  - A data feed agent can be built with the onsite server to pull data from the SQL database.
- **External Online Ordering** with webhook notifications triggered from the onsite server  
  - Includes shift totalling APIs from cloud endpoints.
- **External Corporate Catering Management System** with an SQL database  
  - Bulk data exports are generated from the onsite server.
  - A data feed agent can be built with the onsite server to pull data from the SQL database.

The software, data upload agents, and schemas are identical across all 1,000 physical sites.

As a data engineer, you will design the data ingestion technology, schemas, pipelines, environment setup, and testing.

**Note** it is common to start the design with a number of API endpoints as the entry point for data ingestion. Revise the data schema

**Bonus:** Ability to design and refine queries for business needs.

---

## Data Files

### `online-feed.json`
Contains raw transaction or order data from online ordering channels.  
Includes:
- Order IDs  
- Timestamps  
- Item details  
- Customer data  
- Real-time webhook feed information  

### `online-sale-summary.json`
A summarized or aggregated version of `online-feed.json`.  
May include:
- Daily or shift-based sales totals  
- Average order value  
- Performance metrics for online transactions  

### `pizza-sales-catering-export.csv`
Represents bulk exported data from the corporate catering management system.  
Contains:
- Event IDs  
- Customer names  
- Dates  
- Ordered items and quantities  
- Total revenue  

### POS (Point-of-Sale) SQL Data
**Directory:** `pos-sql/`  
Contains structured CSV files representing different database tables for the onsite POS system.


---

## Timeline

- **15 minutes:** Analyze data, set up environment, and prepare questions for the assessment.  
- **45 minutes:** Onsite technical exercise.  
- **60 minutes:** Technical assessment and general interview questions.

---

## Tasks (In Order of Importance)

1. **Data Setup**  
   - Set up a test SQL database.  
   - Create test endpoints for data ingestion and validation.

2. **Data Pipelines**  
   - Use any tool of choice (e.g., SQL, dbt, pandas, MapReduce) to transform data to meet business requirements.

3. **Data Warehouse**  
   - Design interim schemas for business applications and the data warehouse.

---

## Web-App Dashboard Requirements

The data warehouse will power a web dashboard offering insights for franchise businesses.

### Consumer Behaviour
- Determine when customers place the most orders by merchant segment and time of day.

### Labour Preparation
- Predict restaurant busyness levels based on historical and real-time order data.

### Operations
- Reconcile orders across systems and shifts to detect cross-system or human errors.

### Revenue Analysis
- Identify high-value and repeat customers.  
- Highlight products generating the most revenue.

### Risk Management
- Verify accurate handling of allergy information, especially in catering.  
- Enable live notifications for failed allergy checks.

### Business Planning
- Analyze cumulative revenue trends by product type, time of day, and week of year.

### `sample-queries.txt`
Demonstrates example SQL queries or analytical questions for integrated data, such as:
- Customer behavior trends  
- Sales summaries  
- Product revenue analysis  

---

