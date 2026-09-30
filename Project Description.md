# Project Title
### IFEXA HEALTHCARE PERFORMANCE 

##  Project Overview
The project analyzes healthcare data across different Nigerian states, branches, departments, diagnoses, services, patient demographics, financial performance, waiting times, satisfaction scores, and patient outcomes.

The dashboard was designed to answer the key management question:

How is our healthcare organization performing, what are our patients experiencing, and where are the major areas that require attention?

Power BI was used to transform raw healthcare data into an interactive five-page analytical dashboard that allows management to monitor operational performance, patient activity, financial results, and patient experience.

# Business Problem

Healthcare organizations generate large amounts of operational, financial, and patient-related data. However, raw data alone does not provide management with a clear view of organizational performance.

Management needs to understand:

- How many patients are being served?
- How many visits are being recorded?
- How much revenue is being generated?
- How much does the organization spend?
- Which states and branches have the highest activity?
- Which departments handle the highest patient volume?
- Where are patients experiencing longer waiting times?
- How satisfied are patients?
- What are the most common diagnoses and outcomes?
- Which states are meeting their revenue targets?
- Which departments and services contribute most to financial performance?
- Where should management investigate further?

This project addresses these questions by combining healthcare operational, financial, and patient experience data into a centralized Power BI dashboard.

## Project Objectives

The objectives of this project were to:

1. Monitor overall healthcare performance.
2. Analyze patient volume and demographics.
3. Identify high-volume states, branches, and departments.
4. Analyze diagnoses and patient outcomes.
5. Monitor waiting time and patient satisfaction.
6. Evaluate revenue, cost, profit, and profit margin.
7. Compare revenue against state-level targets.
8. Analyze monthly financial and patient trends.
9. Identify operational areas that require further investigation.
10. Provide management with interactive insights for decision-making.
11. Apply Power BI data modelling and DAX techniques.
12. Build a professional multi-page executive dashboard.

## Datasets
The main healthcare transaction table containing 1,200 records.
- Patient Visits
- State Targets
- Date Table

## Tools & Technologies
- Microsoft Power BI
- Power Query
- DAX
- Microsoft Excel
- GitHub
- Data Modelling
- Data Visualization
- Business Intelligence
- Interactive Dashboard Design

## Data Preparation & Cleaning
The dataset was imported into Power BI and prepared using Power Query.

The following checks and transformations were performed:

- Data Quality Checks
- Checked for blank values.
- Checked for null values.
- Checked for duplicate records.
- Reviewed data types.
- Reviewed categorical values.
- Checked date consistency.
- Reviewed numerical fields.
- Checked state and branch values.
- Verified revenue and cost fields.

## Dataset Findings
The dataset contained:
- 1,200 records
- 1,200 unique Patient IDs
- No major blank/null values identified.
- No duplicate rows identified.
- Visit dates covering the full 2025 calendar year.

## Data Transformations
Additional analytical columns were created to support the dashboard, including:
- Age Group
- Patient Type
Age groups were created to support patient demographic analysis.

Patient Type was derived from Visit_Count:

1 → New Patient

>1 → Returning Patient

This classification was used because each Patient_ID appears once in the supplied dataset, meaning repeat patient records could not be directly identified through multiple rows.

## Data Model

A structured data model was created to support filtering, calculations, and interactive reporting.

The model follows a star-schema approach, separating transactional data from supporting dimension/target tables.

### Main Fact Table
- Patient_Visits
### Supporting Tables
- Date_Table
- State_Targets
- Dim_State
The State dimension was used to provide consistent state filtering between patient data and state-level revenue targets.

## DAX Measures
A total of 16 core DAX measures were created for the project. Some of which are:
1. Total Patients
Total Patients =
DISTINCTCOUNT(Patient_Visits[Patient_ID])
2. Total Visits
Total Visits =
SUM(Patient_Visits[Visit_Count])
3. Total Revenue
Total Revenue =
SUM(Patient_Visits[Revenue_NGN])
4. Total Cost
Total Cost =
SUM(Patient_Visits[Cost_NGN])
5. Total Profit
Total Profit =
[Total Revenue] - [Total Cost]

## Interactivity & Power BI Features
Several Power BI features were implemented to make the dashboard interactive.
1. Slicers were used for:
- Date
- State
- Branch
- Department
- Gender
2. Conditional formatting was used to highlight financial performance, particularly:
- Revenue Variance
- Achievement %
- Revenue vs Target
3. Drill-through functionality was included to allow users to move from summary-level information into more detailed analysis.
4. Tooltips were used to provide additional information without overcrowding the main dashboard.
5. Navigation buttons were used to make movement between dashboard pages easier.
6. Bookmarks were used to support interactive dashboard navigation and presentation.
7. Dynamic titles were created to respond to user selections.

## Key Findings & Insights

1. Rivers recorded the highest patient activity
Rivers recorded approximately:
- 322 patient records
- 804 visits
- ₦12.73M revenue
This indicates that Rivers had the highest recorded patient and visit activity among the four states.
### Management Investigation
Management can investigate:
- What is driving the higher patient volume?
- Whether staffing levels are sufficient.
- Whether facilities can accommodate the workload.
-Which services contribute most to the activity.
2. Pediatrics recorded the highest departmental workload
- Pediatrics had the highest number of patient records among departments, with approximately 221 records.
- It also recorded the highest departmental profit at approximately ₦3.71M.
### Management Investigation
Management could investigate:
- Staffing requirements.
- Patient demand.
- Service capacity.
- Revenue contribution.
- Whether additional resources are required.
2. Laboratory had the longest average waiting time
The Laboratory department recorded an average waiting time of approximately 46.97 minutes, compared with an overall average of approximately 45.27 minutes.
### Management Investigation
Management can investigate:
- Patient queues.
- Laboratory workflow.
- Staffing levels.
- Processing time.
- Peak-period workload.
4. Obio-Akpor recorded the highest branch workload
- Obio-Akpor recorded approximately 303 visits, making it the highest-volume branch in the dataset.
- Its average waiting time was approximately 49.03 minutes, while its average satisfaction score was approximately 3.62/5.
### Management Investigation
Management could examine:
- Staffing capacity.
- Patient flow.
- Queue management.
- Appointment scheduling.
- Service capacity during busy periods.
5. Revenue remained below annual targets across all states
Based on the annual state targets and recorded 2025 revenue:
All four states were below their respective annual revenue targets.
### Management Investigation
Management should investigate:
- Whether targets are realistic based on historical activity.
- Which services generate the highest revenue.
- Revenue contribution by department.
- Revenue opportunities within each state.
- Differences between patient volume and revenue generation.

## Management Areas for Further Investigation
Based on the dashboard findings, management can investigate:
1. Revenue Target Performance
- All four states remained below their annual revenue targets.
- Management should investigate the difference between expected and actual revenue.
2. High-Volume Departments
- Pediatrics recorded high patient activity and departmental profit.
- Management should review capacity and resource allocation.
3. Laboratory Waiting Time
- Laboratory had the highest average waiting time.
- Management should investigate workflow and queue management.
4. High-Volume Branches
- Obio-Akpor recorded the highest visit volume.
- Management should review whether the branch has sufficient capacity.
5. State-Level Performance
- Rivers generated the highest revenue, while Anambra had the lowest target achievement percentage among the four states.
- Management can investigate the factors contributing to these differences.

## Recommendations
Based on the dashboard analysis, the following areas can be considered for management investigation:
- Review state-level revenue performance against annual targets.
- Investigate the causes of revenue gaps across states.
- Review staffing and capacity in high-volume departments.
- Investigate Laboratory workflow to reduce unnecessary waiting time.
- Review workload and capacity at high-volume branches.
- Analyze high-performing services and departments for revenue opportunities.
- Monitor patient satisfaction by branch and department.
- Continue tracking patient outcomes to identify changes over time.
- Review whether annual revenue targets align with actual operational capacity.
- Use the dashboard regularly to monitor performance rather than relying on static reports.
