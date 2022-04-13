
# Amazon Vine Analysis
Using the cloud environment to extract Amazon S3 data that was then transformed in Google Colaboratory with PySpark, loaded into Postgres tables, exported as a CSV and imported into a Jupyter notebook to assess the potential bias of paying for reviews

![Am](https://user-images.githubusercontent.com/30667001/163226418-bf30f21e-cf74-4b1d-85f8-c64a44fa8d24.png)

## Resources
- Data Source: Amazon Review S3 Dataset - US Pet Products v1_00.tsv.gz
- Libraries: PySpark, Pandas, NumPy
- Software: Google Colaboratry, AWS RDS and S3 storage, PostgreSQL Version 11, pgAdmin4, Python 3.7.6, Jupyter Notebook 6.4.5

## Project Overview
Big Market’s client $ellby is poised to launch a catalogue with new products. $ellby wants to know if investing in paid Amazon Vine product reviewers will increase the percentage of positive product evaluations The following steps were taken to assist $ellBy in making a determination:
* Employing Google’s Colaboratory and data stored in AWS S3 buckets to perform ETL processes in a cloud environment.
* From the 50 datasets available, focusing on pet product reviews specifically.
* Extracting data from S3 into a PySpark dataframe and transforming the data into four tables (customer, review, ID, vine).
* Connecting to the Postgres database with PySpark, and loading the transformed data into the pgAdmin tables; queries were run to confirm the data loaded correctly.
* Exporting the vine_table from pgAdmin a CSV file; the data were imported into a Jupyter Notebook. Pandas was used to perform the analysis.
* Determing 5-star reviews to be a fair proxy for the potential bias that may exist with paid reviews.

## Results
![AmazonRevs_Pets](https://user-images.githubusercontent.com/30667001/163252383-fabac151-d9b0-4cfb-9bb8-ac90a75b3bca.png)

* A total count of 38,010 pet products were reviewed.
* Five-star reviews accounted for 54% of total reviews (20,677 in number).
* The overwhelming number of 5-star reviews (20,612) were provided by unpaid reviewers (99.7%), compared to a limited 65 5-star reviews from paid Amazon Vine reviewers (0.3%).

## Summary
The number of positive reviews was almost exclusively from unpaid reviewers. At first glance, it would appear that there is a bias against paying for reviews and $ellBy should feel confident that their launch can proceed without an early introduction of the products to paid reviewers.

This determination, however, may not be correct. A significant difference between individuals who are and are not paid for their reviews may exist that is unclear from basic calculations. Before responding to $ellBy’s inquiries, further analyses should be performed. Potential avenues include:
* Separating data by pet (e.g., dog, cat, bird, fish) and product (e.g., food, toy, health, furniture) type.
* Analyzing additional datasets in case pet products aren’t as generalizable to $ellBy’s product offerings.
* Performing more complex calculations that account for the imbalance between paid and unpaid reviewers. </br>

These additional details should help $ellBy decide if paid reviews will aid in increasing product sales.
