## Crowdfunding_ETL
### Project Team 8: Jyotsna Jayaraman, Asha Kozak and Katharine Tamas

In this scenario, our team has built an ETL Pipeline. Python, Pandas and Python dictionary methods (and regular expressions to show alternative method) were used to extract, transform and then create csv files. An Entity Relationship Diagram (ERD) and table schema were formed and then the data was uploaded into a Postgres database.

**Repository Folders and Contents:**
- Resources:
  - crowdfunding.xlsx
  - contacts.xlsx
  - campaign.csv
  - category.csv
  - contacts.csv
  - subcategory.csv
- Screenshots:
  - Select_output_campaign_1.png
  - Select_output_campaign_2.png
  - Select_output_campaign_3.png
  - Select_output_category.png
  - Select_output_contacts.png
  - Select_output_subcategory.png
  - Tables_constraints_screen_shot1.png
  - Table_constraints_screen_shot2.png
  - Schema_Upload.png
- ELT_Mini_Project_JJayaraman.ipnynb
- ELT_Mini_Project_JKozak.ipnynb
- ELT_Mini_Project_JTamas.ipnynb
- ERD_crowdfunding_db_schema.png
- crowdfunding_db_schema.sql
- Select_statements.sql
- Populating_crowdfunding_db_tables.ipynb


## Table of Contents

- [About](#about)
- [Getting Started](#getting-started)
- [Installing](#installing)
- [Contributing](#contributing)

## About
### Part 1: Create DataFrames for Category, Subcategory, Campaign, and Contacts

At the beginning, we used Jupyter Notebook to import two excel files, that were transformed and manipulated to create four dataframes. These dataframes were then exported into csv files. 
*Note: For creating contact.csv file we chose Option no. 2 (regular expressions). 

**Resource Files We Used:**
  - crowdfunding.xlsx
  - contacts.xlsx

**Our Jupyter Notebook Python Scripts:**
  - ELT_Mini_Project_JKozak.ipnynb
  - ELT_Mini_Project_JTamas.ipnynb
  - ELT_Mini_Project_JJayaraman.ipnynb

**Files We Created:**
  - category.csv
  - subcategory.csv
  - contacts.csv
  - campaign.csv

**Tools/Libraries We Imported:**
   - pandas library: for data manipulation and analysis
   - numpy library: used for numerical computations
   - re library: used for regular expressions to search and manipulate strings in python


### Part 2: Create the Crowdfunding Database

In this section, using QuickDBD, we sketched an ERD to form a table schema of the four csv files we created in Part 2 above. We identified the dependencies between each table (primary and foreign keys), their relationships (one-one/one-many, many-one) and the relevant datatypes for each column.

**Files We Created:**
 - Schema: crowdfunding_db_schema.sql 
 - ERD Diagram: ERD_crowdfunding_db_schema.png

**ERD Diagram:**

![ERD_crowdfunding_db_schema](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/42f17b6b-e8d2-4a89-8b79-a97f748b9856)


### Part 3: Import Data into Crowdfunding Database

Lastly, we created a SQL database (crowdfunding_db) in Postgres through pgAdmin. Table Schema sql file generated through our ERD diagram in QuickDBD was uploaded to create table structure and dependencies. csv files generated in Part 1 were imported into relevant tables using python code using python SQLAlchemy in Juypter Notebook. Select queries were run both in pgAdmin and python.

**Resource Files We Used:**
  - campaign.csv
  - category.csv
  - contacts.csv
  - subcategory.csv

**Our Jupyter Notebook Python Script:**
  - Populating_crowdfunding_db_tables.ipynb
    
**Our SQL Script with SELECT statement used in pgAdmin:**
  - Select_statements.sql
  
**Tools/Libraries We Imported:**
   - pandas library: for data manipulation and analysis
   - sqlalchemy library: provides the SQL toolkit and Object-Relational Mapper (ORM) functionality. The create_engine function is to create a database engine to connect with the database in order to interact with the database, and perform operations such as SQL queries

**Screen shots:**
- Successful schema upload
  
  ![Schema_Upload](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/b2d9ca0a-0020-423f-bcb0-149ae14c0b8e)

- Table dependencies/constraints successfully created on schema upload

![Table_constraints_screen_shot1](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/d9893c70-169a-468f-a1d6-b1ed6b221adb)

![Table_constraints_screen_shot2](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/036f3652-d5db-4ede-980e-6d5a74e1fcec)


- Data from each table displayed successfully using SELECT * statement in pgAdmin (Please reference Populating_crowdfunding_db_tables.ipynb Jupyter notebook showing success of data upload and results of SELECT * statements using python)
  
  - Category Table
    
    ![Select_output_category](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/e2e9b9a1-dcb1-4e09-bae5-b3425d3f3bc1)

  - Subcategory Table
 
    ![Select_output_subcategory](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/8b18e82d-cc8c-467f-98f3-310e5f3b8a2e)

  - Contacts Table

    ![Select_output_contacts](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/85e111a2-408e-4b0e-849b-64a7e958b29e)

  - Campaign Table

![Select_output_campaign_1](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/aa3fe7b1-8b82-4e13-a58a-853922e4231e)
![Select_output_campaign_2](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/192b8db6-b19f-4fe4-9c5c-306501f256ab)
![Select_output_campaign_3](https://github.com/jyojay/Crowdfunding_ETL/assets/132628129/aa6166df-2715-4d1d-9ab5-81fd374b6ddb)

## Getting Started

**Programs/software we used:**
 - Jupyter Notebook: used for python coding in sections.
 - Microsoft Excel: to view csv files. Should be available by default on all PCs.
 - QuickDBD: to sketch an ERD of the tables for the data contained in the csv files. (http://www.quickdatabasediagrams.com/) No need to register, diagram can be generated on the website for free.
 - PostgreSQL: is a relational database management system (RDBMS). An RDBMS consists of tables and their predefined relationships. Postgres stores the data. Refer to "Installing" section below.
 - pgAdmin: The pgAdmin tool functions as the window into the database. It's where queries are written, run and then the results of running them are reviewed. pgAdmin provides access to that data. Refer to "Installing" section below.


**To open the files .ipynb files in Juypter Notebook:**
- Open Anaconda Prompt
- Activate dev environment, type 'conda activate dev'
- Navigate to the folder where repository is saved on local drive
- Open Jupyter Notebook, type 'Jupyter Notebook'

## Installing

**Installation PostgreSQL & pgAdmin:**
 - In your browser, go to Download PostgreSQLLinks: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads.
 - Select the download option for your operating system and the latest version 14.x of PostgreSQL.
 - After downloading the latest version of PostgreSQL 14.x, double-click the postgresql-14.7-2-windows-x64.exe file. Note: The exact file version may be slightly different.
 - Go through the Setup Wizard and install PostgreSQL. Keep the default location C:\Program Files\PostgreSQL\14.
 - Select the components to be installed. Uncheck the option to install Stack Builder.
 - Add your data directory. Keep the default location C:\Program Files\PostgreSQL\14\data.
 - Enter postgres as the password. Be sure to record this password for future use.
 - Keep the default port as 5432. In the Advanced Options, set the locale as [Default locale].
 - The final screen will be the Pre Installation Summary.
 - When you are done, the Postgres 14 folder can be accessed from the Start menu of your computer.
 - This folder contains the pgAdmin 4 application.
 - To confirm the installation, start pgAdmin (this will open in a new browser window). Connect to the default server by clicking on it and entering the password if prompted.

**Installation psycopg2:**
- after activating dev environment in Anaconda Prompt (see Getting Started above), type: "pip install psycopg2"


## Contributing

- How to import csv data to sql: https://www.askpython.com/python-modules/pandas/pandas-to-sql
- Regex testing tool: https://regex101.com/
- Understanding Python Regex: https://learnbyexample.github.io/py_regular_expressions/cover.html


