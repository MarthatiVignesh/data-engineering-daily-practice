# Day 5 - Apache Sqoop: Data Ingestion to Hadoop

## Overview

Day 5 focused on Apache Sqoop and importing relational database
data from MySQL into Hadoop HDFS.

## Environment

- Ubuntu
- Hadoop 3.3.6
- Sqoop 1.4.7
- MySQL 8.0.46
- Java 17
- MySQL Connector/J 8.0.33

## Topics Practiced

1. Sqoop fundamentals
2. Connecting Sqoop with MySQL
3. Accessing databases and tables
4. Default Sqoop import
5. Free-form query import
6. Direct import mode
7. HDFS verification
8. Troubleshooting JDBC authentication

## MySQL Practice Database

Database:

sqoop_practice

Table:

employees

Columns:

- id
- name
- department
- salary
- city

The table contains 5 employee records.

## Import Results

### Default Table Import

Target:

/user/sri/day5-employees

Result:

5 records imported successfully.

### Free-form Query Import

The query filtered employees belonging to the IT department.

Target:

/user/sri/day5-it-employees

Result:

2 records imported successfully.

Output:

1,Arjun,IT,55000.00,Hyderabad
4,Priya,IT,70000.00,Hyderabad

### Direct Import

Target:

/user/sri/day5-direct-employees

Sqoop reported:

Beginning mysqldump fast path import

Result:

5 records imported successfully.

## Final Results

| Import Type | Records Imported |
|-------------|------------------|
| Default table import | 5 |
| Free-form query import | 2 |
| Direct import | 5 |

## Troubleshooting

The free-form query initially failed because Sqoop could not
authenticate with the original MySQL account.

The issue was investigated using:

- MySQL account verification
- TCP connection testing
- Sqoop eval
- JDBC connection testing
- MySQL Connector/J verification

After configuring the TCP connection and Connector/J 8.0.33,
the Sqoop free-form query completed successfully.

## Directory Structure

Day-05-Apache-Sqoop-Data-Ingestion/
├── README.md
├── outputs/
│   ├── free-form-query-troubleshooting.txt
│   ├── sqoop-import-output.txt
│   └── sqoop-list-tables-output.txt
├── practice/
│   └── mysql-setup.txt
└── theory/
    ├── mysql-connection.txt
    ├── sqoop-fundamentals.txt
    └── sqoop-import-modes.txt

## Learning Outcome

By completing Day 5, I practiced how Apache Sqoop connects
relational database data with Hadoop and how different import
methods can be used to ingest MySQL data into HDFS.
