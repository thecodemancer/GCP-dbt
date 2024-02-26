# GCP-dbt

## 1. Introduction

In this quickstart guide, you'll learn how to use dbt Cloud with BigQuery. It will show you how to:

- Create a Google Cloud Platform (GCP) project.
- Access sample data in a public dataset.
- Connect dbt Cloud to BigQuery.
- Take a sample query and turn it into a model in your dbt project. A model in dbt is a select statement.
- Add tests to your models.
- Document your models.
- Schedule a job to run.

### Prerequisites​

- You have a dbt Cloud account.
- You have a Google account.
- You can use a personal or work account to set up BigQuery through Google Cloud Platform (GCP).

## 2. Create a new GCP project​​

1. Go to the <a href="https://console.cloud.google.com/bigquery">BigQuery Console</a> after you log in to your Google account. If you have multiple Google accounts, make sure you’re using the correct one.
2. Create a new project from the <a href="https://console.cloud.google.com/projectcreate?previousPage=%2Fcloud-resource-manager%3Fwalkthrough_id%3Dresource-manager--create-project%26project%3D%26folder%3D%26organizationId%3D%23step_index%3D1&walkthrough_id=resource-manager--create-project">Manage resources</a> page. For more information, refer to Creating a project in the Google Cloud docs. GCP automatically populates the Project name field for you. You can change it to be more descriptive for your use. For example, ```dbt Learn - BigQuery Setup```.

## 3. Create BigQuery datasets​

From the <a href="https://console.cloud.google.com/bigquery">BigQuery Console</a>, click **Editor**. Make sure to select your newly created project, which is available at the top of the page.

Verify that you can run SQL queries. Copy and paste these queries into the Query Editor:

```
select * from `dbt-tutorial.jaffle_shop.customers`;
select * from `dbt-tutorial.jaffle_shop.orders`;
select * from `dbt-tutorial.stripe.payment`;
```

Click **Run**, then check for results from the queries. For example:

Bigquery Query Results
Bigquery Query Results
Create new datasets from the BigQuery Console. For more information, refer to Create datasets in the Google Cloud docs. Datasets in BigQuery are equivalent to schemas in a traditional database. On the Create dataset page:

Dataset ID — Enter a name that fits the purpose. This name is used like schema in fully qualified references to your database objects such as database.schema.table. As an example for this guide, create one for jaffle_shop and another one for stripe afterward.
Data location — Leave it blank (the default). It determines the GCP location of where your data is stored. The current default location is the US multi-region. All tables within this dataset will share this location.
Enable table expiration — Leave it unselected (the default). The default for the billing table expiration is 60 days. Because billing isn’t enabled for this project, GCP defaults to deprecating tables.
Google-managed encryption key — This option is available under Advanced options. Allow Google to manage encryption (the default).
Bigquery Create Dataset ID
Bigquery Create Dataset ID
After you create the jaffle_shop dataset, create one for stripe with all the same values except for Dataset ID.

## 4. Generate BigQuery credentials​

5. Connect dbt Cloud to BigQuery​​
6. Set up a dbt Cloud managed repository​
7. Initialize your dbt project​ and start developing​
8. Build your first model​
9. Change the way your model is materialized​
10. Delete the example models​
11. Build models on top of other models​
12. Add tests to your models​
13. Document your models​
14. Commit your changes​
15. Deploy dbt​

<img src="images/GCP_dbt_1.png" />
