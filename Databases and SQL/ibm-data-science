# IBM Data Science - Dabases and SQL

Created by: Sangwook Cheon

Date: June 3, 2019

Supplementary notes for the Database and SQL course provided by IBM, in addition to Jupyter Notebooks. These notes are created while watching classroom videos to catch anything that might not be included in the notebooks.

### Table of Contents:

- Introduction to SQL and Databases
- Basic SQL Commands
  - Create Table
  - Select
  - Count, Distinct, Limit
  - Insert
  - Update
  - Delete

## Introduction to SQL and Databases

**SQL** is a language used for relational databases to query data.

- Relational databases are data stored in tabular form, with columns and rows.
- RDBMS (Relational Database Management System) is a software tool for storing, organizing, and managing data. Not all types of data are in tabular form.

**Basic SQL Commands**: Create, Insert, Select, Update, Delete

**Cloud Database**: A a database service built and accessed through a Cloud platform. It serves many of the same functions as traditional databases with the added flexibility of **Cloud computing**. Users install software on a Cloud infrastructure to implement the database. Advantages include:

- Ease of use, users can access Cloud databases from virtually anywhere using a vendors API or web interface. 
- Scalability, Cloud databases can expand their storage capacities during runtime to accommodate changing needs, organizations only pay for what they use. 
- Disaster recovery, in the event of a natural disaster equipment failure or power outage data is kept secure through backups on remote servers.

Can use services like IBM db2 or AWS (I would personally go for AWS).



## Basic SQL Commands

DDL (Data Definition Language) statements: Define, change or drop data.

DML (Data Manipulation Language) statements: Read and motify data.

### Create Table Statement

General Syntax:

```sql
create table TABLENAME (
    COLUMN1 datatype,
    COLUMN2 datatype,
    COLUMN3, datatype,
        ...
    ) ;
```

To walk through an example:

```sql
drop table COUNTRY
create table COUNTRY (
    ID int NOT NULL,
    CCODE char(2),
    NAME varchar(60),
    PRIMARY KEY (ID)
    );
```

In the above example, we create a table called COUNTRY. We first drop the table with the same name if it already exists. The ID column has the "NOT NULL" constraint added after the datatype - meaning that it cannot contain a NULL or an empty value. We are also using ID as a "PRIMARY KEY," where there cannot be null values by default. A Primary Key is a unique identifier in a table, and using Primary Keys can help speed up queries significantly.

CCODE is a two letter country code column, and NAME is a variable length country-name column.  



### Select Statement

Use Select statement to see (read) the data. This statement is a DML statement aimed at reading data.

Select Statement: Query

Result from the query: Result set/table

**# RDBMS** supports all the inequality operators used in Python (same syntax), with one difference:

- Not equal is noted by ```<>```, not ```!=```.

General Syntax for Select Statemnet:

```sql
select COLUMN1, COLUMN2, ... from TABLE1 ;
```

To retrieve a list of all country names and their IDs from the COUNTRY table:

```sql
select ID, NAME from COUNTRY ;
```

To retrieve all columns from the COUNTRY table we could use "*" instead of specifying individual column names:

```sql
select * from COUNTRY ;
```

The ```where``` clause can be added to the query to filter results or get specific rows of data. To retrieve data for all rows in the COUNTRY table where the ID is less than 5:

```sql
select * from COUNTRY where ID < 5 ;
```

In case of character based columns, the values of the predicates in the where clause need to be enclosed in **single quotes**. To retrieve the data for the country with country code "CA":

```sql
select * from COUNTRY where CCODE = 'CA'; 
```



### Count, Distinct, Limit


