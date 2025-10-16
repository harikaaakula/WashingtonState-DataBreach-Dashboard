# Washington-State-Data-Breach-Dashboard

# Data Breach Dashboard – Washington State (Power BI Project)

## Project Overview
This Power BI project analyzes **Data Breaches affecting Washington residents** between 2016 to 2026. It was developed as a three-phase coursework project focusing on data storytelling, Exploratory Data Analysis, and Dashboard Design.  
The goal is to provide actionable insights for the **Washington Attorney General’s Office** and Cybersecurity Professionals to better understand Data Breach trends, industry vulnerabilities, and risk management patterns.

---

## Project Phases

### Phase 1 – Project Proposal & Research Design
- Defined project goals using the **SMART model (Doran, 1981)**.  
- Identified Dataset: *Data Breach Notifications Affecting Washington Residents (Personal Information Breakdown)*.  
- Designed **Five guiding research questions** focusing on breach frequency, causes, Information types compromised, and Breach lifecycle.
- Outlined dataset variables, data types, audience, use cases, and suggested visualizations.

---

### Phase 2 – Data Wrangling & Exploratory Data Analysis
- Conducted Data cleaning and wrangling in Power BI using **Power Query**.
- Created relationships and a structured **data model**.
- Generated visuals addressing each research question:
  - Time trends of breach incidents
  - Breach cause by industry
  - Data types compromised
  - Breach lifecycle vs. number of residents affected
- Used **Berinato’s Setup–Conflict–Resolution framework** for visualization storytelling.

---

### Phase 3 – Final Dashboard
- Built an Interactive **Power BI dashboard** to communicate findings to policymakers and risk managers.
- Added **More Info** and **Conclusions** pages inside the dashboard for information on dataset and Conclusions drawn from dashboard.
- Followed Data storytelling principles to make complex breach data accessible to non-technical audiences.

---

##  Dataset Details
**Source:**: Data.Breach Notifications Affecting Washington Residents | Data.WA.gov (https://data.wa.gov/Consumer-Protection/Data-Breach-Notifications-Affecting-Washington-Res/padd-mby7/about_data)  
**Rows:** 6,386  **Columns:** 16  **Years Covered:** 2014–2026  

**Key Variables:**
| Variable | Type | Description |
|-----------|------|-------------|
| DataBreachCause | Categorical | Reason for data breach (Cyberattack, Theft/Mistake, Unauthorized Access) |
| WashingtoniansAffected | Numeric | Number of affected individuals (15–328,889) |
| IndustryType | Categorical | Sector affected (Finance, Health, Education, etc.) |
| InformationType | Categorical | Type of personal data compromised |
| BreachLifecycleRange | Categorical | Duration from identification to reporting (1–99 days, etc.) |
| CyberattackType | Categorical | Attack vector (Malware, Phishing, Ransomware, etc.) |

---

## Target Audience
- **Washington Attorney General’s Office**
- **Policymakers & Legislators**
- **CISOs & Cybersecurity Analysts**
- **Business Leaders** managing risk in vulnerable industries

---

##  Key Insights
1. **Ransomware** and **Malware** cyberattack types are the most common attacks observed over a period of 2016 to 2026.
2. The **Business and Health** industries show the highest vulnerability.
3. **Retail** Business type with in the Business Industry are the most predominently getting attacked from 2016 to 2026
4. Clear upward trend in reported incidents post-2019, suggesting increased regulatory reporting compliance.

---

## Dashboard Preview

<img width="1315" height="738" alt="image" src="https://github.com/user-attachments/assets/f59524a5-b95f-468a-bcf5-3acfcd609ced" />

## Tools & Techniques
- **Power BI Desktop**
- **Power Query** (Data Wrangling)
- **DAX Measures**
- **Data Storytelling Frameworks (Berinato, Knaflic)**

---

## Learnings & Reflection
This project strengthened my understanding of:
- The end-to-end Power BI workflow — from data cleaning to visualization.
- Applying storytelling to complex cybersecurity datasets.
- Designing dashboards that drive **data-informed decision-making**.
  
##  References
- Verizon Data Breach Investigations Report (2025)  
- Doran, G. (1981). *There’s a S.M.A.R.T. Way to Write Management’s Goals and Objectives.*  
- Fotis, F. (2024). *Economic Impact of Cyber Attacks and Cyber Risk Management Strategies.*  
- Washington State Attorney General Data Portal
