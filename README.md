# OOP Bank Account & Pandas Analysis

A simple Python project that demonstrates Object-Oriented Programming (OOP) by creating a bank account system, tracking transactions, exporting transaction data to CSV, and analyzing the data using Pandas.

## Features

- Create a bank account using a custom `BankAccount` class
- Deposit money into the account
- Withdraw money from the account
- Maintain the current account balance
- Validate deposits and withdrawals
- Track every transaction with date and time
- Store transaction details in a structured format
- Export transaction history to a CSV file
- Analyze transaction data using Pandas
- Generate descriptive statistics

## Technologies Used

- Python
- Pandas
- CSV
- Object-Oriented Programming (OOP)
- Datetime

## Core Concepts Covered

### Object-Oriented Programming

The project uses a custom `BankAccount` class to manage account information and transactions.

The class contains the following methods:

- `deposit()` - Adds money to the account
- `withdraw()` - Withdraws money from the account
- `_add_transaction()` - Records transaction details
- `export_to_csv()` - Exports transaction history to a CSV file

### Data Handling

Transaction details are stored using Python dictionaries inside a list. The transaction history is converted into a Pandas DataFrame and exported as a CSV file.

### Pandas Data Analysis

Pandas is used to read and analyze the generated transaction dataset.

The project uses:

- `read_csv()` - Reads the CSV dataset
- `head()` - Displays the first few records
- `sum()` - Calculates total transaction volume
- `value_counts()` - Counts transactions by type
- `describe()` - Generates descriptive statistics

## Project Workflow

```text
Create Bank Account
        ↓
Deposit / Withdraw Money
        ↓
Update Account Balance
        ↓
Record Transaction
        ↓
Export Transaction History to CSV
        ↓
Read CSV using Pandas
        ↓
Analyze Transaction Data


Project Structure
OOP-Bank-Account/
│
├── main.py
├── bank_transactions.csv
└── README.md


File Description
File	Description
main.py	Contains the BankAccount class, transaction logic, CSV export, and Pandas analysis
bank_transactions.csv	Stores the generated transaction history
README.md	Project documentation
Sample Transactions

The account starts with an initial balance of $5000.

Transaction	Amount	Balance After
Deposit	$1500	$6500
Withdrawal	$700	$5800
Withdrawal	$300	$5500
Deposit	$2000	$7500
Sample Output

The following is an example of what the program displays after running the transactions:

Successfully deposited $1500. Current Balance: $6500.0
Successfully withdrew $700. Current Balance: $5800.0
Successfully withdrew $300. Current Balance: $5500.0
Successfully deposited $2000. Current Balance: $7500.0

Transactions saved to bank_transactions.csv

==================================================
           PANDAS DATASET ANALYSIS
==================================================

1. Data Head:

  Account_Number Holder_Name        Type  Amount  Balance_After
0        ACC1001       Shifa     Deposit    1500         6500.0
1        ACC1001       Shifa  Withdrawal     700         5800.0
2        ACC1001       Shifa  Withdrawal     300         5500.0
3        ACC1001       Shifa     Deposit    2000         7500.0

2. Total Volume Processed:

$4500

3. Transactions Count by Type:

Deposit       2
Withdrawal    2

4. Summary Statistics:

            Amount  Balance_After
count     4.000000       4.000000
mean   1125.000000    6325.000000
min     300.000000    5500.000000
max    2000.000000    7500.000000
Pandas Dataset Analysis

The generated CSV file contains the following information:

Column	Description
Account_Number	Unique bank account number
Holder_Name	Name of the account holder
Type	Deposit or Withdrawal
Amount	Transaction amount
Balance_After	Account balance after the transaction
Timestamp	Date and time of the transaction
Total Transaction Volume

The total transaction amount processed in the sample is:

$4500
Transactions Count by Type

The sample contains:

Deposit       2
Withdrawal    2

This means:

2 deposit transactions were made.
2 withdrawal transactions were made.
Summary Statistics

Pandas describe() is used to calculate:

Count
Mean
Standard deviation
Minimum
25th percentile
50th percentile
75th percentile
Maximum
Validation

The program checks for invalid transactions.

Deposit Validation
Deposit amount must be greater than zero.
Withdrawal Validation
Withdrawal amount must be greater than zero.
Withdrawal amount cannot be greater than the available balance.

If an invalid transaction is entered, the program displays an appropriate message.

Learning Outcomes

This project demonstrates:

Python classes and objects
Methods and encapsulation
Conditional statements
Lists and dictionaries
File handling
CSV data storage
Pandas DataFrames
Data analysis
Basic statistical analysis
Date and time handling
