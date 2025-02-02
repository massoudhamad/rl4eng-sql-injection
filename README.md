# SQL Injection Labs
My lab notes and learning progress for the Web Security Academy's SQL Injection chapter.

This repository is a record of my labs for "Chapter 1: SQL injection" following PortSwigger's Web Security Academy training path https://portswigger.net/web-security/sql-injection

The labs are done on Kali Linux VM on VirtualBox, where I also utilize Burp Suite Community Edition 2023.7.2.

**Environment Setup Instructions:** https://github.com/kienmarkdo/Netcat-NMAP-Lab

## General Notes
Prior to doing these labs, I learned the basic theory of:
- What is an SQL injection?
  - Types of SQL injections
- How do I find it?
  - Methodologies for Black / Grey / White Box Testing
  - Leverage automation to find vulnerabilities
- How do I exploit it?
  - Explore these in the labs
- How do I prevent it?
  - Prepared Statements, Stored Procedures, Whitelist Input Validation, Escaping All User Supplied Input, Enforce Least Privilege

![image](https://github.com/kienmarkdo/SQL-Injection-Labs/assets/67518620/33cbdd8a-4a44-4ecd-b429-1683fe381b7e)

## Lab Contents
### Basic SQL injections
- Lab 01 - Retrieval of hidden data using WHERE clause
- Lab 02 - SQL injection vulnerability allowing login bypass
- Lab 03 - SQL injection UNION attack to determine number of columns in a table
- Lab 04 - SQL injection UNION attack to determine data type of columns in a table
- Lab 05 - SQL injection UNION attack to retrieve data from other tables
- Lab 06 - SQL injection UNION attack to retrieve multiple values in a single column
### Examining the database
- Lab 07 - Querying the database type and version on Oracle
- Lab 08 - Querying the database type and version on MySQL and Microsoft
- Lab 09 - Listing the database contents on non-Oracle databases
- Lab 10 - Listing the database contents on Oracle databases
### Blind SQL injections
- Lab 11 - Blind SQL injection with conditional responses
- Lab 12 - Blind SQL injection with conditional errors
- Lab 13 - Blind SQL injection with time delays
- Lab 14 - Blind SQL injection with time delays and information retrieval
- Lab 15 - Blind SQL injection with out-of-band interaction (Burp Pro required)
- Lab 16 - Blind SQL injection with out-of-band data exfiltration (Burp Pro required)
- Lab 17 - SQL injection with filter bypass via XML encoding
- Lab 18 - Visible error-based SQL injection

NOTE: For labs that require Burp Suite Pro features that do not have any workarounds, such as Burp Collaborator, I learned the theory behind it without solving the lab on Web Security Academy.

## Automation
Most of the labs were solved manually then scripted using Python.

Manual SQL injections (or manual pen testing in general) via random payloads is time-consuming; moreover, bots can already do this and it will only catch the low hanging fruits. As such, I will not only try to solve these labs manually, but also I will attempt to write Python scripts that perform the SQL injections.

When I do come across a vulnerability that requires scripting/automation in the future, such as a blind SQL injection vulnerability, I will have been more familiar with it. For instance, many blind SQLi vulnerabilities require some form of enumeration (i.e. password enumeration/brute-force). Rather than using Burp Intruder to do the enumeration, I can script the enumeration process in Python instead.

## References
https://github.com/kienmarkdo/SQL-Injection-Labs

<!-- Written by Kien Do: https://github.com/kienmarkdo/SQL-Injection-Labs -->
