
**Purpose.**

A (hypothetical) music streaming startup, Sparkify, wants to better analyze their data gathered from their app. I designed and implemented this database to enable easy querying of what songs are being listened to, who is listening to them, and general information about songs and artist.

**Justification.**

I created a PostgreSQL database of user and song analytics as well as an ETL pipeline using Python to populate the database from JSON logs and metadata. The database uses a star schema which focuses on what songs are being played and by what users. Once this database is populated, queries can provide the analytics team with useful information about the listener like name, account level, gender, and listening location. Queries can also provide information about the song or artist, such as the artists location, or the duration of the song. 

**Files**

`create_tables.py` connects to the Sparkify database and drops any tables currently existing. It then creates all the necessary tables in the database. `etl.py` will walk through the directories of data and insert song and log data into their respective tables. Both of these files also reference `sql_queries.py` which includes strings of SQL code used for operations such as dropping or creating tables, inserting data, or joining tables. `etl.ipynb` is a Jupyter notebook used for developing the fundamentals of the etl pipeline implemented in `ety.py`. `test.ipynb` is a Jupyter notebook which can quickly identify that the database is inserting the correct data into the correct tables. The `data` folder includes directories of the song and user listening data in JSON format. 

**How to Run Scripts** 

In order to run these programs, first `create_tables.py` must be run to create the necessary tables for the database to use. Then, `etl.py` can be run to finish creating the database. This functionality can be verified by running the code in the `test.ipynb` notebook.
