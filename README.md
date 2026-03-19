# RPT3000
RPT3000 – COBOL Sales Report Generation
Authors:
Ben Stearns
Aidan Dunbar

Date: 03/19/2026

GitHub:
https://github.com/bstearns07/RPT3000

Overview: RPT3000 is a COBOL program that reads a customer master file and produces a formatted Year-To-Date (YTD) sales report. The report includes:

Customer details

Current and prior year sales

Dollar change in sales

Percentage change in sales

Grand totals across all customers

Includes formatting to make the report appear in a proffesional sense
How It Works:

Opens input and output files

Retrieves current system date and time

Prepares report header fields

Reads each customer record

For each record:

Formats customer data

Computes:

Change Amount = This YTD - Last YTD

Change Percent = (Change / Last YTD) × 100

Handles edge cases:

If Last YTD = 0 → sets percent to 999.9

Writes formatted line to output

Updates running totals

Tracks line count

Prints headings when page limit is reached (55 lines)

Calculates grand totals

Computes overall percentage change

Writes summary line at end of report

This program demonstrates structured COBOL programming, file handling, report formatting, and basic business calculations.

Files

RPT3000.cbl – COBOL source program

JCLRPT2.jcl – JCL used to compile and execute the program

README.md – Project documentation

Notes

Values are hardcoded for demonstration purposes

Numeric editing is used to format output

Program is intended for educational use
