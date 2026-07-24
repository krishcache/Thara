# Elsevier Australia - Enterprise Operations Knowledge Base

> **Owner:** Krishna Kumar  
> **Business Area:** Elsevier Australia – Supply Chain & Inventory Management  
> **Purpose:** Centralised knowledge base for Elsevier Australia operations, systems, business processes, Bookmaster, warehouse operations, master reference data, and operational documentation.  
> **Status:** Living Document  
> **Repository:** Thara  
> **Version:** 1.0

---

# 1. Overview

## 1.1 Purpose

This document serves as the central knowledge repository for Elsevier Australia Supply Chain & Inventory Management.

It consolidates operational knowledge, business processes, Bookmaster reporting, warehouse operations, supplier information, reference data, logistics processes, and documentation standards into a single reference document.

This document intentionally excludes software architecture and application development. ORION and future software projects are documented separately.

---

## 1.2 Scope

This document covers:

- Elsevier Australia Operations
- Inventory Management
- Purchase Planning
- Bookmaster ERP
- Warehouse Operations
- POD Operations
- Suppliers
- Warehouses
- Forwarders
- Customers
- Logistics
- Business Rules
- Master Reference Data
- Operational Playbooks
- Reporting Standards

The following are documented separately:

- ORION
- Software Architecture
- Python Development
- Scheduler Development
- Database Design
- AI Development

---

## 1.3 Business Overview

Elsevier Australia manages inventory planning, purchasing, warehouse operations, POD (Print on Demand), logistics coordination, and customer fulfilment for the Australian market.

Inventory is sourced globally from multiple printers and suppliers and distributed through Ligare Australia.

Operations include:

- Inventory Planning
- Purchase Planning
- POD Management
- Warehouse Replenishment
- Freight Coordination
- Customer Order Management
- Supplier Management
- Business Reporting
- KPI Reporting
- Inventory Analysis

---

## 1.4 Business Functions

The Inventory Management function supports multiple business areas.

Primary stakeholders include:

- Operations
- Sales
- Content
- Warehousing
- Logistics
- Finance

---

## 1.5 Primary Stakeholders

| Name | Role | Business Area |
|------|------|---------------|
| Gregory Deysel | Operations Manager | Operations |
| Despina Maclaren | Sales Manager | Sales |
| Natalie Hunt | Content Head | Publishing / Content |

Secondary stakeholders:

- Ganesan Murugesan
- Sunita Sundararajan
- Maninderjit Singh

---

# 2. Organisation & Stakeholders

## 2.1 Leadership

| Name | Role | Responsibility |
|------|------|----------------|
| Sunita Sundararajan | Senior Director – Supply Chain Management (Printed Products) | Global Supply Chain Leadership |
| Ganesan Murugesan | Head of Logistics – South Asia & South East Asia | Regional Logistics |
| Gregory Deysel | Operations Manager | Australia & New Zealand Operations |
| Maninderjit Singh | APAC Warehouse Manager | Warehouse Strategy, Budgets, Relocations, Warehouse Mapping |

---

## 2.2 Operations Team

| Name | Role | Responsibility |
|------|------|----------------|
| Gregory Deysel | Operations Manager | AU Operations |
| Ana Mendes | Consultant | Reports & Process Improvements |
| Liz Roberts | Customer Service | Customer Orders & POD |
| Elna Schonfeldt | Customer Service | Customer Orders & POD |
| Brajesh K. Sharma | Inventory Analyst (SEA) | Backup Inventory Analyst |
| Jennifer Simms | Warehouse Operations | AU Warehouse |
| Kathy Tiananga | Warehouse Operations | AU Warehouse |

---

## 2.3 Warehouse Team

| Name | Organisation | Responsibility |
|------|--------------|----------------|
| Susana Marques | Ligare Australia | Warehouse Manager |
| Ligare Elsevier | Ligare Australia | Shared Warehouse Mailbox |

---

## 2.4 Logistics Leadership

| Name | Role |
|------|------|
| Sunita Sundararajan | Senior Director – Supply Chain Management |
| Ganesan Murugesan | Head of Logistics – South Asia & South East Asia |
| Maninderjit Singh | APAC Warehouse Manager |

---

## 2.5 Sales

| Name | Role |
|------|------|
| Despina Maclaren | Sales Manager |

---

## 2.6 Content

| Name | Role |
|------|------|
| Natalie Hunt | Content Head |

---

## 2.7 Contact Directory

### Elsevier Australia

| Name | Email |
|------|-------|
| Gregory Deysel | g.deysel@elsevier.com |
| Ana Mendes | a.mendes@elsevier.com |
| Liz Roberts | Liz.Roberts@elsevier.com |
| Elna Schonfeldt | elna.schonfeldt@elsevier.com |
| Brajesh K. Sharma | b.sharma@elsevier.com |
| Jennifer Simms | j.simms@elsevier.com |
| Kathy Tiananga | k.tiananga@elsevier.com |
| Maninderjit Singh | m.singh.1@elsevier.com |
| Ganesan Murugesan | G.Murugesan@elsevier.com |
| Sunita Sundararajan | S.Sundararajan@elsevier.com |

### Ligare Australia

| Name | Email |
|------|-------|
| Susana Marques | susanam@ligare.com.au |
| Ligare Elsevier | elsevier@ligare.com.au |

---

# 3. Systems Landscape

## 3.1 Core Systems

| System | Purpose |
|---------|---------|
| Bookmaster ERP | Inventory, Purchasing, Orders, POD |
| IBM ACS | Shipment & ASN Reporting |
| SharePoint | Operational Repository |
| Shared Drive | Central Data Repository |
| Amazon Vendor Central | Amazon Inventory & Sales Reports |
| Booktopia PAD | Purchase Advice Data |
| Nielsen Portal | Monthly Sell-through Data |
| DHL Express | Shipment Tracking |

---

## 3.2 External Data Sources

| Source | Owner | Frequency | Storage |
|---------|-------|-----------|---------|
| Bookmaster Reports | Krishna Kumar | Daily / Monthly | Shared Drive |
| IBM ACS | Krishna Kumar | Daily | Shared Drive |
| Amazon Vendor Central | Krishna Kumar | Weekly (Monday) | Shared Drive |
| Booktopia PAD | Email | Daily | Shared Drive |
| Nielsen Sell-through | Elna Schonfeldt | Monthly | Shared Drive |

---

## 3.3 Data Collection Flow

```text
Bookmaster
      │
      ▼
Bookmaster Reports
      │
      ▼
Shared Drive
      ▲
      │
IBM ACS
Amazon Vendor Central
Booktopia PAD
Nielsen Sell-through
      │
      ▼
Operational Reporting
```

# 4. Business Landscape

## 4.1 Suppliers

### Active Suppliers

| Supplier Code | Supplier Name | Type | Country | Notes |
|---------------|---------------|------|---------|------|
| MP009 | Markono Print Media Pte Ltd | POD Printer | Singapore | Used for POD orders |
| MAR03 | Markono Print Media Pte Ltd | Stock Printer | Singapore | Used for regular (non-POD) orders |
| LIGHT | Lightning Source AU | POD Printer | Australia | POD printing |
| REPLIKA | Replika Press Pvt Ltd | Stock Printer | India | General inventory |
| MUL05 | Multivista Global Pvt Ltd | Stock Printer | India | General inventory |
| KUAN | Kuan Press Sdn Bhd | Stock Printer | Malaysia | General inventory |
| RD005 | RR Donnelley Asia Printing | Stock Printer | Asia | General inventory |
| 1010AUD | 1010 Printing International | Stock Printer | China | General inventory |

---

## 4.2 POD Printers

The Australian POD program currently operates with two primary POD printers.

| Supplier | Location | Purpose |
|----------|----------|---------|
| Markono Print Media Pte Ltd | Singapore | POD Printing |
| Lightning Source Australia | Australia | POD Printing |

---

## 4.3 Warehouses

### Physical Warehouses

| Warehouse | Purpose |
|-----------|---------|
| Ligare Australia | Primary 3PL Warehouse |
| Elsevier Australia Office | Operations |
| POD Warehouse (0005) | Print on Demand Inventory |
| Main Warehouse (0001) | General Inventory |

---

### Warehouse Codes

| Code | Description |
|------|-------------|
| 0001 | Main Stock Warehouse |
| 0003 | Corporate / Drop Shipment Warehouse (Inactive) |
| 0005 | POD Warehouse |

---

### Elsevier Warehouse References

| Code | Description |
|------|-------------|
| ELMAS2 | Elsevier UK Warehouse (S&T Titles) |
| ELSUK2 | Elsevier UK Warehouse (HS Titles) |
| ELSUS2 | Elsevier USA Warehouse |

---

## 4.4 Forwarders

### Freight Partners

| Forwarder | Usage |
|------------|------|
| DGF | Air & Sea Freight |
| Publiship | Sea Freight |
| Scan Shipping | Air & Sea Freight |
| DHL Express | Air Freight |
| Team Global | Freight Coordination |
| Future | Legacy / Historical |
| DSV | Proposed Future Forwarder |

---

### Freight Routing

#### Sea Freight

| Origin | Preferred Forwarder |
|---------|--------------------|
| UK | DGF (Default) |
| UK | Publiship |
| UK | Scan Shipping |
| US | Scan Shipping |

---

#### Air Freight

| Origin | Less than 50kg | More than 50kg |
|---------|----------------|----------------|
| UK | DHL Express | DGF |
| US | DGF | DGF |

---

## 4.5 Customers

### Major Customers

| Customer | Notes |
|----------|------|
| Amazon | Major Retail Customer |
| Booktopia | Major Retail Customer |
| Corporate Customers | Reduced significantly following major customer exit |

---

## 4.6 Publishers

Elsevier Australia manages inventory across two major publishing divisions.

| Division | Description |
|----------|-------------|
| HS | Health Sciences |
| S&T | Science & Technology |

---

## 4.7 Inventory Ownership

Inventory is managed across multiple global printers and distributed through Ligare Australia.

Inventory categories include:

- Standard Stock
- POD Inventory
- New Publication Inventory
- Slow Moving Inventory
- Replenishment Inventory

---

# 5. Master Reference Data

## 5.1 Supplier Master

| Code | Supplier | Country | Purpose |
|------|----------|---------|---------|
| MP009 | Markono Print Media | Singapore | POD Orders |
| MAR03 | Markono Print Media | Singapore | Regular Orders |
| LIGHT | Lightning Source AU | Australia | POD Printing |
| REPLIKA | Replika Press | India | Stock Printing |
| MUL05 | Multivista | India | Stock Printing |
| KUAN | Kuan Press | Malaysia | Stock Printing |
| RD005 | RR Donnelley Asia Printing | Asia | Stock Printing |
| 1010AUD | 1010 Printing International | China | Stock Printing |

---

## 5.2 Warehouse Master

| Warehouse | Description |
|-----------|-------------|
| Ligare Australia | Primary 3PL Warehouse |
| Elsevier Australia | Head Office |
| Warehouse 0001 | Main Stock Warehouse |
| Warehouse 0005 | POD Warehouse |
| Warehouse 0003 | Corporate Warehouse (Inactive) |

---

## 5.3 Printer Master

| Printer | Country | Category |
|----------|---------|----------|
| Markono | Singapore | POD / Stock |
| Lightning Source AU | Australia | POD |
| Replika | India | Stock |
| Multivista | India | Stock |
| Kuan Press | Malaysia | Stock |
| RR Donnelley | Asia | Stock |
| 1010 Printing | China | Stock |

---

## 5.4 Freight Accounts

| Mode | Origin | Currency | Billing Account | Shipping Account |
|------|--------|----------|----------------:|-----------------:|
| Sea Freight | UK | GBP | 10240472 | 68017154 |
| Sea Freight | US | USD | 35060660 | 35060663 |
| Air Freight | UK – HS | GBP | 10240472 | 68088533 |
| Air Freight | UK – S&T | USD | 10240472 | 10534924 |
| Air Freight | US | USD | 35060660 | 35060662 |

---

## 5.5 Consignee

**ELSEVIER AUSTRALIA**

Level 9 / 201 Pacific Highway

St Leonards NSW 2065

Australia

**Attention**

Gregory Deysel

Email: g.deysel@elsevier.com

Mobile: +61 403 673 139

---

## 5.6 Delivery Address / Notify Party

**ELSEVIER AUSTRALIA**

c/o Ligare Australia

Unit 3

92–100 Belmore Road

Riverwood NSW 2210

Australia

**Attention**

Susana Marques

Email: susanam@ligare.com.au

Phone: +61 2 9584 7647

Mobile: +61 401 224 055

---

## 5.7 Material Codes

### Material

| Type | GL Code |
|------|---------|
| ELP | 2701-420969-201101-XX0000-XX99999999-0000000-9999-0000-999999 |
| LLP | 2701-120122-120101-CO1199-XX99999999-0000000-0000-0000-999999 |

---

### Freight

| Type | GL Code |
|------|---------|
| ELP | 2701-120122-501106-CO1199-XX99999999-0000000-0000-0000-999999 |
| LLP | 2701-120013-501402-CO1904-XX99999999-1000000-9999-0000-999999 |

---

## 5.8 Purchase Planning Cycles

### Cycle 1

Health Sciences

- 201 / 206

Science & Technology

- 100 / 100

---

### Cycle 2

Health Sciences

- 201 / 206

Science & Technology

- 300 / 401

---

### Cycle 3

Health Sciences

- 201 / 206

Science & Technology

- 403 / 403

---

### Cycle 4

Health Sciences

- 400 / 400

Science & Technology

- 100 / 100

---

### Cycle 5

Health Sciences

- 400 / 400

Science & Technology

- 401 / 401

---

## 5.9 Shared Resources

### Shared Email

Inventory And Shipping AU (ELS)

InventoryAndShippingAU@elsevier.com

---

### Shared Drive

Operations

```
\\elssyddatp001.science.regn.net
```

Shipping & Inventory

```
\\elssyddatp001.science.regn.net
```

---

### SharePoint

```
C:\Users\kk3\OneDrive - Reed Elsevier Group ICO Reed Elsevier Inc\OG-AU Operations - Inventory_Management
```

# 6. Bookmaster

## 6.1 Overview

Bookmaster is the primary ERP system used by Elsevier Australia for Inventory Management, Purchase Planning, Warehouse Operations, Customer Orders, Purchasing and Print-on-Demand (POD).

Most operational reporting is generated through Bookmaster using predefined reports available under the Elsevier menu.

These reports are extracted via the Data Transfer utility and are used for reporting, analysis and downstream automation.

---

## 6.2 Bookmaster Navigation

### Main Report Screens

| Screen | Description |
|---------|-------------|
| 52 | Elsevier Demand Management |
| 90 | Elsevier Demand Management II |
| 53 | Elsevier Operations |
| 54 | Elsevier Customer Service |

---

## 6.3 Report Classification

Reports are classified into the following business categories.

| Classification | Purpose |
|---------------|---------|
| Master | Master Data |
| Transaction | Daily operational transactions |
| KPI | Performance reporting |
| Inventory | Stock analysis |
| POD | Print On Demand |
| Purchasing | Purchase Orders |
| Customer | Customer reporting |
| Freight | Logistics |
| Warehouse | Warehouse operations |
| Pricing | Price maintenance |
| Reference | Lookup reports |

---

## 6.4 Report Catalogue

Refer to **Bookmaster.md** for the complete report catalogue including:

- Screen Number
- Option Number
- BM Report Name
- Actual Extract Report
- Filter Type
- Extraction Frequency
- Status
- Business Purpose

---

## 6.5 Report Extraction

Reports are extracted using Bookmaster Data Transfer.

General extraction flow:

```
Bookmaster Report

↓

Run Report

↓

Data Transfer

↓

Extract

↓

Excel

↓

Shared Drive
```

Some reports require input parameters before extraction.

Typical parameters include:

- Date
- Date Range
- Accounting Period
- Shipment Number
- Purchase Order Number
- Warehouse
- Customer

---

## 6.6 Report Frequencies

Reports generally fall into the following extraction frequencies.

| Frequency | Purpose |
|-----------|---------|
| Daily | Operational reporting |
| Weekly | Business reporting |
| Monthly | KPI reporting |
| Quarterly | Audit / Review |
| On Demand | Investigation |

Actual frequencies are maintained within the Bookmaster Report Catalogue.

---

## 6.7 Business Rules

General Bookmaster business rules.

- Bookmaster is the system of record.
- Report outputs are extracted into Excel.
- Shared Drive acts as the operational repository.
- Report naming should remain consistent.
- Historical reports should not be overwritten.
- Actual extract report numbers take precedence over menu display report numbers.

---

## 6.8 Report Filters

Reports may require one of the following filter types.

| Filter Type | Example |
|-------------|---------|
| None | Master reports |
| Accounting Period | KPI reports |
| Date | Transactions |
| Date Range | Monthly reporting |
| Purchase Order | PO reports |
| Shipment | Shipment reports |
| ISBN | Inventory lookup |
| Customer | Customer reports |

---

## 6.9 Silent Extraction Process

Most reports are designed for repeatable extraction.

General process:

```
Navigate to Report

↓

Enter Parameters

↓

Run Report

↓

Data Transfer

↓

Export

↓

Excel

↓

Shared Drive
```

Future automation will replicate this process without manual intervention.

---

## 6.10 Data Repository

All operational reports are stored within the shared drive.

Sources include:

- Bookmaster
- IBM ACS
- Amazon Vendor Central
- Booktopia PAD
- Nielsen Sell-through

The shared drive acts as the operational repository before reports are consumed by dashboards or automation.

---

# 7. Warehouse Operations

## 7.1 Overview

Ligare Australia is the primary third-party logistics (3PL) warehouse for Elsevier Australia.

The warehouse manages:

- Inventory Storage
- Receiving
- Put-away
- Picking
- Packing
- Dispatch
- POD Inventory
- Returns

---

## 7.2 Warehouse Layout

The warehouse is organised into multiple storage areas based on inventory type.

Storage areas include:

- Open Picking
- Carton Storage
- Bulk Storage
- POD Storage
- Temporary Storage

Warehouse reference images should be maintained in this section.

---

## 7.3 Storage Types

| Storage Type | Description |
|--------------|-------------|
| Open Pick | Daily picking locations |
| Carton Storage | Carton replenishment |
| Bulk Storage | Pallet storage |
| POD Storage | POD inventory |
| Temporary Storage | Receiving / Holding |

---

## 7.4 Warehouse Location Dictionary

Warehouse locations use prefixes to identify storage areas.

| Prefix | Area | Description |
|---------|------|-------------|
| OA | Open Picking | Shelf Location |
| OB | Open Picking | Shelf Location |
| A-PB | Carton Storage | Mini Bulk |
| E | Bulk Storage | Pallet Storage |
| P | Bulk Storage | Fast Moving Pallets |
| STKIN | Receiving | Temporary Holding |

Additional warehouse prefixes should be added as required.

---

## 7.5 Warehouse Rules

General warehouse rules.

- Location prefixes identify storage type.
- Bulk locations are used for pallet storage.
- Open pick locations support daily operations.
- Temporary locations should be cleared promptly.
- Warehouse location codes must remain unique.
- Warehouse documentation should match physical layout.

---

## 7.6 Warehouse Reference Images

Maintain warehouse photographs including:

- Overall warehouse layout
- Open Picking
- Bulk Storage
- Carton Storage
- Receiving Area
- POD Storage

Images should be updated whenever warehouse layouts change.

---

## 7.7 Receiving Process

General receiving workflow.

```
Supplier

↓

Shipment

↓

Warehouse Receipt

↓

Inspection

↓

Bookmaster Receipt

↓

Put-away
```

---

## 7.8 Put-away Process

```
Receiving

↓

Warehouse Allocation

↓

Location Assignment

↓

Bulk / Open Pick

↓

Inventory Available
```

---

## 7.9 Picking Process

```
Customer Order

↓

Pick List

↓

Warehouse Picking

↓

Packing

↓

Dispatch
```

---

## 7.10 Inventory Movements

Typical inventory movement types.

- Receipt
- Put-away
- Transfer
- Pick
- Dispatch
- Return
- Stock Adjustment
- Cycle Count
- Write-off

- # 8. External Data Sources

## 8.1 Overview

Not all operational data originates from Bookmaster.

Several external systems provide inventory, sales, shipment and purchasing data which support operational reporting, inventory planning and business decision making.

Most external reports are manually downloaded or received through email before being stored in the shared drive.

---

## 8.2 Data Source Summary

| Source | Owner | Collection Method | Frequency | Storage | Purpose |
|---------|-------|------------------|-----------|---------|---------|
| Bookmaster | Krishna Kumar | Report Extraction | Daily / Monthly | Shared Drive | ERP Reporting |
| IBM ACS | Krishna Kumar | Report Export | Daily | Shared Drive | Shipment & ASN Reporting |
| Amazon Vendor Central | Krishna Kumar | Manual Download | Weekly (Monday) | Shared Drive | Amazon Inventory & Sales |
| Booktopia PAD | Email | Email Attachment | Daily | Shared Drive | Purchase Advice |
| Nielsen Sell-through | Elna Schonfeldt | Portal Export | Monthly | Shared Drive | Retail Sell-through Analysis |

---

## 8.3 Bookmaster Reports

Bookmaster remains the primary operational data source.

Major data areas include:

- Inventory
- Purchase Orders
- Customer Orders
- POD
- Warehouse
- Pricing
- KPI Reporting

---

## 8.4 IBM ACS

IBM ACS provides shipment and ASN reporting.

Typical usage:

- Shipment Register
- ASN Tracking
- Shipment Status
- Delivery Monitoring

Frequency

- Daily

Storage

- Shared Drive

---

## 8.5 Amazon Vendor Central

Amazon Vendor Central data is manually downloaded every Monday morning.

Purpose:

- Sales Review
- Inventory Monitoring
- Customer Performance
- Amazon Analysis

Collection Method

Manual Download

Storage

Shared Drive

---

## 8.6 Booktopia PAD

Booktopia sends PAD (Purchase Advice Data) through email.

Process

```
Booktopia

↓

Email

↓

Attachment

↓

Shared Drive
```

Frequency

Daily

Purpose

- Purchase Planning
- Demand Planning
- Customer Requirements

---

## 8.7 Nielsen Sell-through

Nielsen Sell-through data is exported monthly from the Nielsen Portal.

Owner

Elna Schonfeldt

Collection Process

```
Nielsen Portal

↓

Monthly Export

↓

Email

↓

Shared Drive
```

Purpose

- Retail Sell-through Analysis
- Market Performance
- Sales Analysis

---

## 8.8 Shared Drive

The Shared Drive acts as the operational repository for business reporting.

It stores:

- Bookmaster Reports
- IBM ACS Reports
- Amazon Vendor Central Reports
- Booktopia PAD Files
- Nielsen Sell-through Reports
- Historical Operational Reports

Shared Drive

```
\\elssyddatp001.science.regn.net
```

---

## 8.9 SharePoint

SharePoint is used as the central collaboration platform for operational documentation and shared business resources.

Primary usage includes:

- Operational Documents
- Shared Templates
- Reference Files
- Project Documentation

---

## 8.10 Data Collection Flow

```
Bookmaster
        │
        ▼
Bookmaster Reports
        │
        ▼
Shared Drive
        ▲
        │
IBM ACS
Amazon Vendor Central
Booktopia PAD
Nielsen Sell-through
        │
        ▼
Business Reporting
```

---

# 9. Business Processes

## 9.1 Purchase Planning

Purchase Planning is performed using inventory reports, demand analysis, sales trends and business rules.

Primary inputs include:

- Inventory Reports
- Sales History
- Nielsen Sell-through
- Customer Demand
- Publisher Requirements

Purchase Planning follows predefined planning cycles.

---

## 9.2 Inventory Planning

Inventory planning aims to maintain stock availability while minimising excess inventory.

Planning considers:

- Sales
- Forecast
- Inventory Levels
- Lead Time
- Publisher Requirements
- Warehouse Capacity

---

## 9.3 POD Workflow

```
Customer Order

↓

Bookmaster

↓

POD Purchase Order

↓

POD Printer

↓

Printing

↓

Dispatch

↓

Customer Delivery
```

Primary POD Printers

- Markono
- Lightning Source Australia

---

## 9.4 Purchase Order Workflow

```
Purchase Planning

↓

Purchase Order

↓

Supplier

↓

Production

↓

Shipment

↓

Warehouse Receipt

↓

Available Inventory
```

---

## 9.5 Sea Freight Workflow

```
Supplier

↓

Sea Freight

↓

Forwarder

↓

Australian Port

↓

Ligare Warehouse

↓

Inventory Receipt
```

Primary Forwarders

- DGF
- Publiship
- Scan Shipping

---

## 9.6 Air Freight Workflow

```
Supplier

↓

Air Freight

↓

DHL Express / DGF

↓

Australia

↓

Ligare

↓

Inventory
```

---

## 9.7 Receiving Process

```
Shipment

↓

Warehouse Receipt

↓

Inspection

↓

Bookmaster Receipt

↓

Put-away
```

---

## 9.8 Customer Order Lifecycle

```
Customer Order

↓

Bookmaster

↓

Inventory Allocation

↓

Warehouse Picking

↓

Packing

↓

Dispatch

↓

Customer
```

---

## 9.9 Monthly KPI Process

Monthly KPI reporting uses multiple Bookmaster reports.

Typical activities include:

- Transactions
- Inventory
- Sales
- Fill Rate
- Warehouse Performance
- POD Performance

Supporting reports are documented within Bookmaster Report Catalogue.

---

## 9.10 Freight Management

Freight management includes:

- Air Freight
- Sea Freight
- Shipment Monitoring
- Freight Cost Tracking
- Delivery Monitoring

Primary Forwarders

- DGF
- DHL Express
- Publiship
- Scan Shipping

---

# 10. Automation Landscape

## 10.1 Current Manual Processes

Current manual operational activities include:

- Bookmaster Report Extraction
- Amazon Vendor Central Download
- Booktopia PAD Saving
- Nielsen Sell-through Download
- Monthly KPI Compilation
- Report Distribution

---

## 10.2 Current Automated Processes

Current automated processes include:

- Email Distribution
- Scheduled System Reports
- Standard Operational Reporting

---

## 10.3 Automation Pipeline

Current operational flow

```
Bookmaster

↓

Report Extraction

↓

Excel

↓

Shared Drive

↓

Operational Reporting

↓

Business Decisions
```

Future automation initiatives will focus on reducing manual intervention while maintaining existing business processes.

---

## 10.4 Future Automation Opportunities

Potential areas for automation include:

- Bookmaster Silent Extraction
- Automated Report Collection
- Shared Drive Monitoring
- Dashboard Refresh
- Customer Reporting
- Shipment Monitoring
- Purchase Planning Support
- Inventory Analytics

- # 11. Reporting Standards

## 11.1 Purpose

Reporting standards ensure consistency across all operational reports, business analysis, management reporting and future automation.

These standards apply to all manually prepared reports and reports generated through future automation.

---

## 11.2 Excel Standards

### Workbook Standards

- One report per workbook unless otherwise required.
- Sheet names should be meaningful.
- Remove unnecessary blank worksheets.
- Freeze top row where applicable.
- Enable Auto Filter on all tables.

---

### Header Standards

- Use a single header row.
- Header names should be business friendly.
- Avoid abbreviations where possible.
- Use Title Case for column headers.

Example

| Preferred | Avoid |
|-----------|------|
| Order Number | ORDNO |
| Customer Name | CUST |
| Purchase Order | PO_NO |

---

### Date Standards

Preferred format

```
DD-MMM-YYYY
```

Example

```
24-Jul-2026
```

Avoid

```
24/07/26

07/24/26

20260724
```

---

### Number Formatting

Inventory

```
12,345
```

Currency

```
AUD 12,345.67
```

Percentage

```
92.45%
```

---

### General Formatting

- Autofit columns.
- Avoid merged cells.
- Remove hidden rows.
- Remove hidden columns.
- Use consistent fonts.
- Keep reports printer friendly.

---

## 11.3 Report Naming Standards

Recommended naming convention

```
<Report Name>_YYYYMMDD.xlsx
```

Examples

```
SOHQ_20260724.xlsx

POD_Orders_20260724.xlsx

Purchase_Orders_20260724.xlsx
```

---

## 11.4 Folder Structure Standards

Reports should be organised logically.

Example

```
Bookmaster

IBM ACS

Amazon

Booktopia

Nielsen

Archive
```

Historical reports should never overwrite previous extracts.

---

## 11.5 File Naming Standards

General naming convention

```
YYYYMMDD_ReportName.xlsx
```

Example

```
20260724_E00120B.xlsx

20260724_SOHQ.xlsx

20260724_POD_Orders.xlsx
```

---

## 11.6 Documentation Standards

Documentation should:

- Use business terminology.
- Keep screenshots current.
- Record business rules.
- Maintain version history where appropriate.
- Keep procedures up to date.

---

# 12. Operational Playbooks

## 12.1 Purchase Planning

Purpose

Maintain inventory availability while minimising excess inventory.

Primary Inputs

- Inventory Reports
- Sales History
- Nielsen Sell-through
- Publisher Requirements
- Customer Demand

Output

Purchase Orders

---

## 12.2 POD Operations

Workflow

```
Customer Order

↓

Bookmaster

↓

POD Purchase Order

↓

Markono / Lightning Source

↓

Shipment

↓

Customer
```

---

## 12.3 Warehouse Operations

Daily operational activities include:

- Receiving
- Put-away
- Picking
- Packing
- Dispatch
- Returns
- Stock Adjustments

---

## 12.4 Freight Operations

Sea Freight

- DGF
- Publiship
- Scan Shipping

Air Freight

- DHL Express
- DGF

Activities

- Shipment Booking
- Documentation
- Delivery Monitoring
- Freight Invoice Verification

---

## 12.5 Inventory Review

Regular review activities include:

- Low Stock Review
- Overstock Review
- Slow Moving Inventory
- POD Inventory
- Purchase Recommendations

---

## 12.6 Slow Moving Stock Review

Objectives

- Identify aged inventory.
- Reduce excess stock.
- Support inventory optimisation.

Primary Report

- SLOWSTK2

---

## 12.7 Customer Queries

Common customer requests

- Order Status
- Shipment Status
- POD Orders
- Inventory Availability
- Publication Availability

Supporting reports

- Purchase Orders
- POD Reports
- Shipment Reports
- Inventory Reports

---

## 12.8 Exception Handling

Common operational exceptions

- Shipment Delays
- POD Rejections
- Inventory Variance
- Missing ASN
- Freight Issues
- Warehouse Exceptions

---

# 13. Business Rules

## 13.1 Bookmaster Rules

- Bookmaster is the operational system of record.
- Actual extract report numbers take precedence over menu report numbers.
- Historical extracts should be retained.
- Shared Drive is the operational report repository.

---

## 13.2 Inventory Rules

- Inventory planning follows predefined planning cycles.
- POD inventory is managed separately from standard inventory.
- Inventory adjustments should be traceable.
- Historical inventory reports should be retained.

---

## 13.3 Supplier Rules

- MP009 is used for POD orders with Markono.
- MAR03 is used for regular (non-POD) orders with Markono.
- Lightning Source Australia supports POD production.
- Griffin Press is retained for historical reference only.

---

## 13.4 Warehouse Rules

- Ligare is the primary Australia 3PL warehouse.
- Warehouse location prefixes identify storage types.
- Open Pick locations support daily operations.
- Bulk locations support pallet storage.

---

## 13.5 Customer Rules

Primary retail customers include:

- Amazon
- Booktopia

Customer-specific operational reports should be maintained separately where applicable.

---

## 13.6 Purchasing Rules

- Purchase planning follows business planning cycles.
- Supplier selection depends on inventory type.
- POD orders follow dedicated POD workflows.

---

## 13.7 Freight Rules

Sea Freight

UK

Default

- DGF

Alternative

- Publiship
- Scan Shipping

Air Freight

UK

Less than 50kg

- DHL Express

Greater than 50kg

- DGF

US

- DGF

---

# 14. Glossary

## 14.1 Business Terms

| Term | Meaning |
|------|---------|
| POD | Print On Demand |
| LLP | Low Level Profile |
| ELP | Elsevier Logistics Profile |
| KPI | Key Performance Indicator |
| ASN | Advance Shipping Notice |
| SOH | Stock On Hand |

---

## 14.2 Bookmaster Terms

| Term | Meaning |
|------|---------|
| BM | Bookmaster |
| POD Order | Print On Demand Purchase Order |
| Data Transfer | Bookmaster Extraction Utility |
| Accounting Period | Financial Reporting Period |

---

## 14.3 Warehouse Terms

| Term | Meaning |
|------|---------|
| Open Pick | Daily Picking Location |
| Bulk Storage | Pallet Storage |
| Put-away | Inventory Location Assignment |
| Receiving | Goods Receipt |

---

## 14.4 Logistics Terms

| Term | Meaning |
|------|---------|
| DGF | DHL Global Forwarding |
| DHL Express | Express Courier |
| POD Printer | Print-on-Demand Supplier |
| 3PL | Third Party Logistics |

---

## 14.5 Supply Chain Terms

| Term | Meaning |
|------|---------|
| Purchase Planning | Inventory Replenishment Planning |
| Replenishment | Inventory Restocking |
| Sell-through | Retail Sales Performance |
| Inventory Planning | Stock Optimisation |

---

## 14.6 Acronyms

| Acronym | Description |
|----------|-------------|
| ACS | IBM Advanced Customer System |
| BM | Bookmaster |
| POD | Print On Demand |
| KPI | Key Performance Indicator |
| ASN | Advance Shipping Notice |
| SOH | Stock On Hand |
| WH | Warehouse |
| HS | Health Sciences |
| S&T | Science & Technology |
| SEA | South East Asia |
| APAC | Asia Pacific |
| 3PL | Third Party Logistics |

---

# 15. Appendix

## A. Organisation Charts

Maintain current organisation charts for:

- Leadership
- Operations
- Warehouse
- Logistics

---

## B. Warehouse Reference Images

Maintain photographs for:

- Warehouse Layout
- Open Pick Area
- Bulk Storage
- Receiving Area
- POD Storage

---

## C. Bookmaster Navigation

Maintain navigation trees for:

- Screen 52
- Screen 53
- Screen 54
- Screen 90

Refer to **Bookmaster.md** for complete navigation and report details.

---

## D. Reference Tables

Maintain reference tables for:

- Supplier Codes
- Warehouse Codes
- Finance Codes
- Stock Status Codes
- Answer Codes
- Freight Accounts
- Purchase Planning Cycles

---

## E. Useful Links

### Shared Drive

```
\\elssyddatp001.science.regn.net
```

### SharePoint

```
C:\Users\kk3\OneDrive - Reed Elsevier Group ICO Reed Elsevier Inc\OG-AU Operations - Inventory_Management
```

### Shared Mailbox

```
InventoryAndShippingAU@elsevier.com
```
