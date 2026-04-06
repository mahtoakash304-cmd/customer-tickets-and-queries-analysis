# paste.txt (Support Tickets Dataset)

This file is a **tab-separated** dataset of customer support tickets.

## What it contains

Each row represents one ticket with timestamps, classification fields (category, priority, product, channel), operational metrics (first response and resolution time), and outcomes (CSAT, reopened).

## Quick KPIs 

| Metric | Value |
|---|---:|
| Tickets | 1000 |
| Avg first response (hrs) | 3.116 |
| Median first response (hrs) | 3.0 |
| Avg resolution (hrs) | 26.513 |
| Median resolution (hrs) | 23.2 |
| Avg CSAT (1-5) | 3.589 |
| Reopen rate | 6.0% |

| column             |   non_null |   unique | example_values                                                |
|:-------------------|-----------:|---------:|:--------------------------------------------------------------|
| s no.              |       1000 |     1000 | 1, 2, 3                                                       |
| Ticket_ID          |       1000 |     1000 | TKT-00001, TKT-00002, TKT-00003                               |
| Created_At         |       1000 |      998 | 2024-07-25 14:12:00, 2024-11-09 17:13:00, 2024-09-27 18:49:00 |
| Category           |       1000 |        8 | Refund Request, Technical Issue, Billing Issue                |
| z                  |       1000 |        5 | Email, Chat, Phone                                            |
| Priority           |       1000 |        4 | Low, High, Low                                                |
| Product            |       1000 |       10 | Tablet, Earphones, Smartphone                                 |
| Agent              |       1000 |       10 | Ravi Kumar, Arjun Singh, Divya Joshi                          |
| First_Response_Hrs |       1000 |       56 | 1.6, 0.8, 1.6                                                 |
| Resolution_Hrs     |       1000 |      483 | 44.9, 4.1, 31.8                                               |
| Resolved_At        |       1000 |     1000 | 2024-07-27 11:05:00, 2024-11-09 21:18:00, 2024-09-29 02:34:00 |
| Status             |       1000 |        4 | Closed, Resolved, Resolved                                    |
| CSAT_Score         |       1000 |        5 | 5, 4, 5                                                       |
| Reopened           |       1000 |        2 | No, No, No                                                    |
| Month              |       1000 |       12 | Jul, Nov, Sep                                                 |
| Month_Num          |       1000 |       12 | 7, 11, 9                                                      |
| Hour               |       1000 |       13 | 14, 17, 18                                                    |
| Day_of_Week        |       1000 |        7 | Thursday, Saturday, Friday                                    |
| Created_Date       |       1000 |      348 | 2024-07-25, 2024-11-09, 2024-09-27                            |
| Created_Month      |       1000 |       12 | 2024-07, 2024-11, 2024-09                                     |
| Created_DOW        |       1000 |        7 | Thursday, Saturday, Friday                                    | 


```text
s no.	Ticket_ID	Created_At	Category	z	Priority	Product	Agent	First_Response_Hrs	Resolution_Hrs	Resolved_At	Status	CSAT_Score	Reopened	Month	Month_Num	Hour	Day_of_Week
1	TKT-00001	2024-07-25 14:12:00	Refund Request	Email	Low	Tablet	Ravi Kumar	1.6	44.9	2024-07-27 11:05:00	Closed	5	No	Jul	7	14	Thursday
2	TKT-00002	2024-11-09 17:13:00	Technical Issue	Chat	High	Earphones	Arjun Singh	0.8	4.1	2024-11-09 21:18:00	Resolved	4	No	Nov	11	17	Saturday
3	TKT-00003	2024-09-27 18:49:00	Billing Issue	Phone	Low	Smartphone	Divya Joshi	1.6	31.8	2024-09-29 02:34:00	Resolved	5	No	Sep	9	18	Friday
4	TKT-00004	2024-08-24 08:22:00	Billing Issue	Social Media	High	Speaker	Karan Mehta	1.5	9.4	2024-08-24 17:44:00	Resolved	4	No	Aug	8	8	Saturday
5	TKT-00005	2024-02-26 08:10:00	Product Defect	WhatsApp	Low	Laptop	Sunita Ver
```


```python
import pandas as pd
support_df = pd.read_csv('paste.txt', sep='	')
```
