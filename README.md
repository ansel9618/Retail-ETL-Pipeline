# Retail-ETL-Pipeline

![Architecture](https://github.com/ansel9618/Retail-ETL-Pipeline/blob/main/images/Architecture.png)

* We'll create a airflow dag to load the csv file to google cloud storage efficienty
* Then we'll have data quality checks using SODA to make sure that the raw data is good and is in 
  proper format
* Once the checks are done we'll have another task to shape the raw data so that we obtain the Fact 
  and dimension tables using DBT & airflow
* To integrate DBT and airflow we'll be using cosmos --> link-https://www.astronomer.io/cosmos/
  so with cosmos we dont need to run dbt in bash operator using cosmos dbt model becomes tasks in 
  datapipeline
* After we get the fact and dimensiontable we run the dataquality checks again to make sure the data 
  transformations are correct
* Then we run another dbt model/task to get analytics from the transformed data using dbt
* Finally we run a data quality check again to make sure that the analytics are correct amd 
  build a dashboard in order to get insights from the data

### Airflow Dag execution

![Architecture](https://github.com/ansel9618/Retail-ETL-Pipeline/blob/main/images/31.0_.png)

### Metabase Dashboard

![Architecture](https://github.com/ansel9618/Retail-ETL-Pipeline/blob/main/images/38.0_.png)


 
