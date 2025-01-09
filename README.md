# **Vanguard Retirement Investment Planner: A/B Testing**

## **Business Description**
Vanguard is a leading US-based investment management company that provides a variety of financial services, including retirement investment planning. The company aims to enhance its **digital client experience** by optimizing its online process through modernized interfaces and timely in-context prompts.

---

## **Project Overview**
This project evaluates the results of an **A/B test** conducted by Vanguard to determine whether the introduction of a **new User Interface (UI)** and **in-context prompts** improves user experience and increases **completion rates**. The analysis involved **data cleaning**, **exploratory data analysis (EDA)**, **statistical testing**, and delivering **actionable recommendations** based on **key performance indicators (KPIs)**.

---

## **Table of Contents**
- [Business Problem](#business-problem)
- [Data](#data)
- [Process](#process)
- [Tools Used](#tools-used)
- [Results](#results)
- [Recommendations](#actionable-recommendations)
- [How to Navigate Through the Project](#how-to-navigate-through-the-project)
- [Links](#links)

---

## **Business Problem**
The experiment was designed to evaluate whether a modernized **digital process** improves customer experience and leads to **higher completion rates** compared to the traditional process.

### **Key Questions to Answer**:
1. Does the new UI and prompts lead to **higher completion rates**?  
2. Do **younger clients** complete steps faster compared to **older clients**?  
3. What are the **patterns of drop-off** in the process?  

---

## **Data**
The dataset spans from **March 15, 2017, to June 20, 2017**, and contains the following fields:

### **Client Information**:
- `client_id`: Unique identifier for each client.  
- `clnt_tenure_yr/mnth`: Client tenure with Vanguard.  
- `clnt_age`: Client's age.  
- `gendr`: Client's gender.  
- `num_accts`: Number of accounts the client holds.  
- `bal`: Total balance across accounts.  

### **Process Information**:
- `variation`: Group assignment (Control or Test).  
- `visitor_id`: Unique ID for client-device combinations.  
- `visit_id`: Unique session ID.  
- `process_step`: Digital process step.  
- `date_time`: Timestamp of activity.  

### **Behavioral Information**:
- `calls_6_mnth`: Calls made by the client in the last six months.  
- `logons_6_mnth`: Logins by the client in the last six months.  

---

## **Process**

### **Outline of Steps**:
1. **Data Cleaning**  
   - Addressed missing values, standardized column names, and filtered relevant dates.

2. **Exploratory Data Analysis (EDA)**  
   - Identified trends in user behavior, completion rates, and demographics.

3. **Key Performance Indicator (KPI) Calculations**  
   - Completion rates, average time spent, and error rates.

4. **Statistical Testing**  
   - Hypothesis tests on completion rates and time spent.

5. **Data Visualization**  
   - Used Tableau for interactive dashboards showcasing user profiles, KPIs, and group comparisons.

6. **Insights and Recommendations**  
   - Derived actionable insights to improve client engagement.

---

## **Results**

### **1. Summary of Client Profiles**

#### **Clients’ Demographics**:
- **Age**: Average age is **48.5 years**; most clients are aged **50–64 (34%)**.  
- **Gender**:
  - 33.63% are men.  
  - 32.47% are women.  
  - 33.90% have an unknown or undisclosed gender.

#### **Clients’ Relationship with Vanguard**:
- **Tenure**: Most clients (50%) have been with Vanguard for **6 to 16 years**, with an average tenure of **12 years**.  
- **Account Balances**: Average balance is **$162,217**, with a median of **$69,241**.  
- **Accounts Held**: 80% of clients have **2 accounts**.  

---

### **2. Key Performance Indicators**

| KPI                        | Control Group (%) | Test Group (%) |
|----------------------------|-------------------|----------------|
| Completion Rate            | 65.58            | 69.30         |
| Avg Time per Step (secs)   | 34.11            | 57.01         |
| Error Rate                 | 3.32             | 5.25          |
| Engagement (Logons)        | 6.31             | 6.24          |

#### **Time Spent on Each Step**:

| Process Step  | Control (secs) | Test (secs) |
|---------------|----------------|-------------|
| Start         | 140            | 154         |
| Step 1        | 41             | 36          |
| Step 2        | 37             | 42          |
| Step 3        | 90             | 93          |
| Confirm       | 127            | 118         |

---

### **3. Hypothesis Testing**

#### **Completion Rate**:
- **H0**: Completion rate (Test) ≤ Completion rate (Control).  
- **H1**: Completion rate (Test) > Completion rate (Control).  
- **Result**: Null hypothesis rejected. Test group had a significantly higher completion rate.

#### **Time Spent by Age**:
- **H0**: Younger clients take as much or more time than older clients.  
- **H1**: Younger clients take less time.  
- **Result**: Null hypothesis rejected. Younger clients complete steps faster.

---

### **Actionable Recommendations**

1. **Client Research**  
   - Conduct **surveys and focus groups** to understand the specific needs and preferences of different client demographics:
     - Younger clients: Assess interest in **mobile-first designs**, **app-driven navigation**, and **AI-powered financial tools** for a seamless, tech-friendly experience.
     - Older clients: Explore preferences for **browser-based platforms**, **step-by-step guidance**, and **clear, static layouts** for ease of use and reassurance.
   - Analyze **customer feedback** from recent interactions (e.g., live chat transcripts, support emails) to identify pain points and usability concerns.
   - Segment clients by tenure, account balances, and logon behavior to uncover patterns in how different groups interact with the process and which features they value most.
   - Use insights to tailor future enhancements, such as creating separate workflows for tech-savvy and less tech-savvy clients.

---

2. **Optimize Process Steps**  
   - **Streamline Step 1 (Financial Details)**:
     - Introduce **auto-filled fields** based on existing client data, reducing manual entry and potential errors.
     - Provide **dynamic hints** or tooltips that explain required inputs in real-time (e.g., “Enter your total savings here”).
   - **Enhance Step 3 (Charts and Outcomes)**:
     - Include a **simplified summary option** for clients who prefer less detailed charts while maintaining in-depth visuals for advanced users.
     - Offer a comparison of **three clear scenarios** (e.g., conservative, moderate, aggressive investment outcomes) to make decision-making easier.
   - Implement **real-time validation** at each step to minimize the need for users to backtrack and re-enter information.
   - Add a **progress tracker** at the top of the screen to provide clear visibility into how far along users are in the process.

---

3. **UI Improvements**  
   - **Simplify Step 2 (Investment Exploration)**:
     - Use **plain language** descriptions instead of jargon, ensuring clarity for all users.
     - Add interactive **“learn more” links** for users who want additional details without overloading the main interface.
   - **Redesign the Confirmation Stage**:
     - Present a **summary of key decisions** before final submission, allowing clients to review their choices without navigating back through earlier steps.
     - Use **visual confirmations**, such as checkmarks or green highlights, to reassure users that they’ve completed the process successfully.
   - Test various layouts and color schemes to ensure accessibility for all users, including those with visual impairments or color blindness.

---

4. **Error Rate Reduction**  
   - Introduce **context-specific error messages**:
     - Instead of generic messages (e.g., “Invalid input”), provide detailed guidance like, “Please enter a number between $1,000 and $1,000,000.”
   - Offer a **help icon** on every page that users can click for quick answers to common questions.
   - Deploy **live chat or chatbot support** for real-time assistance during critical steps, such as financial data entry or the confirmation process.
   - Monitor error-prone areas using **backend analytics** to identify and prioritize fixes for specific technical or design issues.
   - Add a **feedback option** at the point of abandonment, asking users why they’re leaving to better understand usability challenges.

---

5. **Flexible Experimentation**  
   - Design **rolling experiments** that allow dynamic adjustments based on performance:
     - Start with smaller sample sizes and expand as trends stabilize.
     - Use **adaptive testing** to modify the experiment in real-time based on early results (e.g., extending the test for certain demographics showing unexpected behavior).
   - Introduce **group-specific testing thresholds**:
     - Younger clients: Shorter test cycles to capture quick adoption of new features.
     - Older clients: Longer test durations to account for slower adoption and feedback loops.
   - Regularly review **real-time dashboards** that track KPIs like completion rates, error rates, and time per step to intervene early if issues arise.
   - Experiment with **personalized interfaces** during testing:
     - Group A sees a modern, app-driven design.
     - Group B experiences a more traditional, straightforward layout.
   - Collect and analyze feedback after each test phase to iterate on future UI and process enhancements.

---

## **Tools Used**
- **Jupyter Notebook**  
- **Tableau**  
- Python Libraries:  
  - `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy.stats`, `statsmodels.api`

---

## **How to Navigate Through the Project Files**
1. **Data**: Cleaned datasets.  
2. **Notebooks**: Code for data cleaning, EDA, and hypothesis testing.  
3. **Dashboards**: Tableau visualizations of key insights.  
4. **Presentation**: Summary of findings and recommendations.

---

## **Links**

### **Tableau Dashboards**
- **User Profile**: [View Dashboard](https://public.tableau.com/app/profile/friederike.augustin/viz/vanguard_customer_profile/Dashboard_User_Profile)  
- **Investments**: [View Dashboard](https://public.tableau.com/app/profile/friederike.augustin/viz/vanguard_customer_profile/Dashboard_Bal_Accounts?publish=yes)  
- **KPIs**: [View Dashboard](https://public.tableau.com/app/profile/jonathan.tsui8842/viz/project2KPI/Dashboard1?publish=yes)  
