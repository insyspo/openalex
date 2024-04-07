# OpenAlex upload to BigQuery

Code to upload OpenAlex dump and split it into tables.

The code is divided into two files.


The steps are as follows.
- Using a Google VM we download the most recent dump.
- The dump is uploads as tables. One for each of the main entities.
- The table have just one column as a JSON entry.
