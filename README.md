# Hospital Operations Analysis
## Business Problem / Objective
Hospital administrators need to anticipate periods of high resource strain—bed shortages, ICU overflow, oxygen demand spikes—before they happen. This project analyzes two years of patient visit data to identify seasonal and departmental demand patterns, and recommends where capacity planning should be prioritized.

A few real stakeholder questions:
- Which season/month puts the most strain on beds and ICU capacity?
- Are there departments consistently running near capacity?
- Does severity level predict resource usage in a way that could inform early triage/staffing decisions?
- Is there a readmission pattern worth flagging to hospital leadership?

## Plan
1. [Data Cleaning](#data-cleaning-results): will actually do this twice—once in Excel, and once in SQL—to get more practice :) need to check for:
   - duplicates
   - missing values
   - typos
   - outliers
   - data constraints
   - inconsistent text formatting (look for entries that refer to the same thing but are written differently)
   - inconsistent data formatting (dates, phone numbers, etc.)
   - irrelevant data
   - data normalization
2. Exploratory Data Analysis
3. Data Visualizations + Dashboard
4. Come up with insights + recommendations

## Data Cleaning Results
### Excel
- **Duplicates:** 75 duplicate rows found and deleted (Data → Remove Duplicates). Went from **5076 rows** to **5001 rows**.
<img width="278" height="148" alt="image" src="https://github.com/user-attachments/assets/e7be0121-57b5-4802-824e-2596da76a84a" />

- **Missing values:** 325 blank cells detected with COUNTBLANK function and highlighted them in red. (Home → Conditional Formatting → New Rule → Format only cells that contain blanks)
   - Checked each column for missing values (Date → Filter):
      - `Gender`: 100
      - `Length_of_Stay`: 50
      - `Oxygen_Units_Used`: 100
      - `Department`: 75
      - All other columns contained no missing values.
