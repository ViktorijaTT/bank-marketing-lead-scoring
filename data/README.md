# Data: Bank Marketing (with social and economic context)

## Source and licence

- **File:** `bank-additional-full.csv` (41,188 rows, 21 columns, semicolon separated, rows in date order from May 2008 to November 2010). The official notes are in `bank-additional-names.txt`.
- **Origin:** Real direct-marketing (telephone) campaigns of a Portuguese retail bank. The economic indicators were added from Banco de Portugal statistics.
- **Source:** UCI Machine Learning Repository, "Bank Marketing" (dataset 222).
- **Licence:** Creative Commons Attribution 4.0 International (CC BY 4.0).
- **Citation:** Moro, S., Cortez, P., Rita, P. (2014). A data-driven approach to predict the success of bank telemarketing. *Decision Support Systems*, 62, 22-31. https://doi.org/10.1016/j.dss.2014.03.001

## Data dictionary

Missing values are coded with the text `unknown`. There is no year column.

| Column | Type | Description |
|---|---|---|
| `age` | number | Age of the client, in years |
| `job` | text | Type of job: admin., blue-collar, entrepreneur, housemaid, management, retired, self-employed, services, student, technician, unemployed, unknown |
| `marital` | text | Marital status: divorced (includes widowed), married, single, unknown |
| `education` | text | basic.4y, basic.6y, basic.9y, high.school, illiterate, professional.course, university.degree, unknown |
| `default` | text | Has credit in default? yes, no, unknown |
| `housing` | text | Has a housing loan? yes, no, unknown |
| `loan` | text | Has a personal loan? yes, no, unknown |
| `contact` | text | Contact type: cellular or telephone |
| `month` | text | Month of the last contact in the campaign (jan to dec) |
| `day_of_week` | text | Day of the last contact (mon to fri) |
| `duration` | number | Length of the last call, in seconds. **Known only after the call; the outcome is also known then. Excluded from the lead score.** |
| `campaign` | number | Number of contacts made to this client in this campaign, including the last one |
| `pdays` | number | Days since the client was last contacted in a previous campaign; 999 means never contacted before |
| `previous` | number | Number of contacts made to this client before this campaign |
| `poutcome` | text | Outcome of the previous campaign: failure, nonexistent, success |
| `emp.var.rate` | number | Employment variation rate (quarterly indicator) |
| `cons.price.idx` | number | Consumer price index (monthly indicator) |
| `cons.conf.idx` | number | Consumer confidence index (monthly indicator) |
| `euribor3m` | number | Euribor 3-month interest rate (daily indicator) |
| `nr.employed` | number | Number of employees (quarterly indicator) |
| `y` | text | Target: did the client subscribe a term deposit? yes or no |

Notebooks add two derived columns in memory (the file is not changed): `subscribed` (1 for yes, 0 for no) and `contacted_before` (no where `pdays` is 999, yes otherwise).
