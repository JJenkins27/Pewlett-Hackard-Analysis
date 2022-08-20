# Employee Database Analysis

Using SQL, Postgres, and pgAdmin to analyze employee data for upcoming retirement planning

## Overview of Project

An analysis of employee data tables to provide insight into upcoming retirements and which employees are eligible for the retirement package. Additionally, which employees are eligible for the mentorship program. 

### Purpose

Pewlett Hackard is a large company that employs thousands of people. As baby boomers are beginning to retire at a rapid rate, Pewlett Hackard needs to start planning for retirement packages and replacing the retiring employees in the near future. The number of retirements will leave thousands of open positions. 

Questions posed to analyst are: 
- Who will be retiring in the next few years?
- How many positions will Pewlett Hackard need to fill?
- How many retirees per department?
- How many retirees per title?
- Who is eligible for a mentorship program to train new employees?

## Results

The silver tsunami is going to impact Pewlett Hackard in a major way. Analysis of employee data indicates there are 72,458 employees that are about to retire in the near future.

The retiring employees are spread across the company in all departments. 
- The largest number of employees retiring, 9,281, are in the Development department.
- The second largest number of employees retiring, 8,174, are in the Production department.

While all departments are cruicial to running a business, mass retiring in these two departments could significantly impact future output and earnings.

![retirement_count_names](https://user-images.githubusercontent.com/108373151/185764825-f6c253ae-71b6-4dc0-a7c9-e0ba92171d6a.png)

After grouping the data by most recent title, the following information is noted:
- The majority of employees (about 70%) retiring have Senior titles, which is to be expected as those employees have likely been at the company the longest and probably have received several promotions over the years. 
- Two more managers are about to retire. In other analysis, it was determined that there are only 5 active managers for 9 departments (list of active managers found at this link: [manager_info.csv](Data/manager_info.csv)). After 2 more retire, the company will be even more deficient in this position.

![retiring_titles](https://user-images.githubusercontent.com/108373151/185764416-598a6e01-98cb-48fa-a382-d0649532a87b.png)

In order to assist with the problem of mass employees retiring, the company has decided to implement a mentorship program with employees born in 1965 who are still currently employed. A full list of these names can be found at this link: [mentorship_eligibility.csv](Data/mentorship_eligibility.csv)
- There are 1,549 eligible mentors using these parameters.
- If every eligible employee from these parameters was to sign up for the mentorship program, and there are 72,458 new employees to replace those retiring, there would be 1 mentor for every 47 new employees.

![mentorship_eligibility](https://user-images.githubusercontent.com/108373151/185764573-ffd923e1-a70e-46fd-ad92-a1024db47b2d.png)

### ERD Schema

The image below reflects the conceptual ERD for the employees database.

![EmployeeDB](https://user-images.githubusercontent.com/108373151/185764131-7b802738-b17e-42cd-9d29-903e4d1e8f98.png)

## Summary

With 72,458 employees set to retire in the near future, the impact of the silver tsunami on Pewlett Hackard will be major. They will need to analyze their FTE and potentially replace all those employees with qualified individuals. To ensure their success, Pewlett Hackard is singling out qualified, retirement ready employees to mentor and train the next generation. However, based on their initial thought process, there are only 1,549 eligible mentors. That is 1 mentor for every 47 employees. That is too many new employees to mentor for one individual. To ensure better success in the new generation of employees, the pool of mentors needs to be widened.

Continue to analyze the mentorship eligibility program with the following recommendations: 
- Expanding the birthday year coverage to 5 years (1960-1965) would ensure a larger pool of mentorship-eligible employees. 
- Since the hire date exists in the employees table, include employees that have been working at the company for 10 or more years. 
- Consider the current title of employees, maybe limiting mentors to senior positions.
- Additionally, the table could be broken down into departments of available mentors, as well as their respective titles. 
This further analysis would ensure there is sufficient coverage of qualified mentors in each department. 

Additionally, it seems like there aren't enough managers for each department. This needs to be further analyzed to make sure each department within the company is sufficiently overseen. 
- Find departments without active managers, including the 2 with managers that are ready to retire based on queries above.
- Find list of current employees within those departments.
- Break employee list by department into current titles and length of employment.