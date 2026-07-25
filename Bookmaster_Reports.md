# Bookmaster_Reports.md

# IBM Bookmaster Report Knowledge Base
**Elsevier Australia – Report Catalogue & Extraction Guide**

Version: 1.0  
Owner: Krishna Kumar  
Status: Living Document

---

# Purpose

This document contains the detailed documentation for every operational Bookmaster report used by Elsevier Australia.

Each report documents:

- Business purpose
- Navigation path
- Menu option
- BM Display Name
- Actual Extract Report
- Parameters
- Extraction route
- Output folder
- Naming convention
- Frequency
- Business notes
- Related reports
- Automation status

This document is the operational reference for both manual and automated report extraction.

---

# Relationship

Refer to **Bookmaster.md** for:

- Bookmaster overview
- Navigation hierarchy
- Business rules
- Report classification
- Active / Parked / Ignored summary
- ERP knowledge

---

# Report Documentation Standard

Every report follows the same structure.

---

## Report Information

| Field | Value |
|------|------|
| Screen | |
| Menu Option | |
| BM Display Name | |
| Actual Extract Report | |
| Category | |
| Status | |
| Frequency | |
| Parameters | |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Describe why the report exists and how the business uses it.

---

## Navigation

Bookmaster

↓

Screen

↓

Menu Option

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Execute Report

↓

IBM Data Transfer

↓

Actual Extract Report

↓

Excel

↓

Destination Folder

---

## Parameters

Document every required input.

Examples:

- Accounting Period
- Date
- Date Range
- Shipment Number
- Purchase Order
- ISBN
- Warehouse
- Customer
- Supplier

---

## Destination Folder

Record the standard destination folder.

Examples

Daily

Weekly

Monthly

Hourly

Archive

---

## File Naming Convention

Examples

```
E00046_YYYYMMDD.xlsx

LIGARE4_YYYYMMDD_HHMMSS.xlsx
```

---

## Automation Status

Manual

Supported

Automated

Production

---

## Business Notes

Business-specific observations.

---

## Related Reports

Document reports that are commonly used together.

---

# Report Index

## Screen 52

31. E0012
32. E0012B
33. E0013A
34. E0015
35. E0016A
36. EOM96A
37. E00112A
38. E00113
39. E00114
40. E00115
41. E00116
42. E00123A
43. EOM38E5
44. E00118
45. E00002
46. E00046
47. E00047

---

## Screen 53

48. EOM92
49. EOM92A
50. EOM92B
51. EOM92C

---

## Screen 54

52. EOD06A
53. E00103
54. E00110

---

## Screen 90

55. EOD12
56. E00031A
57. NYP Order Report
58. E00082
59. E00082A
60. Backorder & Fwd Order Summary
61. EOM70C
62. E00075
63. E00075A
64. E00102
65. E00102A
66. E00124
67. LIGARE4
68. E00120C
69. SLOWSTK2
70. E00120B

---

# Future Reports

Append all newly introduced Bookmaster reports below without renumbering existing reports.

71.

72.

73.

74.

75.

...

---

**End of Framework**

The following sections (31 onwards) will contain one complete page for each report using the standard structure defined above.
# 31. E0012 – FORECASTING - Receipts

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 1 |
| BM Display Name | FORECASTING - Receipts |
| Actual Extract Report | E0012 |
| Category | Forecasting |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Forecast receipts into the warehouse.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 1

↓

FORECASTING - Receipts

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E0012
```

↓

Excel

↓

Destination Folder

```
Monthly
```

---

## Parameters

To be documented.

---

## Destination Folder

```
BookMaster\Monthly
```

---

## File Naming Convention

```
E0012_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

To be documented.

---

## Related Reports

- E0012B
- E00113
- E00118

---

# 32. E0012B – FORECASTING - Receipts (AIR)

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 27 |
| BM Display Name | FORECASTING - Receipts (AIR) |
| Actual Extract Report | E0012B |
| Category | Forecasting |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Forecast receipts for Air Freight orders.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 27

↓

FORECASTING - Receipts (AIR)

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E0012B
```

↓

Excel

↓

Destination Folder

```
Monthly
```

---

## Parameters

To be documented.

---

## Destination Folder

```
BookMaster\Monthly
```

---

## File Naming Convention

```
E0012B_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

To be documented.

---

## Related Reports

- E0012
- E00118
```
# 33. E0013A – TRANSACTIONS LOCAL

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 3 |
| BM Display Name | TRANSACTIONS LOCAL |
| Actual Extract Report | E0013A |
| Category | KPI |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Transaction report for local inventory movements.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 3

↓

TRANSACTIONS LOCAL

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E0013A
```

↓

Excel

↓

Destination Folder

```
Monthly
```

---

## Parameters

To be documented.

---

## Destination Folder

```
BookMaster\Monthly
```

---

## File Naming Convention

```
E0013A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Same extract report is also used by **TRANSACTIONS DIST**.

---

## Related Reports

- TRANSACTIONS DIST
- E00112A
- E00115

---

# 34. E0015 – SALES TO INV 1

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 5 |
| BM Display Name | SALES TO INV 1 |
| Actual Extract Report | E0015 |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Sales to Inventory reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 5

↓

SALES TO INV 1

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E0015
```

↓

Excel

↓

Destination Folder

```
Monthly
```

---

## Parameters

To be documented.

---

## Destination Folder

```
BookMaster\Monthly
```

---

## File Naming Convention

```
E0015_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

To be documented.

---

## Related Reports

- E0016A
- E0013A

---

# 35. E0016A – SALES TO INV 2

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 6 |
| BM Display Name | SALES TO INV 2 |
| Actual Extract Report | E0016A |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Sales to Inventory reporting (Part 2).

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 6

↓

SALES TO INV 2

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E0016A
```

↓

Excel

↓

Destination Folder

```
Monthly
```

---

## Parameters

To be documented.

---

## Destination Folder

```
BookMaster\Monthly
```

---

## File Naming Convention

```
E0016A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Bookmaster menu displays **E0016**.

IBM Data Transfer extraction uses **E0016A**.

Always use **E0016A** for automation.

---

## Related Reports

- E0015
- E0013A
# 36. EOM96A – Backorders $

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 7 |
| BM Display Name | Backorders $ |
| Actual Extract Report | EOM96A |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides the dollar value of current backorders.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 7

↓

Backorders $

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM96A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM96A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used for inventory backlog monitoring.

---

## Related Reports

- E00118
- E00112A

---

# 37. E00112A – First Fill Rate

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 8 |
| BM Display Name | First Fill Rate |
| Actual Extract Report | E00112A |
| Category | KPI |
| Status | Active |
| Frequency | Monthly |
| Parameters | Accounting Period |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Measures first fill rate performance for inventory KPI reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 8

↓

First Fill Rate

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Enter Accounting Period

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00112A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

Accounting Period

Example

```
202607
```

---

## File Naming Convention

```
E00112A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary KPI report for Fill Rate calculations.

---

## Related Reports

- E0013A
- EOM96A

---

# 38. E00113 – Warehouse Data

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 9 |
| BM Display Name | Warehouse Data |
| Actual Extract Report | E00113 |
| Category | Warehouse |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Warehouse operational reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 9

↓

Warehouse Data

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00113
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00113_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports warehouse operational analysis.

---

## Related Reports

- LIGARE4
- E00120B# 36. EOM96A – Backorders $

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 7 |
| BM Display Name | Backorders $ |
| Actual Extract Report | EOM96A |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides the dollar value of current backorders.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 7

↓

Backorders $

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM96A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM96A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used for inventory backlog monitoring.

---

## Related Reports

- E00118
- E00112A

---

# 37. E00112A – First Fill Rate

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 8 |
| BM Display Name | First Fill Rate |
| Actual Extract Report | E00112A |
| Category | KPI |
| Status | Active |
| Frequency | Monthly |
| Parameters | Accounting Period |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Measures first fill rate performance for inventory KPI reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 8

↓

First Fill Rate

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Enter Accounting Period

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00112A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

Accounting Period

Example

```
202607
```

---

## File Naming Convention

```
E00112A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary KPI report for Fill Rate calculations.

---

## Related Reports

- E0013A
- EOM96A

---

# 38. E00113 – Warehouse Data

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 9 |
| BM Display Name | Warehouse Data |
| Actual Extract Report | E00113 |
| Category | Warehouse |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Warehouse operational reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 9

↓

Warehouse Data

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00113
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00113_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports warehouse operational analysis.

---

## Related Reports

- LIGARE4
# 36. EOM96A – Backorders $

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 7 |
| BM Display Name | Backorders $ |
| Actual Extract Report | EOM96A |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides the dollar value of current backorders.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 7

↓

Backorders $

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM96A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM96A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used for inventory backlog monitoring.

---

## Related Reports

- E00118
- E00112A

---

# 37. E00112A – First Fill Rate

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 8 |
| BM Display Name | First Fill Rate |
| Actual Extract Report | E00112A |
| Category | KPI |
| Status | Active |
| Frequency | Monthly |
| Parameters | Accounting Period |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Measures first fill rate performance for inventory KPI reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 8

↓

First Fill Rate

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Enter Accounting Period

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00112A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

Accounting Period

Example

```
202607
```

---

## File Naming Convention

```
E00112A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary KPI report for Fill Rate calculations.

---

## Related Reports

- E0013A
- EOM96A

---

# 38. E00113 – Warehouse Data

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 9 |
| BM Display Name | Warehouse Data |
| Actual Extract Report | E00113 |
| Category | Warehouse |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Warehouse operational reporting.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 9

↓

Warehouse Data

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00113
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00113_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports warehouse operational analysis.

---

## Related Reports

- LIGARE4
- E00120B
# 39. E00114 – ISBN13

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 10 |
| BM Display Name | ISBN13 |
| Actual Extract Report | E00114 |
| Category | Master Data |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides ISBN-13 reference information for Bookmaster titles.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 10

↓

ISBN13

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00114
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00114_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Reference report used for title master information.

---

## Related Reports

- E00124
- E00102

---

# 40. E00115 – Stock Movement Returns

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 11 |
| BM Display Name | Stock Movement Returns |
| Actual Extract Report | E00115 |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Reports inventory stock movements and returns.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 11

↓

Stock Movement Returns

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00115
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00115_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports inventory movement reconciliation.

---

## Related Reports

- E00118
- E00113

---

# 41. E00116 – Purchase Order

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 12 |
| BM Display Name | Purchase Order |
| Actual Extract Report | E00116 |
| Category | Purchasing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Purchase order reporting for inventory replenishment.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 12

↓

Purchase Order

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00116
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00116_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used for purchase planning and supplier order review.

---

## Related Reports

- E00031A
- E00082
- E00082A

---

# 42. E00123A – OTO Report

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 14 |
| BM Display Name | OTO Report |
| Actual Extract Report | E00123A |
| Category | Operations |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Operational reporting for Order-to-Order activities.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 14

↓

OTO Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00123A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00123A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports operational order analysis.

---

## Related Reports

- E00116
- E00082
# 43. EOM38E5 – LLP Replenishment

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 23 |
| BM Display Name | LLP Replenishment |
| Actual Extract Report | EOM38E5 |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Supports replenishment planning for LLP inventory.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 23

↓

LLP Replenishment

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM38E5
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM38E5_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports LLP replenishment planning.

---

## Related Reports

- E00116
- E00118

---

# 44. E00118 – B/O This Period

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 24 |
| BM Display Name | B/O This Period |
| Actual Extract Report | E00118 |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Parameters | Accounting Period |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Lists backorders created during the selected accounting period.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 24

↓

B/O This Period

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Enter Accounting Period

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00118
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

Accounting Period

---

## File Naming Convention

```
E00118_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used during monthly inventory review and KPI reporting.

---

## Related Reports

- EOM96A
- E00112A

---

# 45. E00002 – Sales Customer By ISBN

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 26 |
| BM Display Name | Sales Customer By ISBN |
| Actual Extract Report | E00002 |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides customer sales information by ISBN.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 26

↓

Sales Customer By ISBN

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00002
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00002_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Useful for customer-specific sales analysis.

---

## Related Reports

- E0015
- E0016A

---

# 46. E00046 – POD Customer Transactions

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 30 |
| BM Display Name | POD Cust Trans |
| Actual Extract Report | E00046 |
| Category | POD |
| Status | Active |
| Frequency | Daily |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Primary transaction report for Print-on-Demand customer orders.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 30

↓

POD Cust Trans

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00046
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00046_YYYYMMDD.xlsx
```

---

## Automation Status

Production

---

## Business Notes

Primary source for POD transaction history.

Mapped extensively within ORION.

---

## Related Reports

- E00047
- E00082A

- E00120B
# 47. E00047 – POD Orders

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 31 |
| BM Display Name | POD Orders |
| Actual Extract Report | E00047 |
| Category | POD |
| Status | Active |
| Frequency | Daily |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Primary operational report containing all Print-on-Demand purchase orders created within Bookmaster.

---

## Navigation

Bookmaster

↓

Screen 52

↓

Option 31

↓

POD Orders

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00047
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00047_YYYYMMDD.xlsx
```

---

## Automation Status

Production

---

## Business Notes

Primary report used for POD operational monitoring.

Contains supplier information, customer information, order dates and POD order details.

Forms one of the core reports used by ORION.

---

## Related Reports

- E00046
- E00082A
- LIGARE4

---

# 48. EOM92 – HS AUD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 40 |
| BM Display Name | HS AUD Prices |
| Actual Extract Report | EOM92 |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Price list for Higher Education titles in Australian Dollars.

---

## Navigation

Bookmaster

↓

Screen 53

↓

Option 40

↓

HS AUD Prices

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM92
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM92_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Pricing reference report.

---

## Related Reports

- EOM92A
- EOM92B
- EOM92C

---

# 49. EOM92A – S&T AUD Price File

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 41 |
| BM Display Name | S&T AUD Price File |
| Actual Extract Report | EOM92A |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Price list for Science & Technology titles in Australian Dollars.

---

## Navigation

Bookmaster

↓

Screen 53

↓

Option 41

↓

S&T AUD Price File

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM92A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM92A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Pricing reference report.

---

## Related Reports

- EOM92
- EOM92B
- EOM92C

---

# 50. EOM92B – HS NZD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 42 |
| BM Display Name | HS NZD Prices |
| Actual Extract Report | EOM92B |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Price list for Higher Education titles in New Zealand Dollars.

---

## Navigation

Bookmaster

↓

Screen 53

↓

Option 42

↓

HS NZD Prices

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM92B
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM92B_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Pricing reference report.

---

## Related Reports

- EOM92
- EOM92A
- EOM92C

---

# 51. EOM92C – S&T NZD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 43 |
| BM Display Name | S&T NZD Prices |
| Actual Extract Report | EOM92C |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Price list for Science & Technology titles in New Zealand Dollars.

---

## Navigation

Bookmaster

↓

Screen 53

↓

Option 43

↓

S&T NZD Prices

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM92C
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM92C_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Pricing reference report.

---

## Related Reports

- EOM92
- EOM92A
- EOM92B
# 52. EOD06A – OP Report

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 5 |
| BM Display Name | OP Report |
| Actual Extract Report | EOD06A |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Customer Service / Inventory Management |

---

## Business Purpose

Operational report used by Customer Service for order processing and customer enquiries.

---

## Navigation

Bookmaster

↓

Screen 54

↓

Option 5

↓

OP Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOD06A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOD06A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Frequently used by Customer Service for operational monitoring.

---

## Related Reports

- E00103
- E00110

---

# 53. E00103 – OS Report

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 12 |
| BM Display Name | OS Report |
| Actual Extract Report | E00103 |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Customer Service / Inventory Management |

---

## Business Purpose

Outstanding customer order report.

---

## Navigation

Bookmaster

↓

Screen 54

↓

Option 12

↓

OS Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00103
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00103_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports Customer Service follow-up of outstanding orders.

---

## Related Reports

- EOD06A
- E00110

---

# 54. E00110 – Unapproved

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 13 |
| BM Display Name | Unapproved |
| Actual Extract Report | E00110 |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Customer Service / Inventory Management |

---

## Business Purpose

Lists orders awaiting approval before further processing.

---

## Navigation

Bookmaster

↓

Screen 54

↓

Option 13

↓

Unapproved

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00110
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00110_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used to identify orders pending approval.

---

## Related Reports

- EOD06A
- E00103

---

# 55. EOD12 – Shrinkwrap Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 7 |
| BM Display Name | Shrinkwrap Report |
| Actual Extract Report | EOD12 |
| Category | Operations |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Operational report for shrinkwrap requirements and processing.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 7

↓

Shrinkwrap Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOD12
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOD12_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports warehouse operational activities.

---

## Related Reports

- E00031A
- E00082
# 56. E00031A – Purchase Orders

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 8 |
| BM Display Name | Purchase Orders |
| Actual Extract Report | E00031A |
| Category | Purchasing |
| Status | Active |
| Frequency | Daily |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides purchase order information for all active supplier purchase orders.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 8

↓

Purchase Orders

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00031A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00031A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary purchasing report for supplier order monitoring.

---

## Related Reports

- E00082
- E00082A
- E00116

---

# 57. NYP Order Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 9 |
| BM Display Name | NYP Order Report |
| Actual Extract Report | NYP Order Report |
| Category | Publishing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Lists customer orders for titles that are Not Yet Published (NYP).

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 9

↓

NYP Order Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
NYP Order Report
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
NYP_Order_Report_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports publication planning and customer order visibility before publication.

---

## Related Reports

- E00102A
- E00124

---

# 58. E00082 – PO Details

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 11 |
| BM Display Name | PO Details |
| Actual Extract Report | E00082 |
| Category | Purchasing |
| Status | Active |
| Frequency | Daily |
| Parameters | Purchase Order |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides detailed information for individual purchase orders.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 11

↓

PO Details

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Enter Purchase Order

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00082
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

Purchase Order Number

---

## File Naming Convention

```
E00082_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Provides line-level purchase order details.

---

## Related Reports

- E00031A
- E00082A

---

# 59. E00082A – O/S PO's POD

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 12 |
| BM Display Name | O/S PO's POD |
| Actual Extract Report | E00082A |
| Category | POD |
| Status | Active |
| Frequency | Daily |
| Parameters | None |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Primary report containing all outstanding POD purchase orders awaiting fulfilment.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 12

↓

O/S PO's POD

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00082A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

None

---

## File Naming Convention

```
E00082A_YYYYMMDD.xlsx
```

---

## Automation Status

Production

---

## Business Notes

Core operational report for POD order monitoring.

One of the primary reports used by ORION.

---

## Related Reports

- E00046
- E00047
- E00082
- LIGARE4

---

# 60. Backorder & Fwd Order Summary

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 55 |
| BM Display Name | Backorder & Fwd Order Summary |
| Actual Extract Report | Backorder & Fwd Order Summary |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Summarises current backorders and forward orders for inventory review.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 55

↓

Backorder & Fwd Order Summary

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
Backorder & Fwd Order Summary
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
Backorder_Forward_Order_Summary_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Management summary report for inventory backorders and future demand.

---

## Related Reports

- E00118
- EOM96A
# 61. EOM70C – STK Analysis HS

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 60 |
| BM Display Name | STK Analysis HS |
| Actual Extract Report | EOM70C |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides inventory stock analysis for Higher Education (HS) titles.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 60

↓

STK Analysis HS

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
EOM70C
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
EOM70C_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used during inventory planning and stock analysis.

---

## Related Reports

- E00120B
- SLOWSTK2

---

# 62. E00075 – Freight Calc

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 71 |
| BM Display Name | Freight Calc |
| Actual Extract Report | E00075 |
| Category | Freight |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Calculates estimated freight costs for shipments.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 71

↓

Freight Calc

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00075
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00075_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports freight estimation before shipment booking.

---

## Related Reports

- E00075A

---

# 63. E00075A – Freight Calc Detail

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 72 |
| BM Display Name | Freight Calc Detail |
| Actual Extract Report | E00075A |
| Category | Freight |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Detailed freight calculation report.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 72

↓

Freight Calc Detail

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00075A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00075A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Detailed version of Freight Calc.

---

## Related Reports

- E00075

---

# 64. E00102 – Title Listing

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 78 |
| BM Display Name | Title Listing |
| Actual Extract Report | E00102 |
| Category | Master Data |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Master listing of titles maintained within Bookmaster.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 78

↓

Title Listing

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00102
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00102_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Reference report for title master data.

---

## Related Reports

- E00124
- E00114
# 65. E00102A – Publication Date Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 85 |
| BM Display Name | Publication Date Report |
| Actual Extract Report | E00102A |
| Category | Publishing |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides publication dates for titles maintained within Bookmaster.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 85

↓

Publication Date Report

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00102A
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00102A_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Used to identify publication dates for inventory planning and purchasing.

---

## Related Reports

- E00102
- E00124
- NYP Order Report

---

# 66. E00124 – Title Master File

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 86 |
| BM Display Name | Title Master File |
| Actual Extract Report | E00124 |
| Category | Master Data |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Master file containing bibliographic and inventory attributes for all titles.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 86

↓

Title Master File

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00124
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00124_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary reference report for title master information.

---

## Related Reports

- E00102
- E00114
- E00102A

---

# 67. LIGARE4 – SOHQ by Location

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 87 |
| BM Display Name | SOHQ by Location |
| Actual Extract Report | LIGARE4 |
| Category | Warehouse |
| Status | Active |
| Frequency | Hourly (Automation) |
| Parameters | None |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Stock On Hand Quantity by warehouse location.

Primary warehouse inventory report used for operational stock visibility.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 87

↓

SOHQ by Location

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
LIGARE4
```

↓

Excel

↓

Destination Folder

```
BookMaster\Hourly
```

---

## Parameters

No parameters required.

---

## File Naming Convention

Manual

```
LIGARE4_YYYYMMDD.xlsx
```

Automation

```
LIGARE4_YYYYMMDD_HHMMSS.xlsx
```

---

## Automation Status

Production

Runs automatically through Windows Task Scheduler using the ORION extraction framework.

---

## Business Notes

Current production automation extracts this report silently at scheduled intervals.

Primary warehouse stock report used by ORION.

---

## Related Reports

- E00113
- E00120B
- E00082A
- E00047

---

# 68. E00120C – Stock POD Titles

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 88 |
| BM Display Name | Stock POD Titles |
| Actual Extract Report | E00120C |
| Category | POD |
| Status | Active |
| Frequency | As Required |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Lists POD titles currently held in stock.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 88

↓

Stock POD Titles

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00120C
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00120C_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports POD stock analysis and planning.

---

## Related Reports

- E00046
- E00047
- LIGARE4
# 69. SLOWSTK2 – Slow Moving Stock

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 89 |
| BM Display Name | Slow Moving Stock |
| Actual Extract Report | SLOWSTK2 |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Identifies slow-moving inventory for stock optimization, purchasing decisions and inventory review.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 89

↓

Slow Moving Stock

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
SLOWSTK2
```

↓

Excel

↓

Destination Folder

```
BookMaster\Monthly
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
SLOWSTK2_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Supports inventory ageing analysis and purchasing decisions.

Frequently used during inventory review and slow-moving stock exercises.

---

## Related Reports

- EOM70C
- E00120B
- LIGARE4

---

# 70. E00120B – Titles Stock On Hand

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 84 |
| BM Display Name | Titles Stock On Hand |
| Actual Extract Report | E00120B |
| Category | Inventory |
| Status | Active |
| Frequency | Daily |
| Parameters | Refer to Bookmaster |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides current stock on hand by title.

Used for inventory planning, purchasing, stock verification and operational reporting.

---

## Navigation

Bookmaster

↓

Screen 90

↓

Option 84

↓

Titles Stock On Hand

↓

Run Report

---

## Extraction Route

Bookmaster

↓

Run Report

↓

IBM Data Transfer

↓

Report Name

```
E00120B
```

↓

Excel

↓

Destination Folder

```
BookMaster\Daily
```

---

## Parameters

To be documented.

---

## File Naming Convention

```
E00120B_YYYYMMDD.xlsx
```

---

## Automation Status

Supported

---

## Business Notes

Primary inventory stock report for title-level stock visibility.

Often used together with LIGARE4 to compare warehouse stock against title stock.

Supports purchasing, replenishment and inventory analysis.

---

## Related Reports

- LIGARE4
- SLOWSTK2
- EOM70C
- E00113

---

# Future Reports

All newly introduced Bookmaster reports should be appended below without renumbering existing reports.

## 71.

Report Name

Status

Pending Documentation

---

## 72.

Report Name

Status

Pending Documentation

---

## 73.

Report Name

Status

Pending Documentation

---

## 74.

Report Name

Status

Pending Documentation

---

## 75.

Report Name

Status

Pending Documentation

---

(Continue numbering sequentially as new reports are introduced.)

---

**End of Bookmaster_Reports.md**
