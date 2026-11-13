# Government Scheme Outcome & Policy Impact Intelligence

### A Public-Sector Programme Performance, Budget Utilization and Outcome Monitoring Solution using SAP Analytics Cloud

**Developed by: Yash Verma**

---

## Project Overview

This project focuses on designing an analytics solution to monitor the performance of a hypothetical government skills development programme across different districts and training sectors in Karnataka, India.

The objective was to bring important programme indicators into a consolidated analytical view, making it easier to understand budget utilization, enrolment performance, training completion, certification and employment placement outcomes.

The solution was developed using **SAP Analytics Cloud (SAC)**, covering data preparation, data modelling, source-to-target mapping, data upload, analytical exploration, custom KPI calculations and interactive story development.

This is an independently developed portfolio project and is not an official government project.


<img width="1916" height="969" alt="p5" src="https://github.com/user-attachments/assets/3d72f7ee-f593-4758-9f0b-306a58c0fa48" />


---

## Business Problem

Government skill development programmes involve multiple performance indicators, districts, training sectors and reporting periods.

Monitoring these indicators separately can make it difficult to identify performance gaps and understand whether programme objectives are being achieved.

The project addresses the following business questions:

- How effectively is the allocated programme budget being utilized?
- Are enrolment targets being achieved?
- How many enrolled candidates successfully complete their training?
- What proportion of assessed candidates receive certification?
- How effectively are certified candidates progressing into employment?
- How does placement performance differ across districts?

## Project Objectives

1. Develop a consolidated view of programme performance.
2. Monitor budget utilization and target achievement.
3. Analyse the progression of candidates through the training and employment process.
4. Compare performance across districts and training sectors.
5. Present meaningful insights through interactive SAP Analytics Cloud dashboards.
6. Support data-driven programme monitoring and decision-making.

---

## Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| SAP Analytics Cloud | Data modelling, analysis and dashboard development |
| SAP SAC Modeler | Model creation, data mapping and data upload |
| SAP Data Analyzer | Data exploration and analytical validation |
| Microsoft Excel | Dataset preparation and data validation |
| SAP Analytics Cloud Stories | Interactive reporting and visualization |

---

## Dataset Information

The project uses a structured synthetic dataset created for analytical and demonstration purposes.

### Dataset Summary

| Attribute | Details |
|---|---|
| State | Karnataka (hypothetical programme scenario) |
| Number of Records | 288 |
| Districts | 12 |
| Training Sectors | 6 |
| Reporting Period | FY 2025–26 |
| Time Dimension | Q1, Q2, Q3 and Q4 |
| Data Format | Excel Workbook |
| Data Nature | Synthetic |

### Dataset Structure

The dataset follows a district–training sector–quarter level structure.

Each record represents one combination of district, training sector and quarter.

The dataset includes information related to:

- State and District
- Training Sector
- Financial Year and Quarter
- Budget Allocated
- Actual Expenditure
- Enrolment Target and Actual Enrolment
- Completion Target and Actual Completion
- Assessed Candidates
- Certification Target and Actual Certifications
- Placement Target and Actual Placements

The workbook also includes supporting sheets for the data dictionary, KPI definitions and project assumptions.

### Why I Used a Synthetic Dataset

During the project, my SAP Analytics Cloud free trial was due to expire within the next two to three days.

Rather than spending the remaining trial period searching for a suitable dataset, I decided to prepare a structured synthetic dataset and focus on implementing the complete analytics workflow in SAC.

At that stage, I was also unfamiliar with open government data portals. After completing the project, I became aware of these sources and their potential for future analytical work.

This allowed me to use the available time effectively while gaining practical experience with data modelling, mapping, calculations, analysis and reporting.

**Data Disclaimer:** All dataset records and calculated results are illustrative. They do not represent actual Karnataka government programme statistics or official government outcomes.

---

## Implementation Workflow

The project was developed through the following stages.

### 1. Dataset Preparation

Prepared a structured Excel dataset containing 288 records across 12 districts, 6 training sectors and 4 quarters.

Reviewed the dataset structure and maintained supporting documentation through the data dictionary, KPI definitions and assumptions sheets.

**Evidence: Dataset Structure**

<img width="1919" height="1027" alt="1" src="https://github.com/user-attachments/assets/984c772e-eae4-417e-b7be-08ce3d0dbe50" />


### 2. Data Modelling in SAP Analytics Cloud

Created the analytical model in SAP Analytics Cloud Modeler.

Configured the required dimensions and measures to represent programme attributes and numerical performance indicators.

**Dimensions included:**
- State
- District
- Training Sector
- Financial Year
- Quarter

**Measures included:**
- Budget Allocated
- Actual Expenditure
- Enrolment Target
- Enrolled Actual
- Completion Target
- Completed Actual
- Assessed Actual
- Certification Target
- Certified Actual
- Placement Target
- Placed Actual

**Evidence: SAC Data Model**

<img width="1919" height="913" alt="4" src="https://github.com/user-attachments/assets/4d6852a5-2032-46a4-ac03-76bb07a2e2d5" />


### 3. Source-to-Target Data Mapping

Performed source-to-target mapping during the data import process.

Mapped the incoming Excel fields to their corresponding dimensions and measures in the SAC model.

This ensured that the source data was aligned with the model structure before completing the import process.

**Evidence: Data Mapping**

<img width="1919" height="909" alt="7" src="https://github.com/user-attachments/assets/13f2017a-44b3-4e58-bcaa-b4414e82c756" />


### 4. Data Upload and Import Process

Configured and executed the data upload process through SAC Modeler.

Used the upload job to bring the prepared Excel data into the analytical model.

Verified the upload status and confirmed that 288 records were successfully uploaded.

**Evidence: Successful Data Upload**

<img width="1919" height="989" alt="8" src="https://github.com/user-attachments/assets/64c4fe70-97cf-417a-ab20-00b6a7b7552e" />


### 5. Data Exploration Using Data Analyzer

Used SAP Analytics Cloud Data Analyzer to explore the imported data and examine programme performance across dimensions such as district, financial year and quarter.

Created analytical views using relevant measures and dimensions to understand performance at different levels of detail.

This helped validate the calculations and explore the underlying data beyond the final dashboard visuals.

**Evidence: Data Analyzer**

<img width="1916" height="913" alt="10" src="https://github.com/user-attachments/assets/301f21b6-ba24-4f2d-a5e8-d8f82090e05b" />
<img width="1919" height="945" alt="12" src="https://github.com/user-attachments/assets/85ef1974-0c65-4dc7-8bc0-a8efacdb8e6b" />


### 6. Custom KPI Calculations

Created calculated measures to convert the underlying programme figures into meaningful performance indicators.

The five main dashboard KPIs are:

| KPI | Calculation |
|---|---|
| Budget Utilization | Actual Expenditure / Budget Allocated × 100 |
| Enrolment Target Achievement | Enrolled Actual / Enrolment Target × 100 |
| Training Completion Rate | Completed Actual / Enrolled Actual × 100 |
| Certification Rate | Certified Actual / Assessed Actual × 100 |
| Placement Rate | Placed Actual / Certified Actual × 100 |

These calculations help measure different stages of programme performance, from budget utilization to employment placement.

For overall percentage calculations, the intended approach is to calculate the ratio using aggregated numerator and denominator values rather than averaging individual district percentages.

---

## Final Dashboard & Reporting

Developed a two-page interactive SAP Analytics Cloud Story.

### Page 1: Executive Programme Overview

The first page provides a consolidated view of the programme through five KPI cards and four visualizations.

**Key components:**
- Budget Utilization by District
- Enrolment: Target vs Actual
- Training Completion Rate by District
- Certification Rate per District
- Five programme-level KPI cards

This page is designed to help programme decision-makers quickly understand overall performance and compare districts.

<img width="1916" height="969" alt="p5" src="https://github.com/user-attachments/assets/6c43a9a1-13ad-4cec-aca1-1d62f8786f2d" />


### Page 2: District Performance Analysis

The second page focuses on district-wise employment placement performance.

**Key components:**
- Placement Rate by District
- Placement Target vs Actual by District

This page helps identify differences in placement outcomes across districts and highlights where actual placements are above or below the defined targets.

<img width="1916" height="826" alt="Screenshot 2026-11-13 150610" src="https://github.com/user-attachments/assets/704d9375-4b2d-4902-9089-e61dc3095dac" />


---

## Key Analytical Results

The final dashboard presents the following overall KPI values:

| Performance Indicator | Result |
|---|---:|
| Budget Utilization | 87.94% |
| Enrolment Target Achievement | 103.58% |
| Training Completion Rate | 89.66% |
| Certification Rate | 86.22% |
| Placement Rate | 77.89% |

These figures are based on the synthetic dataset and are intended to demonstrate the analytical capabilities of the solution.

### How the Solution Supports Decision-Making

The solution demonstrates how programme monitoring can be improved through a consolidated analytical view.

It can help decision-makers:

- Monitor budget utilization alongside programme outcomes.
- Identify districts with relatively lower training completion or certification rates.
- Compare enrolment targets with actual enrolments.
- Understand the conversion of certified candidates into employment placements.
- Compare district-level placement performance against targets.
- Focus further investigation and programme support on areas showing performance gaps.

The dashboards provide visibility into programme indicators; they do not independently establish the causes of performance differences.

---

## Project Deliverables

The repository contains the following project materials:

- Project report and documentation
- Synthetic Excel dataset
- Data dictionary
- KPI definitions
- Project assumptions
- SAP Analytics Cloud story export
- Implementation and dashboard screenshots

---

## Project Scope & Limitations

- This is an independent portfolio project, not an official government implementation.
- The dataset is synthetic and does not represent actual government records.
- The results are illustrative and should not be interpreted as actual public-sector performance.
- The solution demonstrates analytical monitoring and reporting, not a live government deployment.
- The project focuses on data modelling, data integration, calculations, analysis and story development in SAP Analytics Cloud.

---

## What I Learned

Through this project, I gained practical experience in:

- Structuring data for analytical reporting.
- Creating dimensions and measures in SAP Analytics Cloud Modeler.
- Performing source-to-target mapping.
- Configuring and executing data upload jobs.
- Exploring data using SAP Data Analyzer.
- Developing custom calculated KPIs.
- Building interactive stories and visualizations.
- Translating business questions into analytical requirements.
- Presenting data in a format that supports business decision-making.

---

## Author

**Yash Verma**
This project was independently conceptualized and developed as part of my effort to apply analytical concepts using SAP Analytics Cloud.
