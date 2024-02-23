# ETL Mini Project Readme

This README file provides instructions and guidance for the ETL (Extract, Transform, Load) Mini Project. In this project, you will be working with a partner to build an ETL pipeline using Python and Pandas. The goal is to extract data from Excel files, transform it, create CSV files, design a database schema, and load the data into a PostgreSQL database.

## Project Overview

- **Collaboration**: You will work in pairs, so make sure to communicate and collaborate effectively with your partner.
- **Project Duration**: This project should be completed within one week, with significant progress made by the third day of class.
- **GitHub Repository**: One member of the group should create a new repository named "Crowdfunding_ETL" for this project and add the partner as a collaborator. Do not use an existing repository.
- **Notebook and Resources**: Rename the provided Jupyter notebook file (ETL_Mini_Project_starter_code.ipynb) with both partners' first and last names, and add it to the repository along with the "Resources" folder containing the "crowdfunding.xlsx" and "contacts.xlsx" files. Push these changes to GitHub, and make sure both partners have the updated files on their computers.

## Instructions

The instructions for this ETL Mini Project are divided into several subsections. Follow these steps to complete the project successfully:

### 1. Create the Category and Subcategory DataFrames

- Extract and transform the data from "crowdfunding.xlsx" to create a category DataFrame.
- The category DataFrame should have two columns: "category_id" and "category."
- Export this DataFrame as "category.csv" and save it to your GitHub repository.

### 2. Create the Campaign DataFrame

- Extract and transform the data from "crowdfunding.xlsx" to create a campaign DataFrame.
- The campaign DataFrame should have the following columns:
  - "cf_id"
  - "contact_id"
  - "company_name"
  - "description" (renamed from "blurb")
  - "goal" (converted to float)
  - "pledged" (converted to float)
  - "outcome"
  - "backers_count"
  - "country"
  - "currency"
  - "launch_date" (formatted as "YYYY-MM-DD")
  - "end_date" (formatted as "YYYY-MM-DD")
  - "category_id" (with unique identification numbers)
  - "subcategory_id" (with unique identification numbers)
- Export this DataFrame as "campaign.csv" and save it to your GitHub repository.

### 3. Create the Contacts DataFrame

Choose one of the following options for extracting and transforming the data from "contacts.xlsx":

- **Option 1**: Use Python dictionary methods.
  - Import the "contacts.xlsx" file into a DataFrame.
  - Iterate through the DataFrame, converting each row to a dictionary.
  - Extract the dictionary values from the keys using a list comprehension.
  - Create a new DataFrame with the extracted data.
  - Split each "name" column value into a "first_name" and "last_name" column.
  - Clean and export the DataFrame as "contacts.csv" and save it to your GitHub repository.

- **Option 2**: Use regular expressions.
  - Import the "contacts.xlsx" file into a DataFrame.
  - Extract the "contact_id," "name," and "email" columns using regular expressions.
  - Create a new DataFrame with the extracted data.
  - Convert the "contact_id" column to the integer type.
  - Split each "name" column value into "first_name" and "last_name" columns.
  - Clean and export the DataFrame as "contacts.csv" and save it to your GitHub repository.

### 4. Create the Crowdfunding Database

- Inspect the four CSV files and sketch an Entity-Relationship Diagram (ERD) of the tables using a tool like QuickDBD.
- Use the information from the ERD to create a table schema for each CSV file. Specify data types, primary keys, foreign keys, and other constraints.
- Save the database schema as a PostgreSQL file named "crowdfunding_db_schema.sql" and save it to your GitHub repository.
- Create a new PostgreSQL database named "crowdfunding_db."
- Using the database schema, create the tables in the correct order to handle foreign keys.
- Verify the table creation by running a `SELECT` statement for each table.
- Import each CSV file into its corresponding SQL table.
- Verify that each table has the correct data by running a `SELECT` statement for each.

## Hints and Resources

- To split values in a column, use the `str.split()` method.
- Use NumPy to create unique identification numbers.
- Pay attention to data types when converting columns to float or datetime.
- Use Pandas `merge` function to link dataframes based on common columns.

## Support and Resources

- Seek support from your instructors, learning assistants, and tutors as needed.
- Collaborate and communicate effectively with your project partner.

## Requirements

Here are the key requirements for each part of the project:

- **Category DataFrame**
  - Contains "category_id" and "category" columns.
  - "category_id" entries go sequentially from "cat1" to "catn".
  - "category" column contains only category titles.
  - Exported as "category.csv."

- **Subcategory DataFrame**
  - Contains "subcategory_id" and "subcategory" columns.
  - "subcategory_id" entries go sequentially from "subcat1" to "subcatn".
  - "subcategory" column contains only subcategory titles.
  - Exported as "subcategory.csv."

- **Campaign DataFrame**
  - Contains specified columns with appropriate data types.
  - "launch_date" and "end_date" formatted as "YYYY-MM-DD."
  - "category_id" and "subcategory_id" contain unique identification numbers.
  - Exported as "campaign.csv."

- **Contacts DataFrame (15 points)**
  - Contains specified columns with appropriate data types.
  - "name" column split into "first_name" and "last_name."
  - Exported as "contacts.csv."

- **Crowdfunding Database**
  - Database schema file ("crowdfunding_db_schema.sql") created.
  - "crowdfunding_db" database created with the correct schema.
  - Tables created with appropriate primary and foreign keys.
  - CSV files imported successfully into the tables.
  - Data in each table verified with `SELECT` statements.

Please refer to the detailed project instructions for each part for more information.

Best of luck with your ETL Mini Project!
