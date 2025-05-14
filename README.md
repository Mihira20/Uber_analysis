🚗 Uber Analysis – Data Engineering Project
Hi! This is a data engineering project where I built an end-to-end pipeline to analyze Uber trip data. The goal was to design a scalable and cloud-native workflow that extracts, transforms, and visualizes data to generate insights around ride patterns, demand, and trip performance.

🧰 Tools & Technologies Used:
Google Cloud Storage (GCS) – for storing raw data files
Mage – open-source ETL tool for building and managing pipelines
Google Compute Engine – runs the Mage VM
BigQuery – used as the data warehouse for analytics
Looker – for creating interactive dashboards and reports

🔁 Project Workflow
Here’s a high-level overview of the pipeline:
nginx
Copy
Edit
Google Cloud Storage → Mage (on Compute Engine) → BigQuery → Looker
1. Data Storage
I stored the raw Uber trip data in a Google Cloud Storage bucket.
2. ETL with Mage
Using Mage deployed on a Compute Engine VM, I built a pipeline to:
Ingest and clean the data
Parse timestamps, filter out bad records
Aggregate metrics like total trips, trip duration, and fare
Format the data for loading into BigQuery

3. Analytics with BigQuery
After transformation, I loaded the data into BigQuery. Tables are partitioned and optimized for analytical queries.

4. Data Visualization with Looker
Finally, I connected Looker to BigQuery to build dashboards showing:
Peak trip hours
Trip distribution by zone
Fare trends and ride durations over time

🔍 Insights I Uncovered
Busiest hours and days for Uber rides
Average trip distances and durations
How fare prices change with time and location

🚀 How to Use or Reproduce
Upload your Uber data to a GCS bucket
Run the Mage pipeline from the Compute Engine VM
Transformed data will be loaded into BigQuery
Connect Looker to visualize the insights
