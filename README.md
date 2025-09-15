# Daily Sales Report Automation using AWS

> Automating a daily business task that almost every sales or operations team faces.

# Story Behind This Project

Imagine running a growing business with sales happening every day.

Every morning, someone from the team opens the sales spreadsheet, calculates the total number of orders and revenue, drafts a quick summary email, and sends it to the manager.

Seems simple, right?

But now imagine doing this every single day — weekends included.  
The person leaves, falls sick, or just forgets and the report is missed.

I wanted to automate this repetitive pain point that every small-to-medium business faces.

# The Problem

Most businesses store their daily sales data (CSV, Excel, etc.) in some central location like Google Drive or AWS S3.

But there is :
- No summary automatically going to the manager daily 
- No trigger that works even when the team is asleep
- No proper formatting in the email
- And often no one available to do this at 9AM every morning.


# The Solution — Automated Daily Sales Summary

So I built this smart workflow using AWS cloud services that:

1. Reads raw sales data from an S3 bucket (stored daily)
2. Creates schema automatically using AWS Glue
3. Runs SQL queries on the data using Athena
4. Processes the result in a Lambda function
5. Formats the email nicely
6. Sends it through SES
7. Triggered automatically every morning through EventBridge

No one has to log in.  
No one has to run reports.  
The manager wakes up with a clean sales summary email.

# Architecture Overview

![Architecture Diagram](images/daily-sales-report-architecture.png.png)



