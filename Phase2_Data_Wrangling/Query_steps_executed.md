# Query: InformationType_Specific_CleanData

## Goal
Create one row per unique Information Type to analyse Information compromised trends.

### Steps Performed in Power Query
1. Loaded original dataset.
2. Removed unnecessary columns DateStart, DateEnd, WashingtoniasAffectedRange, BreachLifecycleRange, EntityState.
3. Standardised the rest other columns to make sure the data types are correct.
4. Replaced the null values in WashingtoniasAffected columns with 0
5. Replaced the null values in CyberattackType with Not Reported as there were rows where CyberattackType is not reported
6. Replaced the null values in BusinessType with Not Applicable as Business types are classified for the Industries where the IndustryType column defined as "Business"
7. Formatted the Categorical Variables 
8. No duplicates found so didn't removed any rows.
9. Loaded the final table into Power BI model

---

# Query: InformationType_Aggregate_CleanData

## Goal
Create one row per unique Breach ID summarizing all Information Types.

### Steps Performed in Power Query
1. Loaded original dataset.
2. Removed unnecessary columns DateStart, DateEnd, WashingtoniasAffectedRange, BreachLifecycleRange, EntityState.
3. Standardised rest other columns to make sure the data types are correct.
4. Replaced the null values in WashingtoniasAffected columns with 0
5. Replaced the null values in CyberattackType with Not Reported as there were rows where CyberattackType is not reported
6. Replaced the null values in BusinessType with Not Applicable as Business types are classified for the Industries where the IndustryType column defined as "Business"
7.The dataset was grouped by key incident attributes (Id, DateAware, DateSubmitted, DataBreachCause, Name, CyberattackType, IndustryType, BusinessType, Year) to create unique records for each breach.
8. For each group, the maximum value of WashingtoniansAffected was retained, and all corresponding InformationType entries were combined into a single column, InformationTypes_Aggregated, separated by semicolons (;).
9. The intermediate nested table used for aggregation was then removed, leaving a clean dataset with one row per incident and all associated information types preserved.
9. Formatted the Categorical Variables 
10. No duplicates found so didn't removed any rows.
11. Loaded the final table into Power BI model
