# Bookmaster_Reports.md

# IBM Bookmaster Reports
### Elsevier Australia – Operational Report Catalogue

Version: 2.0  
Document Owner: Krishna Kumar  
Status: Active  
Last Updated: Jul-2026

---

# Purpose

This document serves as the operational reference for all IBM Bookmaster reports used by Elsevier Australia.

It documents:

- Report information
- Business purpose
- Bookmaster navigation
- Typical report input
- Destination staging folder
- File naming convention
- Business notes

The objective is to provide a quick operational reference for manually running reports and supporting future automation through ORION.

---

# Relationship

This document should be read together with the following knowledge bases.

| Document | Purpose |
|----------|---------|
| Bookmaster.md | IBM Bookmaster application overview, menus, screens and business processes |
| ORION.md | Silent extraction framework, automation, Python, VBS, Scheduler, SQL and ETL logic |

---

# Standard Report Extraction Process

Unless otherwise specified, every Bookmaster report follows the same extraction process.

Bookmaster

↓

Navigate to the required Screen

↓

Select the required Menu Option

↓

Enter the required report input (if applicable)

↓

Run Report

↓

IBM Data Transfer

↓

Export to Microsoft Excel

↓

Save into the designated Staging Folder

---

# Report Staging Strategy

The extracted reports are **not** intended for permanent storage.

Instead, they are stored temporarily in dedicated staging folders based on business frequency.

The staging folders act as an intermediate layer between IBM Bookmaster and downstream ORION automation.

---

## Staging Folder Structure

| Folder | Purpose |
|---------|---------|
| Daily | Reports extracted once per day |
| Weekly | Reports extracted weekly |
| Monthly | Reports extracted once per accounting period |
| Continuous | Operational reports extracted multiple times throughout the day or on-demand |
| Archive *(Future)* | Long-term storage if required |

---

## Staging Workflow

IBM Bookmaster

↓

Report Extraction

↓

Staging Folder

↓

ORION Processing

↓

Database / Dashboard

↓

Delete Processed Report

---

## Staging Behaviour

- Reports are temporarily stored in their designated staging folders.
- ORION reads reports from the staging folders according to the scheduled frequency.
- Processed data is appended or updated in the destination database.
- Successfully processed report files are automatically deleted.
- Staging folders should only contain reports awaiting processing.

---

# File Naming Convention

All extracted reports shall follow the standard naming convention.

```
<ReportName>_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00046_25-Jul-26_091530.xlsx
```

This format is designed for easy human readability while remaining unique for automation.

---

# Report Input Standards

Typical report inputs currently used within Bookmaster.

| Input Type | Example | Description |
|------------|---------|-------------|
| Accounting Period | `202606` | Single accounting period |
| Date Range | `2026-06-01 2026-06-30` | From Date → To Date |
| Same Period | `202606 202606` | From Period → To Period (Single Month) |
| Period Range | `202507 202606` | From Period → To Period (Multiple Months) |
| No Input | `None` | Report executes without user input |

The values above represent the **typical** inputs entered when running the report.

Specific report input requirements are documented within each report section.

---

# Report Catalogue
# Report Catalogue

## Screen 52 – Inventory Reports

| No. | BM Report | Actual Extract Report | Report Name | Category | Default Staging Folder |
|----:|-----------|-----------------------|-------------|----------|------------------------|
| 31 | E0012 | E0012 | FORECASTING - Receipts | Forecasting | Monthly |
| 32 | E0012B | E0012B | FORECASTING - Receipts (AIR) | Forecasting | Monthly |
| 33 | E0013A | E0013A | TRANSACTIONS LOCAL | Inventory | Monthly |
| 34 | E0015 | E0015 | SALES TO INV 1 | Sales | Monthly |
| 35 | E0016 | E0016A | SALES TO INV 2 | Sales | Monthly |
| 36 | EOM96A | EOM96A | Backorders $ | Inventory | Monthly |
| 37 | E00112A | E00112A | First Fill Rate | KPI | Monthly |
| 38 | E00113 | E00113 | Warehouse Data | Inventory | Monthly |
| 39 | E00114 | E00114 | ISBN13 | Master Data | Monthly |
| 40 | E00115 | E00115 | Stock Mvmt Returns | Inventory | Monthly |
| 41 | E00116 | E00116 | Purchase Order | Purchasing | Monthly |
| 42 | E00123A | E00123A | OTO Report | Operations | Monthly |
| 43 | EOM38E5 | EOM38E5 | LLP Replenishment | Inventory | Monthly |
| 44 | E00118 | E00118 | B/O This Period | Inventory | Monthly |
| 45 | E00002 | E00002 | Sales Customer By ISBN | Sales | Monthly |
| 46 | E00046 | E00046 | POD Customer Transactions | POD | Monthly |
| 47 | E00047 | E00047 | POD Orders | POD | Monthly |

---

## Screen 53 – Pricing Reports

| No. | BM Report | Actual Extract Report | Report Name | Category | Default Staging Folder |
|----:|-----------|-----------------------|-------------|----------|------------------------|
| 48 | EOM92 | EOM92 | HS AUD Prices | Pricing | Monthly |
| 49 | EOM92A | EOM92A | S&T AUD Price File | Pricing | Monthly |
| 50 | EOM92B | EOM92B | HS NZD Prices | Pricing | Monthly |
| 51 | EOM92C | EOM92C | S&T NZD Prices | Pricing | Monthly |

---

## Screen 54 – Customer Service Reports

| No. | BM Report | Actual Extract Report | Report Name | Category | Default Staging Folder |
|----:|-----------|-----------------------|-------------|----------|------------------------|
| 52 | EOD06A | EOD06A | OP Report | Customer Service | Monthly |
| 53 | E00103 | E00103 | OS Report | Customer Service | Monthly |
| 54 | E00110 | E00110 | Unapproved | Customer Service | Monthly |

---

## Screen 90 – Operations & Warehouse Reports

| No. | BM Report | Actual Extract Report | Report Name | Category | Default Staging Folder |
|----:|-----------|-----------------------|-------------|----------|------------------------|
| 55 | EOD12 | EOD12 | Shrinkwrap Report | Operations | Monthly |
| 56 | E00031A | E00031A | Purchase Orders | Purchasing | Monthly |
| 57 | NYP Order Report | NYP Order Report | NYP Order Report | Publishing | Monthly |
| 58 | E00082 | E00082 | PO Details | Purchasing | Monthly |
| 59 | E00082A | E00082A | O/S PO's POD | POD | Weekly |
| 60 | Backorder & Fwd Order Summary | Backorder & Fwd Order Summary | Backorder & Fwd Order Summary | Inventory | Monthly |
| 61 | EOM70C | EOM70C | STK Analysis HS | Inventory | Monthly |
| 62 | E00075 | E00075 | Freight Calc | Freight | Continuous |
| 63 | E00075A | E00075A | Freight Calc Detail | Freight | Continuous |
| 64 | E00102 | E00102 | Title Listing | Master Data | Monthly |
| 65 | E00102A | E00102A | Publication Date Report | Publishing | Monthly |
| 66 | E00124 | E00124 | Title Master File | Master Data | Weekly |
| 67 | LIGARE4 | LIGARE4 | SOHQ by Location | Warehouse | Daily *(Planned)* |
| 68 | E00120C | E00120C | Stock POD Titles | POD | Weekly |
| 69 | SLOWSTK2 | SLOWSTK2 | Slow Moving Stock | Inventory | Monthly |
| 70 | E00120B | E00120B | Titles Stock On Hand | Inventory | Monthly |

---
# 31. E0012 – FORECASTING - Receipts

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 1 |
| BM Report | E0012 |
| Actual Extract Report | E0012 |
| Category | Forecasting |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Forecast incoming warehouse receipts for purchasing and inventory planning.

---

## Navigation

```
52 → 1
```

---

## Report Input

```
2026-06-01 2026-06-30
```

Example

```
01-Jun-2026 to 30-Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E0012_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E0012_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used during monthly purchasing and inventory forecasting.

---

# 32. E0012B – FORECASTING - Receipts (AIR)

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 27 |
| BM Report | E0012B |
| Actual Extract Report | E0012B |
| Category | Forecasting |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Forecast incoming Air Freight receipts for purchasing and inventory planning.

---

## Navigation

```
52 → 27
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E0012B_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E0012B_30-Jun-26_091530.xlsx
```

---

## Business Notes

Specialised forecasting report for Air Freight receipts.

---

# 33. E0013A – TRANSACTIONS LOCAL

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 3 |
| BM Report | E0013A |
| Actual Extract Report | E0013A |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides local inventory transaction history for reconciliation and operational analysis.

---

## Navigation

```
52 → 3
```

---

## Report Input

```
202606 202606
```

Example

```
From Jun-2026 to Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E0013A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E0013A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to analyse local inventory transactions for the selected accounting period.

---
# 34. E0015 – SALES TO INV 1

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 5 |
| BM Report | E0015 |
| Actual Extract Report | E0015 |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Sales to Inventory analysis for the selected accounting period.

---

## Navigation

```
52 → 5
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E0015_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E0015_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for monthly Sales versus Inventory analysis.

---

# 35. E0016 – SALES TO INV 2

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 6 |
| BM Report | E0016 |
| Actual Extract Report | E0016A |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Continuation of the Sales to Inventory reporting used for inventory planning and sales analysis.

---

## Navigation

```
52 → 6
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E0016A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E0016A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Bookmaster report is **E0016**, while IBM Data Transfer extracts **E0016A**.

---

# 36. EOM96A – Backorders $

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 7 |
| BM Report | EOM96A |
| Actual Extract Report | EOM96A |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides the total customer backorder value for the selected accounting period.

---

## Navigation

```
52 → 7
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM96A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM96A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for monthly management reporting and inventory review.

---
# 37. E00112A – First Fill Rate

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 8 |
| BM Report | E00112A |
| Actual Extract Report | E00112A |
| Category | KPI |
| Status | Active |
| Frequency | Monthly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Measures the First Fill Rate KPI for the selected reporting period.

Used for monthly inventory performance reporting and management review.

---

## Navigation

```
52 → 8
```

---

## Report Input

```
2026-06-01 2026-06-30
```

Example

```
01-Jun-2026 to 30-Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00112A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00112A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Primary KPI report used to measure First Fill Rate performance.

---

# 38. E00113 – Warehouse Data

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 9 |
| BM Report | E00113 |
| Actual Extract Report | E00113 |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides warehouse operational data for inventory analysis and reconciliation.

---

## Navigation

```
52 → 9
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00113_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00113_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports warehouse inventory analysis and operational reporting.

---

# 39. E00114 – ISBN13

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 10 |
| BM Report | E00114 |
| Actual Extract Report | E00114 |
| Category | Master Data |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides ISBN-13 reference information for title master data validation.

---

## Navigation

```
52 → 10
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00114_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00114_30-Jun-26_091530.xlsx
```

---

## Business Notes

Reference report used for title master data verification.

---

# 40. E00115 – Stock Mvmt Returns

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 11 |
| BM Report | E00115 |
| Actual Extract Report | E00115 |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides stock movement and returns information for inventory reconciliation and analysis.

---

## Navigation

```
52 → 11
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00115_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00115_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to analyse stock movements and returns for the selected accounting period.

---
# 41. E00116 – Purchase Order

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 12 |
| BM Report | E00116 |
| Actual Extract Report | E00116 |
| Category | Purchasing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Purchase Order information for purchasing activities and inventory replenishment.

---

## Navigation

```
52 → 12
```

---

## Report Input

```
2026-06-01 2026-06-30
```

Example

```
01-Jun-2026 to 30-Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00116_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00116_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for Purchase Order monitoring and inventory replenishment.

---

# 42. E00123A – OTO Report

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 14 |
| BM Report | E00123A |
| Actual Extract Report | E00123A |
| Category | Operations |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides operational reporting for Order-to-Order (OTO) activities.

---

## Navigation

```
52 → 14
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00123A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00123A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports operational reporting and internal business analysis.

---

# 43. EOM38E5 – LLP Replenishment

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 23 |
| BM Report | EOM38E5 |
| Actual Extract Report | EOM38E5 |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Supports LLP inventory replenishment planning.

---

## Navigation

```
52 → 23
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM38E5_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM38E5_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to determine LLP replenishment requirements.

---

# 44. E00118 – B/O This Period

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 24 |
| BM Report | E00118 |
| Actual Extract Report | E00118 |
| Category | Inventory |
| Status | Active |
| Frequency | Monthly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides customer backorders created during the selected accounting period.

---

## Navigation

```
52 → 24
```

---

## Report Input

```
202606
```

Example

```
Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00118_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00118_30-Jun-26_091530.xlsx
```

---

## Business Notes

Monthly backorder report used for inventory planning and management reporting.

---
# 45. E00002 – Sales Customer By ISBN

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 26 |
| BM Report | E00002 |
| Actual Extract Report | E00002 |
| Category | Sales |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides customer sales information by ISBN for sales analysis and inventory planning.

---

## Navigation

```
52 → 26
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00002_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00002_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for customer sales analysis by ISBN.

---

# 46. E00046 – POD Customer Transactions

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 30 |
| BM Report | E00046 |
| Actual Extract Report | E00046 |
| Category | POD |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides POD customer transaction history for operational analysis and POD reporting.

---

## Navigation

```
52 → 30
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00046_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00046_30-Jun-26_091530.xlsx
```

---

## Business Notes

Primary source for POD customer transaction data used by ORION.

---

# 47. E00047 – POD Orders

## Report Information

| Field | Value |
|------|------|
| Screen | 52 |
| Menu Option | 31 |
| BM Report | E00047 |
| Actual Extract Report | E00047 |
| Category | POD |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides POD order details for operational monitoring and POD dashboard reporting.

---

## Navigation

```
52 → 31
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00047_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00047_30-Jun-26_091530.xlsx
```

---

## Business Notes

Primary source for POD order information used by ORION and the POD Control Center.

---
# 48. EOM92 – HS AUD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 1 |
| BM Report | EOM92 |
| Actual Extract Report | EOM92 |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Higher Education AUD price data.

---

## Navigation

```
53 → 1
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM92_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM92_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for Higher Education pricing reference.

---

# 49. EOM92A – S&T AUD Price File

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 2 |
| BM Report | EOM92A |
| Actual Extract Report | EOM92A |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Science & Technology AUD price file.

---

## Navigation

```
53 → 2
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM92A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM92A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used as the AUD pricing reference for Science & Technology titles.

---

# 50. EOM92B – HS NZD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 3 |
| BM Report | EOM92B |
| Actual Extract Report | EOM92B |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Higher Education NZD price data.

---

## Navigation

```
53 → 3
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM92B_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM92B_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for Higher Education NZD pricing reference.

---

# 51. EOM92C – S&T NZD Prices

## Report Information

| Field | Value |
|------|------|
| Screen | 53 |
| Menu Option | 4 |
| BM Report | EOM92C |
| Actual Extract Report | EOM92C |
| Category | Pricing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Science & Technology NZD price data.

---

## Navigation

```
53 → 4
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM92C_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM92C_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used as the NZD pricing reference for Science & Technology titles.

---
# 52. EOD06A – OP Report

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 1 |
| BM Report | EOD06A |
| Actual Extract Report | EOD06A |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Customer Service |

---

## Business Purpose

Provides the OP Report for Customer Service operations.

---

## Navigation

```
54 → 1
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOD06A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOD06A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used by Customer Service for operational reporting.

---

# 53. E00103 – OS Report

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 2 |
| BM Report | E00103 |
| Actual Extract Report | E00103 |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Customer Service |

---

## Business Purpose

Provides the OS Report for Customer Service operations.

---

## Navigation

```
54 → 2
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00103_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00103_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports Customer Service operational monitoring.

---

# 54. E00110 – Unapproved

## Report Information

| Field | Value |
|------|------|
| Screen | 54 |
| Menu Option | 3 |
| BM Report | E00110 |
| Actual Extract Report | E00110 |
| Category | Customer Service |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Customer Service |

---

## Business Purpose

Lists unapproved transactions requiring review.

---

## Navigation

```
54 → 3
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00110_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00110_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to identify records pending approval.

---
# 55. EOD12 – Shrinkwrap Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 1 |
| BM Report | EOD12 |
| Actual Extract Report | EOD12 |
| Category | Operations |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides shrinkwrap requirements for warehouse operations.

---

## Navigation

```
90 → 1
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOD12_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOD12_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports warehouse packaging operations.

---

# 56. E00031A – Purchase Orders

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 2 |
| BM Report | E00031A |
| Actual Extract Report | E00031A |
| Category | Purchasing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Purchase Order information for purchasing activities.

---

## Navigation

```
90 → 2
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00031A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00031A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used for Purchase Order monitoring and procurement activities.

---

# 57. NYP Order Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 3 |
| BM Report | NYP Order Report |
| Actual Extract Report | NYP Order Report |
| Category | Publishing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides New Publication (NYP) order information.

---

## Navigation

```
90 → 3
```

---

## Report Input

```
202507 202606
```

Example

```
From Jul-2025 to Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
NYP_Order_Report_dd-MMM-yy_HHmmss.xlsx
```

Example

```
NYP_Order_Report_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports monitoring of New Publication orders across multiple accounting periods.

---

# 58. E00082 – PO Details

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 4 |
| BM Report | E00082 |
| Actual Extract Report | E00082 |
| Category | Purchasing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides detailed Purchase Order information.

---

## Navigation

```
90 → 4
```

---

## Report Input

```
202606 202606
```

Example

```
From Jun-2026 to Jun-2026
```

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00082_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00082_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to review Purchase Order details for the selected accounting period.

---
# 59. E00082A – O/S PO's POD

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 5 |
| BM Report | E00082A |
| Actual Extract Report | E00082A |
| Category | POD |
| Status | Active |
| Frequency | Weekly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides outstanding POD Purchase Orders awaiting fulfilment.

---

## Navigation

```
90 → 5
```

---

## Report Input

```
202606 202606
```

Example

```
From Jun-2026 to Jun-2026
```

---

## Destination Staging Folder

Weekly

---

## File Naming Convention

```
E00082A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00082A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Primary report for monitoring outstanding POD Purchase Orders.

---

# 60. Backorder & Fwd Order Summary

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 6 |
| BM Report | Backorder & Fwd Order Summary |
| Actual Extract Report | Backorder & Fwd Order Summary |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Summarises customer backorders and forward orders.

---

## Navigation

```
90 → 6
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
Backorder_Fwd_Order_Summary_dd-MMM-yy_HHmmss.xlsx
```

Example

```
Backorder_Fwd_Order_Summary_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to review customer backorders and forward order commitments.

---

# 61. EOM70C – STK Analysis HS

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 7 |
| BM Report | EOM70C |
| Actual Extract Report | EOM70C |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Higher Education stock analysis for inventory review.

---

## Navigation

```
90 → 7
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
EOM70C_dd-MMM-yy_HHmmss.xlsx
```

Example

```
EOM70C_30-Jun-26_091530.xlsx
```

---

## Business Notes

Supports Higher Education inventory analysis.

---

# 62. E00075 – Freight Calc

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 8 |
| BM Report | E00075 |
| Actual Extract Report | E00075 |
| Category | Freight |
| Status | Active |
| Frequency | On Demand |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Calculates freight charges for shipments.

---

## Navigation

```
90 → 8
```

---

## Report Input

None

---

## Destination Staging Folder

Continuous

---

## File Naming Convention

```
E00075_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00075_30-Jun-26_091530.xlsx
```

---

## Business Notes

Operational report used throughout the day for freight calculations.

---
# 63. E00075A – Freight Calc Detail

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 9 |
| BM Report | E00075A |
| Actual Extract Report | E00075A |
| Category | Freight |
| Status | Active |
| Frequency | On Demand |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides detailed freight calculation information for shipment analysis.

---

## Navigation

```
90 → 9
```

---

## Report Input

None

---

## Destination Staging Folder

Continuous

---

## File Naming Convention

```
E00075A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00075A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Detailed operational freight report used throughout the day.

---

# 64. E00102 – Title Listing

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 10 |
| BM Report | E00102 |
| Actual Extract Report | E00102 |
| Category | Master Data |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides title listing information for master data validation.

---

## Navigation

```
90 → 10
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00102_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00102_30-Jun-26_091530.xlsx
```

---

## Business Notes

Used to review title master information.

---

# 65. E00102A – Publication Date Report

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 11 |
| BM Report | E00102A |
| Actual Extract Report | E00102A |
| Category | Publishing |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides publication date information for titles.

---

## Navigation

```
90 → 11
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00102A_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00102A_30-Jun-26_091530.xlsx
```

---

## Business Notes

Reference report for publication date validation.

---

# 66. E00124 – Title Master File

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 12 |
| BM Report | E00124 |
| Actual Extract Report | E00124 |
| Category | Master Data |
| Status | Active |
| Frequency | Weekly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides the latest Title Master data.

---

## Navigation

```
90 → 12
```

---

## Report Input

None

---

## Destination Staging Folder

Weekly

---

## File Naming Convention

```
E00124_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00124_30-Jun-26_091530.xlsx
```

---

## Business Notes

Weekly snapshot used to capture and maintain Title Master data.

---
# 67. LIGARE4 – SOHQ by Location

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 13 |
| BM Report | LIGARE4 |
| Actual Extract Report | LIGARE4 |
| Category | Warehouse |
| Status | Active |
| Frequency | Daily *(Currently Hourly during ORION testing)* |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Stock On Hand Quantity (SOHQ) by warehouse location.

---

## Navigation

```
90 → 13
```

---

## Report Input

None

---

## Destination Staging Folder

Daily

---

## File Naming Convention

```
LIGARE4_dd-MMM-yy_HHmmss.xlsx
```

Example

```
LIGARE4_30-Jun-26_091530.xlsx
```

---

## Business Notes

- Currently extracted every 5 minutes during ORION testing.
- Planned to run once daily after Amazon and Booktopia automation is implemented.
- Primary warehouse stock report for Ligare inventory.

---

# 68. E00120C – Stock POD Titles

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 14 |
| BM Report | E00120C |
| Actual Extract Report | E00120C |
| Category | POD |
| Status | Active |
| Frequency | Weekly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Stock On Hand details for POD titles.

---

## Navigation

```
90 → 14
```

---

## Report Input

None

---

## Destination Staging Folder

Weekly

---

## File Naming Convention

```
E00120C_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00120C_30-Jun-26_091530.xlsx
```

---

## Business Notes

Weekly snapshot used to monitor POD stock availability.

---

# 69. SLOWSTK2 – Slow Moving Stock

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 15 |
| BM Report | SLOWSTK2 |
| Actual Extract Report | SLOWSTK2 |
| Category | Inventory |
| Status | Active |
| Frequency | Weekly |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Identifies slow moving inventory based on historical sales.

---

## Navigation

```
90 → 15
```

---

## Report Input

None

---

## Destination Staging Folder

Weekly

---

## File Naming Convention

```
SLOWSTK2_dd-MMM-yy_HHmmss.xlsx
```

Example

```
SLOWSTK2_30-Jun-26_091530.xlsx
```

---

## Business Notes

Weekly inventory review report used for stock optimisation and ageing analysis.

---

# 70. E00120B – Titles Stock On Hand

## Report Information

| Field | Value |
|------|------|
| Screen | 90 |
| Menu Option | 16 |
| BM Report | E00120B |
| Actual Extract Report | E00120B |
| Category | Inventory |
| Status | Active |
| Frequency | As Required |
| Output Format | Excel |
| Business Owner | Inventory Management |

---

## Business Purpose

Provides Stock On Hand information for all inventory titles.

---

## Navigation

```
90 → 16
```

---

## Report Input

None

---

## Destination Staging Folder

Monthly

---

## File Naming Convention

```
E00120B_dd-MMM-yy_HHmmss.xlsx
```

Example

```
E00120B_30-Jun-26_091530.xlsx
```

---

## Business Notes

Primary Stock On Hand report used for inventory review and reconciliation.

---
# Future Reports

This section is reserved for future IBM Bookmaster reports that are introduced after the initial implementation of ORION.

New reports should follow the standard documentation template defined in this document.

---

# Revision History

| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0 | Jul-2026 | Krishna Kumar | Initial Bookmaster report catalogue created. |
| 2.0 | Jul-2026 | Krishna Kumar | Complete redesign of the document with simplified report structure, staging strategy and standardized report template. |

---

# Change Log

## Version 2.0

### Added

- Standard Report Extraction Process
- Report Staging Strategy
- Staging Folder Structure
- Report Catalogue
- Standard Report Template
- Report Input Standards
- Standard File Naming Convention

### Updated

- Simplified report documentation structure.
- Added Actual Extract Report to Report Information.
- Standardized Navigation format.
- Standardized Report Input section.
- Introduced Destination Staging Folder.
- Standardized File Naming Convention.

### Removed

- Automation Compatibility
- Expected Runtime
- Completion Check
- Known Issues
- Automation Notes
- Automation Status
- Related Reports

Automation-specific implementation has been moved to **ORION.md**.

---

# Future Enhancements

The following enhancements are planned for future versions of this document.

- Additional Bookmaster reports.
- Report screenshots.
- Sample report outputs.
- Cross-reference to Bookmaster.md.
- Cross-reference to ORION.md.
- Default ORION report schedules.
- Report ownership matrix.
- Business process mapping.
- Data dictionary for each report.

---

**End of Document**
