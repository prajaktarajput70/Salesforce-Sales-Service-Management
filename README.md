# Salesforce Admin Project – Project Management System

## Project Overview

This project demonstrates Salesforce Admin concepts by building a **Project Management System**.
The system helps manage projects, resources, and supplies using Salesforce customization features such as custom objects, record types, page layouts, relationships, validation rules, reports, and dashboards.

---

## Platform Used

* Salesforce Lightning Platform
* CRM Customization Features

---

## Project Implementation (Day-wise)

### Day 1 – Custom Objects & Fields

Created Custom Objects:

* Project
* Human Resource
* Supply

Fields Created

Project Object:

* Project Name (Text)
* Project Status (Picklist – Prospecting, Ongoing, Completed)
* Start Date (Date)
* Project Type (Picklist)
* Project Manager (Text)
* Phone (Phone)
* Email (Email)
* Website (URL)

Project Type Values:

* DevOps
* Blockchain
* Salesforce
* Event Planning Services
* Consulting Services
* Marketing Services

Human Resource Object:

* Resource Name (Text)
* Quantity (Number)
* Utilization (Percent)

Supply Object:

* Supply Name (Text)
* Unit Cost (Currency)

---

### Day 2 – Tabs & Lightning Application

Created Custom Tabs:

* Project
* Human Resource
* Supply

Created Lightning App:
**Project Management Application**

Added Tabs:

* Project
* Human Resource
* Supply

---

### Day 3 – Record Types

Created Record Types on Project Object.

IT Record Type
Allowed Project Types:

* DevOps
* Blockchain
* Salesforce

Infrastructure Record Type
Allowed Project Types:

* Event Planning Services
* Consulting Services
* Marketing Services

---

### Day 4 – Page Layout Customization

IT Page Layout Fields:

* Project Name
* Project Status
* Start Date
* Project Type
* Website (Mandatory)

Infrastructure Page Layout

Section 1 – Project Details

* Project Name
* Project Status
* Start Date
* Project Type

Section 2 – Contact Information

* Project Manager
* Phone
* Email
* Website

---

### Day 5 – Relationships & Roll-Up Summary Fields

Relationship 1
Human Resource → Project
Type: Lookup Relationship

Purpose:

* Assign resources to projects
* Track resource allocation

Relationship 2
Supply → Project
Type: Lookup Relationship

Purpose:

* Allocate supplies to projects
* Track supply usage

Roll-Up Summary Fields (Project Object)

1. Total Human Resources – COUNT
2. Total Supplies – COUNT
3. Total Supply Cost – SUM (Unit Cost)

---

### Day 6 – Validation Rules

Start Date Validation
Start date cannot be previous, today, or within next 5 days.

Formula:
Start_Date__c <= TODAY()+5

Phone Number Validation
Phone must be 10 digits and cannot start with 0,1,2,3,4,5.

Formula:
OR(
LEN(Phone) <> 10,
BEGINS(Phone,"0"),
BEGINS(Phone,"1"),
BEGINS(Phone,"2"),
BEGINS(Phone,"3"),
BEGINS(Phone,"4"),
BEGINS(Phone,"5")
)

Utilization Validation
Utilization cannot exceed 100%.

Formula:
Utilization__c > 100

Resource Name Validation
Only alphabets allowed.

Formula:
NOT(REGEX(Resource_Name__c , "^[A-Za-z ]+$"))

---

### Day 7 – Security Configuration

Profiles Created:

* Suppliers
* People Management

Security Settings:

* Removed Project Object access
* Login allowed between 10 AM – 3 PM (Weekdays)
* Password expiry set to 30 days
* Account lock after 3 incorrect attempts

---

### Day 8 – Reports

Created Reports:

* Projects with Human Resources
* Projects with Supplies
* Supply Cost per Project
* Resource Utilization Report

---

### Day 9 – Dashboard

Created Dashboard: **Project Management Dashboard**

Dashboard Components:

* Total Projects
* Project Status Distribution
* Resources per Project
* Total Supply Cost

---

## Key Salesforce Features Used

* Custom Objects
* Custom Fields
* Record Types
* Page Layout Customization
* Lookup Relationships
* Roll-Up Summary Fields
* Validation Rules
* Lightning Application
* Profiles & Security
* Reports
* Dashboards

---

## Author

Prajakta Daryavsing Rajput
