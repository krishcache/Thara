# Bookmaster.md

# IBM Bookmaster ERP Knowledge Base
**Elsevier Australia – Supply Chain & Inventory Management**

Version: 1.0  
Owner: Krishna Kumar  
Status: Living Document

---

# 1. Purpose

This document serves as the complete functional and technical reference for the IBM Bookmaster ERP system used by Elsevier Australia.

It documents:

- Bookmaster report navigation
- Report catalogue
- Report extraction methods
- Business field mappings
- Report parameters
- Operational business rules
- Data transfer process
- Silent extraction framework
- Report frequencies
- Report ownership

This document intentionally excludes ORION architecture, application development, Python code, database design, APIs, automation logic and UI development. Those are maintained separately in ORION.md.

---

# 2. Scope

This document covers only the Bookmaster reporting environment used by Elsevier Australia Supply Chain.

Included:

- Report navigation
- Screen hierarchy
- Report catalogue
- Report mappings
- Data Transfer
- Report parameters
- Business usage
- Extraction standards

Excluded:

- ORION architecture
- Flask application
- Python source code
- Scheduler configuration
- Database schema
- Dashboard UI
- Future application development

---

# 3. System Overview

Bookmaster is Elsevier Australia's core ERP system used for inventory management, purchasing, POD operations, warehouse management and operational reporting.

The system runs on IBM i (AS/400) and is accessed using IBM Access Client Solutions (ACS).

Bookmaster reports are extracted through the IBM Data Transfer utility into Excel format and subsequently processed by ORION.

---

# 4. Navigation Structure

Bookmaster reports are organised into operational screens.

Primary navigation screens used by Elsevier Australia:

- Screen 52 – Elsevier Demand Management
- Screen 53 – Elsevier Operations
- Screen 54 – Elsevier Customer Service
- Screen 90 – Elsevier Demand Management II

These four screens contain all operational reports currently required by the Australia Inventory Management team.

---

# 5. Bookmaster Report Summary

Total Reports Reviewed : 60

| Status | Count |
|---------|------:|
| Active | 51 |
| Parked | 2 |
| Ignored | 7 |

Only the 51 Active reports form part of the standard Bookmaster extraction framework.

---

# 6. Document Conventions

Throughout this document:

**BM Display Name**
: Name displayed inside Bookmaster menus.

**Actual Report Number**
: Actual report used for IBM Data Transfer extraction.

When they differ, the Actual Report Number always takes precedence.

Example:

BM Display Name

Sales To Inv 2 (E0016)

Actual Extract Report

E0016A

---

# 7. Report Classification

Reports are classified into the following business groups.

- Inventory
- Purchasing
- POD
- Warehouse
- Customer Service
- Freight
- Pricing
- Sales
- Forecasting
- Master Data
- KPI
- Operational Analysis

---

# 8. Report Status Definitions

## Active

Report is currently used operationally and forms part of the standard extraction framework.

## Parked

Report has future business value but is currently excluded from implementation.

## Ignored

Report is obsolete, display-only or outside the current operational scope.

---

# 9. Navigation Screens

The following sections document every report available within Screens 52, 53, 54 and 90.

```
# 10. Screen 52 – Elsevier Demand Management

| Option | BM Display Name | Actual Extract Report | Status | Category |
|--------:|-----------------|----------------------|--------|----------|
| 1 | FORECASTING - Receipts | E0012 | Active | Forecasting |
| 3 | TRANSACTIONS LOCAL | E0013A | Active | KPI |
| 4 | TRANSACTIONS DIST | E0013A | Active | KPI |
| 5 | SALES TO INV 1 | E0015 | Active | Sales |
| 6 | SALES TO INV 2 | E0016A | Active | Sales |
| 7 | Backorders $ | EOM96A | Active | Inventory |
| 8 | First Fill Rate | E00112A | Active | KPI |
| 9 | Warehouse Data | E00113 | Active | Warehouse |
| 10 | ISBN13 | E00114 | Active | Master Data |
| 11 | Stock Movement Returns | E00115 | Active | Inventory |
| 12 | Purchase Order | E00116 | Active | Purchasing |
| 14 | OTO Report | E00123A | Active | Operations |
| 23 | LLP Replenishment | EOM38E5 | Active | Inventory |
| 24 | B/O This Period | E00118 | Active | Inventory |
| 25 | POD EDI Rejected PO's | PODREJ | Ignored | POD |
| 26 | Sales Customer By ISBN | E00002 | Active | Sales |
| 27 | FORECASTING - Receipts (AIR) | E0012B | Active | Forecasting |
| 30 | POD Customer Transactions | E00046 | Active | POD |
| 31 | POD Orders | E00047 | Active | POD |

---

# 11. Screen 53 – Elsevier Operations

| Option | BM Display Name | Actual Extract Report | Status | Category |
|--------:|-----------------|----------------------|--------|----------|
| 14 | Held POD Orders | Pending (Ana Replacement Report) | Parked | POD |
| 40 | HS AUD Prices | EOM92 | Active | Pricing |
| 41 | S&T AUD Price File | EOM92A | Active | Pricing |
| 42 | HS NZD Prices | EOM92B | Active | Pricing |
| 43 | S&T NZD Prices | EOM92C | Active | Pricing |
| 44 | HS + S&T AUD Prices | EOM92E | Ignored | Pricing |

---

# 12. Screen 54 – Elsevier Customer Service

| Option | BM Display Name | Actual Extract Report | Status | Category |
|--------:|-----------------|----------------------|--------|----------|
| 5 | OP Report | EOD06A | Active | Customer Service |
| 12 | OS Report | E00103 | Active | Customer Service |
| 13 | Unapproved | E00110 | Active | Customer Service |

---

# 13. Screen 90 – Elsevier Demand Management II

| Option | BM Display Name | Actual Extract Report | Status | Category |
|--------:|-----------------|----------------------|--------|----------|
| 7 | Shrinkwrap Report | EOD12 | Active | Operations |
| 8 | Purchase Orders | E00031A | Active | Purchasing |
| 9 | NYP Order Report | NYP Order Report | Active | Publishing |
| 11 | PO Details | E00082 | Active | Purchasing |
| 12 | O/S PO's POD | E00082A | Active | POD |
| 55 | Backorder & Fwd Order Summary | Backorder & Fwd Order Summary | Active | Inventory |
| 59 | STK Analysis Corp | EOM701C | Ignored | Inventory |
| 60 | STK Analysis HS | EOM70C | Active | Inventory |
| 65 | Value Of Orders Placed Air | Value Of Orders Placed Air | Ignored | Purchasing |
| 71 | Freight Calc | E00075 | Active | Freight |
| 72 | Freight Calc Detail | E00075A | Active | Freight |
| 76 | Warehouse 0005 | ELSEVIER/E00094 (Display Only) | Ignored | Warehouse |
| 78 | Title Listing | E00102 | Active | Master Data |
| 81 | POD TAT | E00106A | Ignored | POD |
| 82 | Number of Units in a PO | Number of Units in a PO | Ignored | Purchasing |
| 84 | Titles Stock On Hand | E00120B | Active | Inventory |
| 85 | Publication Date Report | E00102A | Active | Publishing |
| 86 | Title Master File | E00124 | Active | Master Data |
| 87 | SOHQ by Location (Ligare4) | LIGARE4 | Active | Warehouse |
| 88 | Stock POD Titles | E00120C | Active | POD |
| 89 | Slow Moving Stock | SLOWSTK2 | Active | Inventory |
| 100 | Shipment Details Ligare | Shipment Details Ligare | Parked | Warehouse |
# 14. Report Dictionary

Every report documented in this knowledge base follows the standard template below.

---

## Standard Report Template

### Report Information

| Field | Description |
|-------|-------------|
| Screen | Bookmaster Screen Number |
| Menu Option | Menu Option Number |
| BM Display Name | Name displayed in Bookmaster |
| Actual Extract Report | Report used during Data Transfer extraction |
| Classification | Inventory / POD / KPI / Purchasing / Freight etc. |
| Status | Active / Parked / Ignored |
| Frequency | Daily / Weekly / Monthly / On Demand |
| Parameters | Required user inputs before extraction |
| Output Format | Excel |
| Business Owner | Inventory Management |
| Used By | Business process / Dashboard / KPI |

---

# 15. Report Parameters

Bookmaster reports require different parameter types before execution.

| Parameter Type | Example |
|---------------|---------|
| None | Master reports |
| Accounting Period | KPI Reports |
| Date | Daily Reports |
| Date Range | Monthly Reports |
| Warehouse | Warehouse Reports |
| Shipment Number | Shipment Reports |
| Purchase Order | Purchasing Reports |
| ISBN | Inventory Lookup |
| Customer | Customer Reports |
| Supplier | Purchasing Reports |

---

# 16. Report Extraction Standards

## Standard Extraction Process

```
Bookmaster

↓

Navigate to Report

↓

Enter Parameters

↓

Run Report

↓

IBM Data Transfer

↓

Excel

↓

Shared Drive
```

---

## Silent Extraction Process

Future ORION automation follows the same process without user interaction.

```
Bookmaster

↓

ODBC

↓

SQL

↓

Excel

↓

Shared Drive

↓

Dashboard
```

---

## Data Transfer Rules

- Always use the Actual Extract Report number.
- IBM Data Transfer is the standard extraction method.
- Historical files must never be overwritten.
- Excel is the standard output format.
- Preserve original report structure wherever possible.

---

# 17. Report Frequency Standards

| Frequency | Typical Usage |
|-----------|---------------|
| Hourly | Automated monitoring |
| Daily | Operational reports |
| Weekly | Management reports |
| Monthly | KPI reporting |
| Quarterly | Business review |
| On Demand | Investigation / Ad-hoc |

Actual frequencies are maintained against each report.

---

# 18. Report Categories

## Inventory

Stock analysis and inventory reporting.

Examples

- E00120B
- SLOWSTK2
- E00115
- E00118

---

## POD

Print-on-Demand reporting.

Examples

- E00046
- E00047
- E00082A
- E00120C

---

## Purchasing

Purchase order management.

Examples

- E00116
- E00031A
- E00082

---

## Warehouse

Warehouse operations.

Examples

- LIGARE4
- E00113

---

## Freight

Shipment and freight reporting.

Examples

- E00075
- E00075A

---

## Pricing

Price maintenance.

Examples

- EOM92
- EOM92A
- EOM92B
- EOM92C

---

## Customer Service

Customer order management.

Examples

- EOD06A
- E00103
- E00110

---

## KPI

Business performance reporting.

Examples

- E0013A
- E00112A

---

## Forecasting

Forecast reports.

Examples

- E0012
- E0012B

---

## Master Data

Reference and title master reports.

Examples

- E00114
- E00124
- E00102
# 19. Business Rules

## General Rules

- Bookmaster is the official System of Record.
- Actual Extract Report Number always takes precedence over the BM display report number.
- Historical report extracts must never be overwritten.
- Standard output format is Microsoft Excel (.xlsx).
- Shared Drive is the operational repository for all report outputs.
- Report structures should remain unchanged unless business-approved.

---

## Parameter Rules

- Use Date parameters for transaction reports.
- Use Accounting Period for KPI reports.
- Use Shipment Number for shipment reports.
- Use Purchase Order Number for purchasing reports.
- Use Warehouse parameter where applicable.
- Use ISBN only for title-specific lookups.

---

## Extraction Rules

- Execute the report before initiating IBM Data Transfer.
- Verify report parameters prior to extraction.
- Preserve original data types wherever possible.
- Convert date columns to standard business format after extraction.
- Maintain consistent file naming standards.

---

## File Naming Standards

General Format

```
<ReportName>_YYYYMMDD.xlsx
```

Examples

```
E00046_20260725.xlsx

E00120B_20260725.xlsx

LIGARE4_20260725.xlsx
```

Automated Extracts

```
<ReportName>_YYYYMMDD_HHMMSS.xlsx
```

Example

```
LIGARE4_20260725_081243.xlsx
```

---

# 20. Silent Extraction Framework

The ORION extraction engine performs silent report extraction using IBM i Access ODBC without requiring manual interaction.

General flow

```
Scheduler

↓

Python

↓

IBM i Access ODBC

↓

Bookmaster Database

↓

SQL Query

↓

Excel Export

↓

Shared Drive

↓

Dashboard
```

Current silent extraction supports repeatable report execution and timestamped output generation.

---

# 21. Active Reports

Total Active Reports

**51**

These reports form the supported Bookmaster operational reporting framework.

Future sections should document each report individually using the standard Report Dictionary template.

---

# 22. Parked Reports

| Report | Reason |
|---------|--------|
| Held POD Orders | Awaiting replacement report from Ana Mendes |
| Shipment Details Ligare | Planned for future warehouse automation using Shipment ID |

These reports remain part of the long-term roadmap but are excluded from the current implementation.

---

# 23. Ignored Reports

| Report | Reason |
|---------|--------|
| POD EDI Rejected PO's (PODREJ) | No longer required |
| HS + S&T AUD Prices (EOM92E) | Outside operational scope |
| POD TAT (E00106A) | Legacy report using Griffin supplier |
| Number of Units in a PO | Business not using |
| STK Analysis Corp (EOM701C) | No longer used |
| Value Of Orders Placed Air | Not required |
| Warehouse 0005 (ELSEVIER/E00094) | Display screen only |

These reports are intentionally excluded from the operational extraction framework.

---

# 24. Appendix

## Screen Hierarchy

```
Bookmaster

├── Screen 52
│      Elsevier Demand Management
│
├── Screen 53
│      Elsevier Operations
│
├── Screen 54
│      Elsevier Customer Service
│
└── Screen 90
       Elsevier Demand Management II
```

---

## Report Inventory Summary

```
Total Reports Reviewed      : 60

Active Reports              : 51

Parked Reports              : 2

Ignored Reports             : 7
```

---

## Future Expansion

The following information will be added progressively as business knowledge expands:

- Complete field mappings
- Sample report outputs
- Screen captures
- Report parameter examples
- SQL mappings
- ORION extraction IDs
- Data Transfer templates
- Business process references

---

**End of Document**
# 25. Development Notes

> This section documents business-facing extraction standards only.
> ORION implementation, source code and application architecture are maintained separately in **ORION.md**.

---

## Silent Extraction Philosophy

The objective of silent extraction is to remove manual intervention while preserving the business behaviour of Bookmaster.

The extraction process must replicate the standard IBM Data Transfer workflow without altering report content.

---

## Extraction Principles

- Bookmaster remains the System of Record.
- No business logic should be duplicated outside Bookmaster.
- Reports should be extracted exactly as produced by Bookmaster.
- Automation must never modify source data.
- Automation should only read, extract and store report outputs.

---

## Output Repository

All extracted reports should be stored under the standard BookMaster folder structure.

Example

```
BookMaster

├── Daily
├── Weekly
├── Monthly
├── Hourly
├── Archive
└── Scripts
```

---

## Output Standards

Every automated extract should include:

- Report Name
- Timestamp
- Original report structure
- Standard Excel formatting

Historical outputs should always be retained.

---

# 26. Known Business Exceptions

## Legacy Reports

Some reports continue to exist within Bookmaster but are no longer used operationally.

Examples include:

- Griffin-related reports
- Legacy pricing reports
- Display-only screens
- Historical warehouse reports

These remain documented for reference purposes only.

---

## Menu Report Number vs Extract Report Number

Several Bookmaster menu options display one report number while IBM Data Transfer requires another report number.

Example

| BM Menu | Actual Extract |
|---------|----------------|
| SALES TO INV 2 (E0016) | E0016A |
| TRANSACTIONS DIST (E0013B) | E0013A |

Always use the **Actual Extract Report** documented in this knowledge base.

---

# 27. Maintenance Guidelines

Whenever a new Bookmaster report is introduced:

1. Add the report to the appropriate screen.
2. Record the BM Display Name.
3. Record the Actual Extract Report Number.
4. Classify the report.
5. Record required parameters.
6. Record extraction frequency.
7. Record business purpose.
8. Mark the report as:
   - Active
   - Parked
   - Ignored

---

Whenever an existing report changes:

- Update the report dictionary.
- Update field mappings.
- Update parameter requirements.
- Update extraction notes.
- Update ORION mappings if applicable.

---

# 28. Change Log

| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0 | Jul-2026 | Krishna Kumar | Initial Bookmaster knowledge base created. |
| 1.x | TBD | Krishna Kumar | Report dictionary expansion. |
| Future | TBD | Krishna Kumar | Complete field mappings and extraction examples. |

---

# 29. Roadmap

## Phase 1

- Complete report inventory
- Navigation trees
- Report catalogue

## Phase 2

- Complete report dictionary for all Active reports

## Phase 3

- Complete business field mappings

## Phase 4

- Add screenshots for every report

## Phase 5

- Link report outputs with ORION report IDs

## Phase 6

- Complete warehouse and operational references

---

# 30. Completion Status

| Area | Status |
|------|--------|
| Navigation | ✅ Complete |
| Report Inventory | ✅ Complete |
| Report Classification | ✅ Complete |
| Active / Parked / Ignored | ✅ Complete |
| Business Rules | ✅ Complete |
| Extraction Standards | ✅ Complete |
| Silent Extraction Standards | ✅ Complete |
| Field Mappings | ⏳ In Progress |
| Report Dictionary | ⏳ In Progress |
| Screen Images | ⏳ In Progress |
| Sample Outputs | ⏳ In Progress |

---

**End of Bookmaster.md**
