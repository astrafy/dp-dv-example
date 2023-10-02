# dp-dv-example

This repository contains the [worked example](https://automate-dv.readthedocs.io/en/latest/worked_example/) from automate_dv
package. 

Data Vault 2.0 is a complex data modelling tehcnique and this repository contains imple data in order to grasp at best the
different concepts of data vault 2.0

We have created different scenarios README files in order to explain each concept with concrete examples

## Use cases

- Initial Load
- Delta load with no historic data
- Delta load with historic data
- ....

## Landing Zone structure

Use following funciton to generate fake data:

https://github.com/unytics/bigfunctions/blob/main/bigfunctions/faker.yaml


## Ingestion partitioned table

https://cloud.google.com/bigquery/docs/partitioned-tables#ingestion_time

new dummy data to be in new date partitions.

Two use cases:
- partition expiration of one day. This would handle the use case where we ingest
new data every day and we don't keep history in landing zone

- no partition expiration (keep full history in landing zone). In that case, need intermediate
staging tables to get only latest data from landing zone.


## Airflow and backfilling