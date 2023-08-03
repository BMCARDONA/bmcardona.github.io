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

# Ideas:
- Heatmap of temperatures in a country during a specific month

# Data Analysis Checklist

<!-- ##################### 1. ASK #################### -->

## 1. Ask
- Ask SMART (specific, measurable, achievable, relevant, time-bound) and effective questions
- Structure how you think
- Summarize data
- Put things into context
- Manage team and stakeholder expectations
- Problem-solve and conflict-resolution

#### Skills:
- How data analysts solve problems with data
- The use of analytics for making data-driven decisions
- Spreadsheet formulas and functions
- Dashboard basics, including an introduction to Tableau
- Data reporting basics

<!-- ##################### 2. PREPARE #################### -->

## 2. Prepare
- Ensure ethical data analysis practices
- Address issues of bias and credibility
- Access databases and import data
- Write simple queries
- Organize and protect data
- Connect with the data community (optional)

#### Skills:
- How data is generated
- Features of different data types, fields, and values
- Database structures
- The function of metadata in data analytics
- Structured Query Language (SQL) functions

<!-- ##################### 3. PROCESS #################### -->

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

#### Skills:
- Data integrity and the importance of clean data
- The tools and processes used by data analysts to clean data
- Data-cleaning verification and reports
- Statistics, hypothesis testing, and margin of error
- Resume building and interpretation of job postings (optional)

<!-- ##################### 4. ANALYZE #################### -->

## 4. Analyze
- Steps data analysts take to organize data
    - subqueries
- How to combine data from multiple sources
- Spreadsheet calculations and pivot tables
- SQL calculations
- Temporary tables
- Data validation

#### Skills:
Sorting data in spreadsheets and by writing SQL queries
Filtering data in spreadsheets and by writing SQL queries
Converting data
Formatting data
Substantiating data analysis processes
Seeking feedback and support from others during data analysis


<!-- ##################### 5. SHARE #################### -->

## 5. Share
- Create visualizations and dashboards in Tableau
    - Five-second rule: A data visualization should be clear, effective, and convincing enough to be absorbed in five seconds or less.
    - Color contrast: Graphs and charts should use a diverging color palette to show contrast between elements.
    - Conventions and expectations: Visuals and their organization should align with audience expectations and cultural conventions. For example, if the majority of your audience associates green with a positive concept and red with a negative one, your visualization should reflect this.
    - Minimal labels: Titles, axes, and annotations should use as few labels as it takes to make sense. Having too many labels makes your graph or chart too busy. It takes up too much space and prevents the labels from being shown clearly.
    - McCandless Method lists four elements of good data visualization: 
        - Information: the data you are working with
        - Story: a clear and compelling narrative or concept
        - Goal: a specific objective or function for the visual
        - Visual form: an effective use of metaphor or visual expression
        - Follow this high level 60-minute chart to guide your thinking whenever you begin working on a data visualization. 
            - Prep (5 min): Create the mental and physical space necessary for an environment of comprehensive thinking. This means allowing yourself room to brainstorm how you want your data to appear while considering the amount and type of data that you have.
            - Talk and listen (15 min): Identify the object of your work by getting to the “ask behind the ask” and establishing expectations. Ask questions and really concentrate on feedback from stakeholders regarding your projects to help you hone how to lay out your data. 
            - Sketch and design (20 min): Draft your approach to the problem. Define the timing and output of your work to get a clear and concise idea of what you are crafting.
            - Prototype and improve (20 min): Generate a visual solution and gauge its effectiveness at accurately communicating your data. Take your time and repeat the process until a final visual is produced. It is alright if you go through several visuals until you find the perfect fit. 
    - Cheatsheet: https://towardsdatascience.com/the-ultimate-cheat-sheet-on-tableau-charts-642bca94dde5
- Address accessibility issues when communicating about data
- Understand the purpose of different business communication tools
- Tell a data-driven story
- Present to others about data
    - What's the single most important thing I want my audience to learn from my analysis?
    - Characters, setting, plot, big reveal, aha moment
    - less than 5 lines; less than 25 words
    - Evaluating your recorded presentation
        - Do you:
            - Use an attention-grabbing opening?
            - Start with broad ideas and later talk about specific details?
            - Speak in short sentences?
            - Pause for five seconds after showing a data visualization?
            - Pause intentionally at certain points?
            - Keep the pitch of your voice level?
            - Stand still and move with purpose?
            - Maintain good posture?
            - Look at your audience (or camera) while speaking?
            - Keep your message concise?
            - End by explaining why the data analysis matters?
    - Best practices for slide decks:
        - Include a title, subtitle, and date
        - Use a logical sequence of slides
        - Provide an agenda with a timeline
        - Limit the amount of text on slides. Your audience should be able to scan each block of text on your slides within 5 seconds
        - Start with the business task. Focus on the business task and frame the information in the context of the business task.
        - Establish the initial hypothesis
        - Show what business metrics you used
        - Use visualizations
        - Introduce the graphic by name
        - Provide a title for each graph
        - Go from the general to the specific
        - Use speaker notes to help you remember talking points
        - Include key takeaways
- Answer questions about data

#### Skills:
- Design thinking
- How data analysts use visualizations to communicate about data
- The benefits of Tableau for presenting data analysis findings
- Data-driven storytelling
- Dashboards and dashboard filters
- Strategies for creating an effective data presentation

<!-- ##################### 6. ACT #################### -->

## 6. Act 
- Code in R
- Write functions in R
- Access data in R
- Clean data in R
- Generate data visualizations in R
- Report on data analysis to stakeholders

#### Skills:
- Programming languages and environments
- R packages
- R functions, variables, data types, pipes, and vectors
- R data frames
- Bias and credibility in R
- R visualization tools
- R Markdown for documentation, creating structure, and emphasis

<!-- ##################### R Programming #################### -->

## What you will learn: 
- Programming languages and environments
- R packages
- R functions, variables, data types, pipes, and vectors
- R data frames
- Bias and credibility in R
- R visualization tools
- R Markdown for documentation, creating structure, and emphasis

## Skills
- Coding in R
- Writing functions in R
- Accessing data in R
- Cleaning data in R
- Generating data visualizations in R
- Reporting on data analysis to stakeholders

<!-- ##################### Capstone #################### -->

## What you will learn:
- How a data analytics portfolio distinguishes you from other candidates
- Practical, real-world problem-solving
- Strategies for extracting insights from data
- Clear presentation of data findings
- Motivation and ability to take initiative

## Skill sets you will build:
- Building a portfolio
- Increasing your employability
- Showcasing your data analytics knowledge, skill, and technical expertise
- Sharing your work during an interview
- Communicating your unique value proposition to a potential employer

# Course 1– Foundations: Data, Data, Everywhere

- Introducing data analytics: Data helps us make decisions, in everyday life and in business. In this first part of the course, you will learn how data analysts use tools of their trade to inform those decisions. You will also get to know more about this course and the overall program expectations.

- Thinking analytically: Data analysts balance many different roles in their work. In this part of the course, you will learn about some of these roles and the key skills that are required. You will also explore analytical thinking and how it relates to data-driven decision making.

- Exploring the wonderful world of data: Data has its own life cycle, and data analysts use an analysis process that cuts across and leverages this life cycle. In this part of the course, you will learn about the data life cycle and data analysis process. They are both relevant to your work in this program and on the job as a future data analyst. You will be introduced to applications that help guide data through the data analysis process.

- Setting up a data toolbox: Spreadsheets, query languages, and data visualization tools are all a big part of a data analyst’s job. In this part of the course, you will learn the basic concepts to use them for data analysis. You will understand how they work through examples provided.

- Discovering data career possibilities: All kinds of businesses value the work that data analysts do. In this part of the course, you will examine different types of businesses and the jobs and tasks that analysts do for them. You will also learn how a Google Data Analytics Certificate will help you meet many of the requirements for a position with these organizations.


# Course 2 – Ask Questions to Make Data-Driven Decisions

- Asking effective questions: To do the job of a data analyst, you need to ask questions and problem-solve. In this part of the course, you’ll check out some common analysis problems and how analysts solve them. You’ll also learn about effective questioning techniques that can help guide your analysis.

- Making data-driven decisions: In analytics, data drives decision making. In this part of the course, you’ll explore data of all kinds and its impact on decision making. You’ll also learn how to share your data through reports and dashboards.

- Mastering spreadsheet basics: Spreadsheets are an important data analytics tool. In this part of the course, you’ll learn both why and how data analysts use spreadsheets in their work. You’ll also explore how structured thinking can help analysts better understand problems and come up with solutions. 

- Always remembering the stakeholder: Successful data analysts learn to balance needs and expectations. In this part of the course, you’ll learn strategies for managing the expectations of stakeholders while establishing clear communication with your team to achieve your objectives.  


# Course 3 – Prepare Data for Exploration

- Understanding data types and structures: We all generate lots of data in our daily lives. In this part of the course, you will check out how we generate data and how analysts decide which data to collect for analysis. You’ll also learn about structured and unstructured data, data types, and data formats as you start thinking about how to prepare your data for exploration.

- Understanding bias, credibility, privacy, ethics, and access: When data analysts work with data, they always check that the data is unbiased and credible. In this part of the course, you will learn how to identify different types of bias in data and how to ensure credibility in your data. You will also explore open data and the relationship between and importance of data ethics and data privacy.

- Databases: Where data lives: When you are analyzing data, you will access much of the data from a database. It’s where data lives. In this part of the course, you will learn all about databases, including how to access them and extract, filter, and sort the data they contain. You will also check out metadata to discover the different types and how analysts use them.

- Organizing and protecting your data: Good organization skills are a big part of most types of work, and data analytics is no different. In this part of the course, you will learn the best practices for organizing data and keeping it secure. You will also learn how analysts use file naming conventions to help them keep their work organized.

- Engaging in the data community (optional): Having a strong online presence can be a big help for job seekers of all kinds. In this part of the course, you will explore how to manage your online presence. You will also discover the benefits of networking with other data analytics professionals.


# Course 4 – Process Data from Dirty to Clean 

- Ensuring data integrity. Data integrity is necessary to ensure a successful analysis. In this part of the course, you will explore methods and steps that analysts take to check data for integrity. This includes knowing what to do when you have an insufficient amount of data. You will also learn about sample size, avoiding sample bias, and using random samples. All of these measures also help to ensure a successful data analysis.

- Understanding clean data. Every data analyst wants clean data to work with when performing an analysis. In this part of the course, you will learn the difference between clean and dirty data. You will practice data cleaning techniques in spreadsheets and other tools.

- Cleaning data using SQL. Knowing a variety of ways to clean data can make an analyst’s job much easier. In this part of the course, you will use SQL to clean data from databases. You will explore how SQL queries and functions can be used to clean and transform your data before an analysis.

- Verifying and reporting cleaning results. Cleaning data is an important step in the data analysis process. In this part of the course, you will verify that data is clean and report data cleaning results. With verified clean data, you will be ready for the next step in the data analysis process.

- (Optional) Adding data to your resume. Creating an effective resume will help you in your data analytics career. In this part of the course, you will learn all about the job application process. Your focus will be on building a resume that highlights your strengths and relevant experience. 


# Course 5 – Analyze Data to Answer Questions

- Organizing data to begin analysis. Organizing data makes the data easier to use in an analysis. In this part of the course, you will learn the importance of organizing your data with sorting and filtering. You will explore organizing data in both spreadsheets and with SQL queries and temporary tables.

- Formatting and adjusting your data. As you move closer to analyzing your data, you will want to have the data formatted and ready to go. In this part of the course, you will learn all about converting and formatting data, including how to use SQL queries to combine data. You will also discover the value of feedback and support from your colleagues and how it can lead to new insights that you can apply to your work.

- Aggregating data for analysis. During an analysis, you might need to combine data to gain insights and complete business objectives. In this part of the course, you will explore the functions, procedures, and syntax to combine, or aggregate data. You will learn how to combine data within multiple cells in spreadsheets, and within multiple database tables using SQL queries. 

- Performing data calculations. Calculations are one of the more common tasks that data analysts perform during an analysis. In this part of the course, you will explore formulas, functions, and pivot tables in spreadsheets and SQL queries. All of these are used in data calculations. You will also learn about the benefits of using SQL to manage temporary database tables. 

# Course 6 – Share Data Through the Art of Visualization

- Data visualization: Data visualization is in many ways the culmination of the data analysis process. In this part of the course, you will be introduced to the concepts involved in data visualization. You will learn about accessibility, design thinking, and other factors that play a role in visualizing the data in your analysis.

- Data visualizations with Tableau: Tableau is a tool that can help analysts create effective data visualizations. In this part of the course, you will learn all about Tableau and its uses. You will also explore the importance of creativity and clarity while visualizing your findings appropriately.

- Stories about your data: Connecting your objective with your data through insights is essential to good data storytelling. In this part of the course, you will learn about data-driven stories and their attributes. You will also gain an understanding of how to use Tableau to create dashboards and dashboard filters. 

- Developing presentations and slideshows: In this part of the course, you will discover how to give an effective presentation about your data analysis. You will consider all aspects of your analysis when creating a presentation and learn how to use multiple data sources in the data visualizations you will share. In addition, you will learn how to anticipate potential limitations and questions that might arise and how to provide useful answers to stakeholders.


# Course 7 - Data Analysis with R Programming

- Understanding the basics of R: R is a programming language that can be used to perform tasks in every phase of the data analysis process. In this part of the course, you will learn about R and RStudio, an integrated developer environment (IDE) for R. You will explore the benefits of using RStudio to work with R. RStudio enables you to easily leverage the features and functionality of R. 

- Programming using RStudio: In this part of the course, you will explore the fundamental concepts associated with R. You will learn about functions and variables that you can use in your calculations and other programming. You will also learn about R packages, which are collections of R functions, code, and sample data that you can use in RStudio.

- Working with data in R: The R programming language was designed to work with data at all stages of the data analysis process. In this part of the course, you will examine how R can help you structure, organize, and clean your data through functions and other processes. You will learn about data frames and how to work with them in R. You will also revisit the concept of data bias and how you can use R to address it.

- Visualizations, aesthetics, and annotations: R is a great tool for creating detailed visualizations. In this part of the course, you will learn how to use R to generate and troubleshoot visualizations. You will also explore the features of R and RStudio that can help you improve the aesthetics of your visualizations. You will learn how to annotate visualizations and save the changes. 

- Documentation and reports: R has a number of different options to explore when you are ready to save and present your analysis. In this part of the course, you will explore R Markdown, a file format for making dynamic documents with R. You will learn how to format and export R Markdown and incorporate R code chunks in your documents.
