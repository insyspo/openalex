# OpenAlex upload to BigQuery

Code to upload OpenAlex dump and split it into tables.

The code is divided into two files.
[Bash commands to upload](https://github.com/insyspo/openalex/blob/main/bash_commands_to_download_and_upload.ipynb)
[BigQuery code for relational model](https://github.com/insyspo/openalex/blob/main/OpenAlex_create_tables_2024_02.ipynb)


The steps are as follows.
- Using a Google VM we download the most recent dump.
- The dump is uploads as tables. One for each of the main entities.
- The table have just one column as a JSON entry.
