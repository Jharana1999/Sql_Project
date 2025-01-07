# Data Analyst SQL Queries

## Project Overview
This project contains a collection of SQL queries designed to extract insights from a job postings dataset, specifically focusing on remote Data Analyst roles. The queries analyze job demand, average salaries, top-paying roles, and key skills required for high-paying jobs. The dataset includes job postings facts, skills data, and company information.

## Queries Overview
### 1. High Demand High Salary
**Objective:** Identify high-demand skills for remote Data Analyst roles with competitive average salaries.

**Key Metrics:**
- Skill demand count
- Average annual salary

**Query Breakdown:**
- The `skills_demand` CTE calculates the demand count for each skill.
- The `average_salary` CTE calculates the average salary associated with each skill.
- The final query joins the CTEs and filters for skills with a demand count greater than 10, sorted by average salary in descending order.

### 2. Top 5 Most In-Demand Skills
**Objective:** Identify the top 5 most in-demand skills for Data Analyst roles.

**Key Metrics:**
- Skill demand count

**Query Logic:**
- Counts the number of job postings associated with each skill and sorts the results in descending order by demand count.

### 3. Top Paying Roles
**Objective:** Identify the top 10 highest-paying remote Data Analyst roles.

**Key Metrics:**
- Job title
- Job location
- Salary
- Company name

**Query Logic:**
- Filters for remote positions with non-null salary values and sorts the results by salary in descending order.

### 4. Skills for Top Paying Roles
**Objective:** Identify the skills associated with the top-paying remote Data Analyst roles.

**Key Metrics:**
- Skill name
- Average annual salary

**Query Logic:**
- Calculates the average salary for each skill across all job postings and sorts the results by average salary in descending order.

### 5. Skills for Top 10 Paying Jobs
**Objective:** Identify the skills required for the top 10 highest-paying remote Data Analyst roles.

**Query Logic:**
- Uses a CTE to select the top 10 highest-paying jobs and joins it with skills data to extract associated skills.


## Dataset Structure
The project utilizes the following tables:
- **job_postings_fact:** Contains job postings data including job IDs, titles, locations, schedules, salaries, and posting dates.
- **skills_job_dim:** A mapping table linking job postings to specific skills.
- **skills_dim:** Contains the list of skills along with their IDs.
- **company_dim:** Contains company information such as company ID and name.


## Instructions to Run the Queries
1. Clone this repository to your local machine.
2. Load the dataset into your SQL environment.
3. Execute the queries in the order provided or based on your analysis needs.

## Tools Used
- SQL
- Database Management System (DBMS)
