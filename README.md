# Crowdfunding_ETL
***Project Team 8: Jyotsna Jayaraman, Asha Kozak and Katharine Tamas***

In this scenario, our team has built an ETL Pipeline. Python, Pandas and Python dictionary methods (and regular expressions to show alternative method) were used to extract, transform and then create csv files. An Entity Relationship Diagram (ERD) and table schema were formed and then the data was uploaded into a Postgres database.

**Repository Folders and Contents:**
- Resources:
  - crowdfunding.xlsx
  - contacts.xlsx
  - campaign.csv
  - category.csv
  - contacts.csv
  - subcategory.csv
- ERD_crowdfunding_db_schema.png
- ELT_Mini_Project_JJayaraman.ipnynb
- ELT_Mini_Project_JKozak.ipnynb
- ELT_Mini_Project_JTamas.ipnynb
- Populating_crowdfunding_db_tables.ipynb
- Schema_Upload.png
- Select_output_campaign_1.png
- Select_output_campaign_2.png
- Select_output_campaign_3.png
- Select_output_category.png
- Select_output_contacts.png
- Select_output_subcategory.png
- Select_statements.sql
- Tables_constraints_screen_shot1.png
- Table_constraints_screen_shot2.png
- crowdfunding_db_schema.sql

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Installing](#installing)
- [Usage](#usage)
- [Contributing](#contributing)

## About
**Part 1: Create DataFrames for Category, Subcategory, Campaign, and Contacts**

At the beginning, we used Jupyter Notebook to import two excel files, that were transformed and manipulated to create four dataframes. These dataframes were then exported into csv files. MORE DETAIL HERE....... 

Resource Files We Used:
  - crowdfunding.xlsx
  - contacts.xlsx

Our Jupyter Notebook Python Scripts:
  - ELT_Mini_Project_JKozak.ipnynb
  - ELT_Mini_Project_JTamas.ipnynb
  - ELT_Mini_Project_JJayaraman.ipnynb

Files We Created:
  - campaign.csv
  - category.csv
  - contacts.csv
  - subcategory.csv

Tools/Libraries We Imported:
   - pandas library: for data manipulation and analysis
   - numpy library: used for numerical computations
   - re library: used for regular expressions to search and manipulate strings in python


**Part 2: Create the Crowdfunding Database**

In this section, using QuickDBD, we sketched an ERD to form a table schema of the four csv files we created in Part 2 above. We identified the dependencies between each table (primary and foreign keys) and the relevant datatypes for each column.

Files We Created:
 - Schema: crowdfunding_db_schema.sql
 - ERD Diagram: ERD_crowdfunding_db_schema.png
 - SQL Code: Select_statements.sql


**Part 3: Import Data into Crowdfunding Database**

Lastly, we created a SQL database in Postgres. Data was imported using python code in Juypter Notebook. ADD MORE INFORMATION.....

Resource Files We Used:
  - campaign.csv
  - category.csv
  - contacts.csv
  - subcategory.csv

Our Jupyter Notebook Python Script:
  - Populating_crowdfunding_db_tables.ipynb

Tools/Libraries We Imported:
   - pandas library: for data manipulation and analysis
   - sqlalchemy library: provides the SQL toolkit and Object-Relational Mapper (ORM) functionality. The create_engine function is to create a database engine to connect with the database in order to interact with the database, and perform operations such as SQL queries

## Getting Started

Programs/software we used:
 - Jupyter Notebook: used for python coding in sections.
 - Microsoft Excel: to view csv files. Should be available by default on all PCs.
 - QuickDBD: to sketch an ERD of the tables for the data contained in the csv files. (http://www.quickdatabasediagrams.com/) No need to register, diagram can be generated on the website for free.
 - PostgreSQL: is a relational database management system (RDBMS). An RDBMS consists of tables and their predefined relationships. Postgres stores the data. Refer to "Installing" section below.
 - pgAdmin: The pgAdmin tool functions as the window into the database. It's where queries are written, run and then the results of running them are reviewed. pgAdmin provides access to that data. Refer to "Installing" section below.


To open the files .ipynb files in Juypter Notebook:

- Open Anaconda Prompt
- Activate dev environment, type 'conda activate dev'
- Navigate to the folder where repository is saved on local drive
- Open Jupyter Notebook, type 'Jupyter Notebook'

## Installing

Installation PostgreSQL & pgAdmin:
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

Installation psycopg2: after activating dev environment in Anaconda Prompt (see Getting Started above), type: "pip install psycopg2"

## Usage

A step by step series of examples that tell you how to get a development env running.

## Contributing

How to import csv data to sql: https://www.askpython.com/python-modules/pandas/pandas-to-sql

