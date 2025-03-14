# OpenAlex upload to BigQuery

## Code to upload OpenAlex dump and split it into tables

The code is divided into two files.

Upload - [Bash commands to upload](https://github.com/insyspo/openalex/blob/main/bash_commands_to_download_and_upload.ipynb)

Model - [BigQuery code for relational model](https://github.com/insyspo/openalex/blob/main/OpenAlex_create_tables_2024_04.ipynb)

## Diagrams for tables

- [General](https://github.com/insyspo/openalex/blob/main/openalex.png)
- [Authors](https://github.com/insyspo/openalex/blob/main/authors.png)
- [Concepts](https://github.com/insyspo/openalex/blob/main/concepts.png)
- [Topics](https://github.com/insyspo/openalex/blob/main/topics.png)
- [Works](https://github.com/insyspo/openalex/blob/main/works.png)
- [Institutions](https://github.com/insyspo/openalex/blob/main/institutions.png)
- [Fields](https://github.com/insyspo/openalex/blob/main/fields.png)
- [Subfields](https://github.com/insyspo/openalex/blob/main/subfields.png)
- [Domains](https://github.com/insyspo/openalex/blob/main/domains.png)
- [Sources](https://github.com/insyspo/openalex/blob/main/sources.png)
- [Publishers](https://github.com/insyspo/openalex/blob/main/publishers.png)

## Steps

The steps are as follows.
- First file (Upload):
  - Using a Google VM we download the most recent dump. [OpenAlex dump](https://docs.openalex.org/download-all-data/openalex-snapshot).
  - The dump is uploaded as tables. One for each of the main entities [Entities](https://docs.openalex.org/api-entities/entities-overview).
  - The tables have just one column as a JSON entry are uploaded to BigQuery using a project already set up. [How to create projects](https://cloud.google.com/resource-manager/docs/creating-managing-projects).
- Second file (Model):
  - Everything is run over Google Colaboratory taking advatage of the internal authorisation mechanism. Also, the queries are organised in sequence. [Integrating Colab and BigQuery](https://colab.research.google.com/notebooks/bigquery.ipynb). 
  - All the tables are split into fields creating columns for the values.
  - New tables are created to connect the main ones.
  - New tables are created to explode the array of data inside the values in the tables.
