# HealthConnect Clinic — Appointment No-Show Analysis
## Project Overview
HealthConnect Clinic is a fictional outpatient healthcare analytics project focused on understanding appointment attendance and no-show behaviour.
The project uses Python, Pandas, SciPy, and Power BI to perform exploratory analysis, statistical validation, risk segmentation, and decision-support reporting.

## Business Problem

The goal is to identify the factors associated with appointment no-shows and translate those findings into practical recommendations for improving appointment attendance and clinic capacity utilisation.

HealthConnect therefore needs to understand:

- How frequently appointments are attended, missed or cancelled. 
- Which patient and appointment characteristics may be associated with no-shows.
- Whether booking lead time is related to attendance.
- Whether previous no-show behaviour is associated with future attendance.
- Whether reminders and reminder channels may influence appointment outcomes.
- Whether factors such as distance and waiting time may be associated with attendance patterns.

The goal is not to diagnose patients or make clinical decisions, but to analyse appointment and operational data to support better administrative decision-making.

## Dataset Overview

The HealthConnect appointment dataset contains:

- 5,000 appointment records
- 18 variables
- Appointment-level data
- Anonymised patient identifiers
- Adult patient records
- Appointment booking and scheduling information
- Reminder information
- Operational information
- Final appointment outcomes

  ## HealthConnect Knowledge Base

The analysis is supported by the approved HealthConnect Clinic Knowledge Base, which provides the operational context for interpreting the dataset.

The Knowledge Base establishes that HealthConnect:

- Has two fictional clinic locations.
- Provides general, follow-up, specialist and diagnostic services.
- Uses appointment-based care.
- Allows appointments to be rescheduled or cancelled.
- Encourages patients to arrive at least 15 minutes before appointments.
- Encourages patients who cannot attend to contact the clinic as early as possible.
- May use appointment reminders.
- Directs medical or clinical questions to qualified healthcare professionals.
- Important Analytical Boundary

The dataset and analysis are focused on administrative and operational appointment behaviour.

## The project will not:

- Diagnose medical conditions.
- Predict or interpret individual patient health conditions.
- Recommend treatment or medication.
- Make clinical decisions.
- Assume that demographic characteristics cause a patient's behaviour.
- Invent clinic policies, prices or appointment availability.


## Business Questions

The initial analysis will investigate the following business questions:

- What proportion of HealthConnect appointments are attended, missed or cancelled?
- Which appointment types have the highest no-show rates?
- Are no-show rates different across age groups?
- Does booking lead time appear to be associated with appointment attendance?
- Are patients with previous no-shows more likely to miss future appointments?
- Is appointment timing associated with different attendance patterns?
- Is there an observable relationship between reminders and appointment attendance?
- Do different reminder channels show different appointment outcomes?
- Is distance from the clinic associated with appointment attendance?
- Is estimated waiting time associated with appointment outcomes?

These questions will guide the detailed analysis in the next stage of the project.



## Project Objectives

## Week 4 project objectives were to:

- Understand the HealthConnect business problem.
- Understand the available appointment dataset.
- Review the dataset structure and Data Dictionary.
- Identify variables relevant to appointment attendance and no-shows.
- Define meaningful business questions.
- Identify potential business KPIs.
- Establish the initial analytical approach.
- Identify project limitations, risks and dependencies.
- Establish a foundation for the detailed analysis to follow.


## Week 5 — Exploratory Data Analysis
Analysed 5,000 appointment records and investigated no-show behaviour across:
-	Appointment type
-	Age and gender
-	Appointment day and time
-	Booking lead time
-	Previous appointments
-	Previous no-shows
-	Reminder status and channel
-	Distance to clinic
-	Waiting time
##### The overall no-show rate was 48.46%.
##### The strongest Week 5 finding was booking lead time:
-	0–14 days: 30.60%
-	15–29 days: 43.04%
-	30–44 days: 52.82%
-	45–60 days: 67.23%
A Power BI Executive Overview dashboard was developed to communicate these findings.


## Week 6 — Advanced Analytics & Decision Support
Week 6 focused on validating the Week 5 findings and identifying higher-risk appointment segments.
##### Statistical testing confirmed significant associations between no-show behaviour and:
-	Booking lead time: χ² = 359.38, p < 0.001
-	Previous appointment history: χ² = 11.84, p = 0.0079
-	Distance: χ² = 16.21, p = 0.0010
-	Reminder status: χ² = 6.30, p = 0.0120
##### Previous no-show behaviour was identified as an important behavioural indicator:
-	0 previous no-shows: 43.51%
-	1: 53.49%
-	2: 59.36%
-	3: 67.95%
##### The highest-risk segment identified was appointments booked 45–60 days in advance for patients living 15+ km from the clinic:
73.00% no-show rate | 237 appointments | 173 no-shows
This was 24.54 percentage points above the overall clinic rate.

## Key Findings
#### The current risk hierarchy is:
Booking lead time → Previous no-show behaviour → Distance → Reminder status → Previous appointment history
The analysis identifies associations, not causation.
#### Power BI
Two dashboard pages have been developed:
##### Executive Overview
-	Overall appointment KPIs
-	No-show rate analysis
-	Patient and appointment segmentation
##### Advanced Decision Support
-	45–60 day no-show rate: 67.23%
-	High-risk no-show rate: 73.00%
-	High-risk difference: +24.54 pp
-	High-risk appointments: 237

  
### Data Science Handover
A binary no_show_target was created for future predictive modelling.
#### Potential predictors include:
booking_lead_days, previous_appointments, previous_no_shows, distance_to_clinic_km, reminder_sent, reminder_channel_model, appointment_type, age_group, appointment_time, and appointment_day.
appointment_outcome is excluded from modelling to prevent target leakage.
#### Tools
Python: Pandas, NumPy, SciPy, Matplotlib, Jupyter
Power BI: Power Query, DAX, interactive dashboards
Version Control: Git & GitHub
#### Project Status
- Week 5: Completed
- Week 6: Completed
- Week 7: Predictive analytics, model testing, feature evaluation and validation
