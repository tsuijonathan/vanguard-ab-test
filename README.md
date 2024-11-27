# Vanguard Retirement Investment Planner: A/B Testing

## Overview

This project evaluates the results of a digital experiment conducted by Vanguard to test the impact of a new User Interface (UI) and in-context prompts using various KPI's. The goal is to determine if these changes improve the user experience and increase completion rates. The analysis includes data cleaning, exploratory data analysis (EDA), and hypothesis testing, resulting in actionable insights.

## A/B Testing

Control Group: Clients experienced Vanguard's traditional online process.
Test Group: Clients interacted with the redesigned UI, featuring in-context prompts.

Process Steps: Both groups navigated through a sequence: 
Start: introduction and client onboarding by entering account logon and personal details
Step 1: User inputs financial information, balances, assets, debts
Step 2: Explore different investments strategies and goals
Step 3: Charts with potential investment outcomes
Confirm: Approve plan with print/share options 

Goal: Assess if the redesigned UI leads to higher process completion rates and better KPI results.

## Data:

The dataset contains the following fields:

client_id: Unique identifier for each client.
variation: Group assignment (Test or Control).
visitor_id: Unique ID for each client-device combination.
visit_id: Unique ID for each web session.
process_step: The step in the digital process.
date_time: Timestamp of web activity.
clnt_tenure_yr/mnth: Client tenure in years and months.
clnt_age: Age of the client.
gendr: Gender of the client.
num_accts: Number of accounts the client holds.
bal: Total balance across all accounts.
calls_6_mnth: Number of client calls in the past six months.
logons_6_mnth: Number of client logons in the past six months.

## Methodology

1) Data Cleaning and EDA 
Explored the data using Pandas, Matplotlib and Seaborn to identify data cleaning problems, patterns and trends to provide a client behavior analysis.

2) Calculated Key Performance Indicators 
Completion Rate: The proportion of users who reach the final ‘confirm’ step.
Time Spent on Each Step: The average duration users spend on each step.
Error Rates: If there’s a step where users go back to a previous step, it may indicate confusion or an error. You should consider moving from a later step to an earlier one as an error.

3) Hypothesis Testing
We conducted 2 separate tests comparing the control and test groups from the A/B testing:

Two-Sample Z Test:
H0: completion_rate_test <= completion_rate_control
H1: completion_rate_test > completion_rate_control

Two-Sample T-Test:
H0: avg_time_spent_per_step_younger >= avg_time_spent_per_step_older
H1: avg_time_spent_per_step_younger < avg_time_spent_per_step_older

4) Experiment Evaluation
Assessed whether the experiment was well-structured and recommended improvements

5) Data Visualization and Insights
Utilized Tableau to create interactive dashboards with key findings.

6) Presentation
Presentation slides explaining our process, findings, insights and recommendations with visuals are found at this link: https://www.canva.com/design/DAGXM2Uu19k/nMY5MEVzCy5PUiihnY_8-A/edit?utm_content=DAGXM2Uu19k&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

## Libraries and Tools Used
- Juypter
- Tableau
- pandas
- matplotlib.pyplot
- seaborn
- numpy
- scipy.stats
- statsmodels.api
- canva
- Trello

## Team Members
- Fritzi
- Jonathan