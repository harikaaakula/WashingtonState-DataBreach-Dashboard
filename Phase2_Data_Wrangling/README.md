# Phase 2 – Data Wrangling and Exploratory Analysis

## Objective
This phase focused on **Data preparation and Exploration** using Power Query and Power BI to ensure the dataset accurately supports the five derived research questions in Phase 1 of Research Design.

---

## Data Wrangling Process

### Issue Identified
The original dataset contained multiple rows for the same `Breach ID`, since **Each record of a Breach had various types of information compromised** (e.g., SSN, Medical Data, Financial Info), which resulted in **Duplicate IDs with Unique “Information Type” entries**.

---

### Approach
To handle this, **Two separate Queries** were created in Power Query:

| Query Name | Description | Purpose |
|-------------|--------------|----------|
| **InformationType_Aggregate_CleanData** | Aggregated view where each `Breach ID` appears only once. Aggregated all related information types into a single field (e.g., concatenated list of compromised types). | Used for **Overall breach-level analysis** (e.g., breach count, cause, affected individuals). |
| **InformationType_Specific_CleanData** | Detailed view preserving one row per `(Breach ID, Information Type)` pair. | Used for **Information Type-specific Analysis** (e.g., how often each type of information was compromised). |

---

### Power Query Steps Summary

**For InformationType_Aggregate_CleanData:**
- Removed unnecessary columns or columns not required to analyse for the identified research questions.
- Grouped by `Breach ID`.
- Aggregated “Information Type” using `Text.Combine()` to list all unique types.
- Ensured numeric fields (e.g., affected individuals) were aggregated using `List.Max()` or `List.Sum()` where appropriate.
- Removed duplicates and validated record count.

**For InformationType_Specific_CleanData:**
- Retained one record per unique `(Breach ID, Information Type)`.
- Cleaned column names and standardised text formats.
- Ensured consistency with the summary query (data types, relationships).

---

## Data Modelling
Both queries were loaded into Power BI and connected via the **Breach ID** field:
- Relationship type: *One-to-many*  
  (One Breach ID in the aggregated query → Many Information Types in the Specific query)
- This model allows flexible visuals that can analyse overall breaches or zoom into data type specifics.

---

## Exploratory Analysis
Key Research Questions addressed after modifying initially identified questions:

Key visuals created using both queries:
- **Line Chart:** Yearly trends of breaches and affected individuals (using `InformationType_Summary`).
- **Stacked Column Chart:** Frequency of each compromised information type (using `InformationType_Detail`).
- **Heatmap:** Relationship between industry and breach cause.

---

## Deliverables
- Queries:
  - `InformationType_Summary.csv`
  - `InformationType_Detail.csv`
  - Query_steps_executed.md
- Power BI Model (`PowerBI_Second_Deliverable.pbix`)
- Visual Previews (`/Visuals_Preview`)

---

## Reflection
Creating two structured queries allowed:
- **Aggregation without losing granularity**.
- Improved data accuracy and analytical flexibility.
- Demonstrated strong Power Query transformation logic and relational modelling skills.
