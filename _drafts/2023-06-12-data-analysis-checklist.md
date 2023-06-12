---
layout: post
title: A High-Level Data Analysis Checklist
date: 2023-06-12 10:34:00-0400
last_edited:
categories: ["Productivity", "Data Analysis"]
related_posts: false
img: assets/img/data_analysis.jpg
---

To easily reference the six steps (Ask, Prepare, Process, Analyze, Share, Act) of the data analysis process, I thought I would create a high-level data analysis checklist. Enjoy! 

# Data Analysis Checklist

## 1. Ask
- Ask SMART (specific, measurable, achievable, relevant, time-bound) and effective questions
- Structure how you think
- Summarize data
- Put things into context
- Manage team and stakeholder expectations
- Problem-solve and conflict-resolution

## 2. Prepare
- Ensure ethical data analysis practices
- Address issues of bias and credibility
- Access databases and import data
- Write simple queries
- Organize and protect data
- Connect with the data community (optional)

## 3. Process
- Connect business objectives to data analysis
- Identify clean and dirty data
- Clean small datasets using spreadsheet tools
    - Sources of errors: Did you use the right tools and functions to find the source of the errors in your dataset?
    - Null data: Did you search for NULLs using conditional formatting and filters?
    - Misspelled words: Did you locate all misspellings?
    - Mistyped numbers: Did you double-check that your numeric data has been entered correctly?
    - Extra spaces and characters: Did you remove any extra spaces or characters using the TRIM function?
    - Duplicates: Did you remove duplicates in spreadsheets using the Remove Duplicates function or DISTINCT in SQL?
    - Mismatched data types: Did you check that numeric, date, and string data are typecast correctly?
    - Messy (inconsistent) strings: Did you make sure that all of your strings are consistent and meaningful?
    - Messy (inconsistent) date formats: Did you format the dates consistently throughout your dataset?
    - Misleading variable labels (columns): Did you name your columns meaningfully?
    - Truncated data: Did you check for truncated or missing data that needs correction?
    - Business Logic: Did you check that the data makes sense given your knowledge of the business? 
- Clean large datasets by writing SQL queries
    
- Document data-cleaning processes

## 4. Analyze
- Sort data in spreadsheets and by writing SQL queries
- Filter data in spreadsheets and by writing SQL queries
- Convert data
- Format data
- Substantiate data analysis processes
- Seek feedback and support from others during data analysis

## 5. Share
- Create visualizations and dashboards in Tableau
- Address accessibility issues when communicating about data
- Understand the purpose of different business communication tools
- Tell a data-driven story
- Present to others about data
- Answer questions about data

## 6. Act 
- Code in R
- Write functions in R
- Access data in R
- Clean data in R
- Generate data visualizations in R
- Report on data analysis to stakeholders

