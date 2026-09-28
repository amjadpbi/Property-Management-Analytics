# Property Management — Project Audit

## 1. Executive Summary

### Finding
This project is a synthetic property-management analytics dashboard created as a Power BI learning exercise. The actual implementation centers on a portfolio of rental properties and covers occupancy, financial performance, leasing pipeline, maintenance operations, marketing campaigns, and AI receptionist call activity.

### Evidence
- Project folder contains `Property.pbip`, `Property.Report`, `Property.SemanticModel`, and CSV source files.
- Source tables include `Properties.csv`, `DailyOccupancy.csv`, `FinancialData.csv`, `LeadsPipeline.csv`, `LeaseData.csv`, `MaintenanceTickets.csv`, `MarketingCampaigns.csv`, and `AIReceptionistCalls.csv`.
- The semantic model contains table definitions for each of these entities plus `_Measures`, `DateTable`, and `Expense Breakdown Table`.
- The report contains six pages: Executive Summary, Sales Pipeline, Property Operations, Financial Overview, AI Receptionist, and Marketing Performance.

### Classification
- OBSERVED FACT: the project files and data model directly show the tables, measures, and report pages.
- CREATOR-PROVIDED HISTORY: the project was inspired by a freelance platform opportunity and created as learning/practice.
- INFERENCE: the exact original freelance brief is not present, so the reconstructed business problem is inferred from the model and data.
- UNKNOWN: the full original client brief and data are not in the project files.

### Finding
The clear modeled business problem is portfolio-level property operations and leasing performance for a residential or mixed property portfolio, not a real client dataset or an actual production deployment.

### Classification
- OBSERVED FACT: the data and measures clearly model property operations and revenue/occupancy metrics.
- CREATOR-PROVIDED HISTORY: it was intended as a practice exercise based on a real-world-style requirement.

## 2. Project Classification

### Finding
This is a learning/practice project using synthetic data. It is not evidence of a real client delivery, actual private data, or verified business impact.

### Evidence
- The creator’s written context explicitly states the project was based on a freelance-style requirement and was created for learning.
- No original client contract, project brief, or actual client data is present in the folder.
- The source datasets are synthetic-looking and structured for analytical simulation.

### Classification
- CREATOR-PROVIDED HISTORY: the freelance inspiration and the process of creating synthetic data.
- OBSERVED FACT: synthetic data structure and model design.
- UNKNOWN: original client identity or original business brief.

### Implementation status
- IMPLEMENTED: portfolio property dataset, model, measures, and multi-page report.
- PARTIALLY IMPLEMENTED: some original freelance requirements are approximated but not explicitly document-backed.
- PLANNED / DESIGNED: original client project requirements are not present in the project folder.
- UNKNOWN: exact original brief and client delivery status.

## 3. Creator-Provided Context

### Finding
The creator states that the project was inspired by a property-management problem found on a freelance platform. They used the requirements as a real-world-style learning problem, shared them with Claude to understand the business, created synthetic data, and built a Power BI solution.

### Evidence
- This is the explicit narrative provided with the audit prompt.

### Classification
- CREATOR-PROVIDED HISTORY.

### Finding
This context should be treated as a history note, not as proof of a real external project delivery.

### Classification
- CREATOR-PROVIDED HISTORY.

## 4. Original Freelance / Business Context

### Finding
The actual project appears to model a property portfolio operating environment with several connected processes:

- portfolio property inventory
- occupancy tracking
- leasing and renewals
- lead generation and conversion
- financial performance and collection
- maintenance and SLA tracking
- marketing campaign performance
- AI receptionist call activity and lead qualification

### Evidence
- Source tables and model relationships are directly observable.
- Measure names and display folders reveal business groups such as `REVENUE METRICS`, `OCCUPANCY METRICS`, `LEAD & SALES METRICS`, `FINANCIAL METRICS`, and `MAINTENANCE METRICS`.

### Classification
- OBSERVED FACT for the implemented portfolio model.
- INFERENCE for the original freelance brief details.

### Finding
The exact original business requirement is not recoverable from the project folder alone. What can be reconstructed is the implemented business scenario: a property portfolio manager wants to understand operational health, occupancy, revenue, lead conversion, maintenance backlog, and campaign effectiveness.

### Evidence
- Table names and measure definitions.
- Report pages names and KPI groups.

### Classification
- INFERENCE.

### Finding
The implemented problem is best described as a portfolio-level property-management dashboard for operational and financial performance benchmarking.

### Classification
- INFERENCE based on observed project content.

## 5. Project Structure

### Finding
The project contains the following main elements:

- `Property.pbip` — project entry point for the Power BI solution.
- `Property.Report/` — report definition in PBIR format.
- `Property.SemanticModel/` — semantic model in TMDL format.
- `Properties.csv` — property dimension data.
- `DailyOccupancy.csv` — daily occupancy data by property.
- `FinancialData.csv` — monthly revenue and expense data.
- `LeadsPipeline.csv` — leads and conversion pipeline data.
- `LeaseData.csv` — lease lifecycle data.
- `MaintenanceTickets.csv` — maintenance operations data.
- `MarketingCampaigns.csv` — campaign performance data.
- `AIReceptionistCalls.csv` — inbound call activity and qualification data.
- `Property.pbix` — final binary report/model file.
- `.gitignore` — basic project support file.

### Evidence
- Project folder listing and file inventory.

### Classification
- OBSERVED FACT.

### Finding
The Power BI project is a local PBIP/PBIR/TMDL structure with direct model binding from the report to the semantic model.

### Evidence
- `Property.Report/definition.pbir` contains a `datasetReference.byPath` pointing to `../Property.SemanticModel`.

### Classification
- OBSERVED FACT.

## 6. Synthetic Data

### Finding
There are 8 source CSV files in the project root, plus the final PBIX.

### Evidence
- File inventory from the project folder.

### Classification
- OBSERVED FACT.

### Finding
Source file row counts and headers observed directly:

- `Properties.csv` — 25 rows, columns: `PropertyID, PropertyName, PropertyType, TotalUnits, Region, AcquisitionDate`
- `DailyOccupancy.csv` — 9,150 rows, columns: `Date, PropertyID, TotalUnits, OccupiedUnits, VacantUnits, OccupancyRate`
- `FinancialData.csv` — 300 rows, columns: `Month, PropertyID, PotentialRevenue, ActualRevenue, CollectedRevenue, CollectionRate, MaintenanceCost, UtilitiesCost, StaffCost, MarketingCost, OtherExpenses, TotalExpenses, NetOperatingIncome, RevenueTarget`
- `LeadsPipeline.csv` — 2,102 rows, columns: `LeadID, LeadDate, Source, PropertyID, Status, SalesRep, ConversionDate, EstimatedMonthlyRent, LeadScore`
- `LeaseData.csv` — 1,813 rows, columns: `LeaseID, PropertyID, UnitNumber, LeaseStartDate, LeaseEndDate, MonthlyRent, LeaseTerm, RenewalStatus, TenantType`
- `MaintenanceTickets.csv` — 9,019 rows, columns: `TicketID, OpenDate, PropertyID, Category, Priority, Status, ClosedDate, DaysToResolve, Cost`
- `MarketingCampaigns.csv` — 84 rows, columns: `Month, CampaignName, Channel, Budget, ActualSpend, Impressions, Clicks, Leads, Conversions, CPL, ConversionRate`
- `AIReceptionistCalls.csv` — 21,690 rows, columns: `CallID, CallDate, CallTime, CallType, DurationSeconds, IsQualifiedLead, AppointmentBooked, Resolved, SentimentScore, PropertyInquired`

### Classification
- OBSERVED FACT.

### Finding
The data appears synthetic, based on its regularized structure, generated identifiers, synthetic property IDs, balanced dimensions, and clearly created operational scenarios. The creator explicitly states the data was synthetic.

### Evidence
- The creator’s provided context.
- The data patterns and generated field names.

### Classification
- CREATOR-PROVIDED HISTORY plus OBSERVED FACT.

### Finding
The data covers a variety of property-management entities and operational variables:

- Properties: property inventory and attributes
- Occupancy: rolling daily occupancy and vacancy rates
- Revenue: monthly revenue, collection, target, and net operating income
- Leads: lead source, pipeline stages, and conversion dates
- Leases: contract start/end, rent, term, and renewal status
- Maintenance: ticket status, priority, resolution time, and cost
- Marketing: budget, spend, leads, conversions, CPL, conversion rate
- AI receptionist: calls, lead qualification, appointment booking, sentiment, property inquiry

### Classification
- OBSERVED FACT.

### Finding
The project does not contain a script, prompt archive, or generation workflow to independently verify the exact data-generation method. The creator explicitly states that synthetic data was created after understanding the problem, but the project folder does not independently demonstrate the underlying prompt or generation procedure.

### Classification
- CREATOR-PROVIDED HISTORY.
- UNKNOWN for the exact generation workflow.

## 7. Power Query / Data Preparation

### Finding
The model shows each table imported directly from CSV with the same basic pattern, executed in Power Query M:

```m
Source = Csv.Document(File.Contents("D:\Power BI\Upwork Project\<file>.csv"), [Delimiter=",", Columns=<n>, Encoding=1252, QuoteStyle=QuoteStyle.None]),
#"Promoted Headers" = Table.PromoteHeaders(Source, [PromoteAllScalars=true]),
#"Changed Type" = Table.TransformColumnTypes(...)
```

### Evidence
- Table definitions for `Properties`, `DailyOccupancy`, `FinancialData`, `LeadsPipeline`, `LeaseData`, `MaintenanceTickets`, `MarketingCampaigns`, and `AIReceptionistCalls` all show this pattern.

### Classification
- OBSERVED FACT.

### Finding
Power Query is used mainly for ingestion and column typing. The project does not show extensive multi-step transformation logic, merges, appends, custom functions, or staging queries beyond straightforward import and type conversion.

### Evidence
- Partition source definitions and table structure.

### Classification
- OBSERVED FACT.

### Finding
Some derived logic exists in the semantic model itself, especially in calculated columns. For example:

- `LeadsPipeline` contains `DaysInPipeline`, `LeadSourceCategory`, and `IsConverted`.
- `MaintenanceTickets` contains `IsOverdue` and `TicketAgeCategory`.
- `AIReceptionistCalls` contains `CallHour`, `CallDurationMinutes`, and `IsBusinessHours`.

### Evidence
- Table definitions in TMDL.

### Classification
- OBSERVED FACT.

### Finding
The project does not contain a separate staging model or formal ETL layer beyond direct CSV import and model-level calculated columns. The majority of a business transformation story is represented in the semantic model and DAX measures rather than elaborate Power Query steps.

### Classification
- INFERENCE grounded in model structure.

## 8. Data Model

### Finding
The semantic model contains the following tables:

- `Properties`
- `DailyOccupancy`
- `FinancialData`
- `LeadsPipeline`
- `LeaseData`
- `MaintenanceTickets`
- `MarketingCampaigns`
- `AIReceptionistCalls`
- `DateTable`
- `Expense Breakdown Table`
- `_Measures`
- multiple local date tables auto-generated for date-based relationships

### Evidence
- `model.tmdl` and table file inventory.

### Classification
- OBSERVED FACT.

### Finding
The core relationship pattern is a portfolio dimension connected to operational fact tables:

- `DailyOccupancy.PropertyID` → `Properties.PropertyID`
- `FinancialData.PropertyID` → `Properties.PropertyID`
- `LeadsPipeline.PropertyID` → `Properties.PropertyID`
- `LeaseData.PropertyID` → `Properties.PropertyID`
- `MaintenanceTickets.PropertyID` → `Properties.PropertyID`
- `AIReceptionistCalls.PropertyInquired` → `Properties.PropertyID`

Date-based relationships connect the operational tables to date tables:

- `DailyOccupancy.Date` → `DateTable.Date`
- `LeadsPipeline.LeadDate` → `DateTable.Date`
- `MaintenanceTickets.OpenDate` → `DateTable.Date`
- `AIReceptionistCalls.CallDate` → `DateTable.Date`
- `FinancialData.Month` → `DateTable.Date`
- `MarketingCampaigns.Month` → `DateTable.Date`
- `LeaseData.LeaseStartDate` and `LeaseEndDate` to local date tables
- `Properties.AcquisitionDate` to local date table

### Evidence
- `Property.SemanticModel/definition/relationships.tmdl`.

### Classification
- OBSERVED FACT.

### Finding
This is not a classic one-table star schema with a single fact table; instead it is a multi-fact portfolio model with several operational facts linked to a `Properties` dimension and to a date table. It is best described as a multi-fact, star-like model around property inventory and time.

### Evidence
- Multiple fact-like tables and relationships.

### Classification
- OBSERVED FACT / INFERENCE.

### Finding
The model also includes an `Expense Breakdown Table` as a calculated table used for visual grouping around revenue and expense categories. This is not a raw source table; it is methodically generated in TMDL with `DATATABLE`.

### Evidence
- `Expense Breakdown Table.tmdl`.

### Classification
- OBSERVED FACT.

### Finding
The project uses time intelligence and multiple date tables. The model file shows `annotation __PBI_TimeIntelligenceEnabled = 1`.

### Evidence
- `model.tmdl`.

### Classification
- OBSERVED FACT.

## 9. Business Process Reconstruction

### Finding
The project represents several distinct but connected operating processes.

#### 1. Property portfolio performance
- Source: `Properties.csv`, `DailyOccupancy.csv`, `FinancialData.csv`
- Model tables: `Properties`, `DailyOccupancy`, `FinancialData`
- Measures: occupancy rate, revenue per unit, NOI, NOI margin, revenue vs target, total units, portfolio occupancy rate
- Report pages: Executive Summary, Financial Overview, Property Operations

#### 2. Leasing and lead conversion
- Source: `LeadsPipeline.csv`, `LeaseData.csv`
- Model tables: `LeadsPipeline`, `LeaseData`
- Measures: `Total Leads`, `Converted Leads`, `Lead Conversion Rate`, `Qualification Rate`, `Lead to Tour Conversion`, `Tour to Lease Conversion`, `Avg Days to Convert`, `Lead Value`, `Weighted Pipeline Value`, `Pipeline Value`
- Report pages: Sales Pipeline, Executive Summary

#### 3. Maintenance operations / SLA management
- Source: `MaintenanceTickets.csv`
- Model tables: `MaintenanceTickets`
- Measures: `Total Tickets`, `Open Tickets`, `Closed Tickets`, `Avg Resolution Time`, `Emergency Tickets`, `Avg Ticket Cost`, `SLA Compliance Rate`, `Aging Tickets`, `IsOverdue`, `TicketAgeCategory`
- Report pages: Property Operations

#### 4. Marketing performance
- Source: `MarketingCampaigns.csv`
- Model tables: `MarketingCampaigns`
- Measures: campaign spend, impressions, leads, conversion rate, CPL, etc. (the dataset contains marketing metrics but the exact top-level measures are not fully enumerated in the snippet inspected; they appear as a report focus in the page names)
- Report pages: Marketing Performance

#### 5. AI receptionist call handling
- Source: `AIReceptionistCalls.csv`
- Model tables: `AIReceptionistCalls`
- Measures: call count, qualified lead rate, appointment booking, documented sentiment, call-hours logic, resolution handling via `CallType` and `IsQualifiedLead`
- Report pages: AI Receptionist

#### 6. Lease and contract lifecycle
- Source: `LeaseData.csv`
- Model tables: `LeaseData`
- Measures: lease terms, tenancy types, renewal status, rent metrics; less explicitly surfaced in the visible measure names but present in the table and relationship model
- Report pages: likely property operations / sales pipeline context

### Evidence
- Table structures, measures, report page names, and relationship layout.

### Classification
- OBSERVED FACT for the implemented process groupings.
- INFERENCE for exact original requirement details.

## 10. DAX / Measures

### Finding
The `_Measures` table contains a substantial set of deployed measures grouped into display folders, including:

- `REVENUE METRICS`
- `OCCUPANCY METRICS`
- `LEAD & SALES METRICS`
- `FINANCIAL METRICS`
- `MAINTENANCE METRICS`

### Evidence
- `_Measures.tmdl`.

### Classification
- OBSERVED FACT.

### Finding
Key measure groups and examples:

#### Revenue and financial performance
- `Total Revenue` = `SUM(FinancialData[CollectedRevenue])`
- `Potential Revenue` = `SUM(FinancialData[PotentialRevenue])`
- `Revenue vs Target` = `[Total Revenue] - [Revenue Target]`
- `Revenue vs Target %` = `DIVIDE([Total Revenue]-[Revenue Target], [Revenue Target], 0)`
- `Collection Rate` = `DIVIDE(SUM(FinancialData[CollectedRevenue]), SUM(FinancialData[ActualRevenue]), 0)`
- `Delinquency Amount` = `SUM(FinancialData[ActualRevenue]) - SUM(FinancialData[CollectedRevenue])`
- `NOI` = `SUM(FinancialData[NetOperatingIncome])`
- `NOI Margin` = `DIVIDE([NOI], [Total Revenue], 0)`
- `Operating Expense Ratio` = `DIVIDE([Total Expenses], [Total Revenue], 0)`
- `Break-even Occupancy` = `DIVIDE([Total Expenses], [Potential Revenue], 0)`

#### Occupancy and property utilization
- `Portfolio Occupancy Rate` = `DIVIDE(SUM(DailyOccupancy[OccupiedUnits]), SUM(DailyOccupancy[TotalUnits]), 0)`
- `Avg Occupancy Rate` = `AVERAGEX(DailyOccupancy, DailyOccupancy[OccupancyRate])`
- `Occupied Units` = `SUM(DailyOccupancy[OccupiedUnits])`
- `Vacant Units` = `SUM(DailyOccupancy[VacantUnits])`
- `Properties Below 90%` = count of property rows under 90% occupancy from summarization

#### Lead and sales pipeline
- `Total Leads` = `COUNTROWS(LeadsPipeline)`
- `Converted Leads` = `CALCULATE([Total Leads], LeadsPipeline[Status] = "Lease Signed")`
- `Lead Conversion Rate` = `DIVIDE([Converted Leads], [Total Leads], 0)`
- `Qualification Rate` = `DIVIDE([3 - Qualified], [Total Leads], 0)`
- `Avg Days to Convert` = average days from lead date to conversion date
- `Lead Value` = `SUMX(FILTER(LeadsPipeline, LeadsPipeline[Status] = "Lease Signed"), LeadsPipeline[EstimatedMonthlyRent] * 12)`
- `Weighted Pipeline Value` = weighted value by status stage
- `Pipeline Value` = sum of qualified/toured/application deals

#### Maintenance and operations
- `Total Tickets` = `COUNTROWS(MaintenanceTickets)`
- `Open Tickets` = `CALCULATE([Total Tickets], MaintenanceTickets[Status] <> "Closed")`
- `Closed Tickets` = `CALCULATE([Total Tickets], MaintenanceTickets[Status] = "Closed")`
- `Avg Resolution Time` = average `DaysToResolve` for closed tickets
- `Emergency Tickets` = count of emergency tickets
- `SLA Compliance Rate` = proportion of closed tickets resolved within severity-based target days
- `Aging Tickets` = unresolved tickets with age over 7 days

### Classification
- OBSERVED FACT based on static measure definitions.

### Finding
The measures are coherent with a property-management analytic scenario: occupancy, rent collection, conversion, maintenance SLA, and portfolio financial performance. They are consistent with a practice dashboard rather than a validated real client implementation.

### Classification
- INFERENCE plus OBSERVED FACT.

### Finding
No runtime DAX execution was performed in this audit. The conclusions about measure logic arise from static inspection only.

### Classification
- UNKNOWN for runtime verification.

## 11. Report Structure

### Finding
The report contains six pages, with the page names matching the business functions:

- Executive Summary
- Sales Pipeline
- Property Operations
- Financial Overview
- AI Receptionist
- Marketing Performance

### Evidence
- `Property.Report/definition/pages/pages.json` and each page object.

### Classification
- OBSERVED FACT.

### Finding
The page visual counts observed directly are:

- Executive Summary — 22 visuals
- Sales Pipeline — 16 visuals
- Property Operations — 17 visuals
- Financial Overview — 17 visuals
- AI Receptionist — 16 visuals
- Marketing Performance — 17 visuals

### Evidence
- Counted from page folders under `Property.Report/definition/pages`.

### Classification
- OBSERVED FACT.

### Finding
The report includes a mix of visual types, including:

- KPIs/cards
- funnel charts
- bar charts
- column charts
- combo charts
- line charts
- donut charts
- tables/matrices
- slicers
- textbox/page navigation/shape elements
- custom visuals as public custom visuals in `report.json`

### Evidence
- Visual JSON files under page folders and `report.json` public custom visuals list.

### Classification
- OBSERVED FACT.

### Finding
The report is structured as a multi-page property operations dashboard: summary page for portfolio overview, sales page for leasing pipeline, property operations for maintenance, financial overview for revenue and expenses, AI receptionist for inbound call funnel, and marketing performance for campaign analytics.

### Classification
- INFERENCE based on page names and visuals.

## 12. Business Questions Supported

### Finding
The implemented model and report can answer, within the synthetic scenario, questions such as:

- What is the portfolio occupancy rate and which properties are below target occupancy?
- How does revenue perform against target and how do expenses affect NOI?
- What are the collection and delinquency trends?
- How many leads are generated and what is the conversion rate to lease signed?
- Which lead sources and sales reps are producing the strongest pipeline?
- Which properties or units have maintenance issues and how quickly are tickets resolved?
- Which maintenance priorities are delayed or non-compliant with SLA?
- How do marketing campaigns perform by spend, impressions, leads, and conversions?
- How are AI receptionist calls generating qualified leads and appointments?
- Which property types or regions are performing best or weakest?

### Evidence
- Report design, page names, and DAX measure logic.

### Classification
- INFERENCE grounded in observed model artifacts.

### Finding
These are analytical capabilities of the synthetic model, not verified real-world business outcomes.

### Classification
- INFERENCE.

## 13. End-to-End Lineage

### Finding
The actual visible lineage is:

```text
Synthetic CSV source data
  -> Power Query CSV import and type conversion
  -> semantic model tables (Properties, DailyOccupancy, FinancialData, LeadsPipeline, LeaseData, MaintenanceTickets, MarketingCampaigns, AIReceptionistCalls)
  -> relationships to Properties and DateTable
  -> DAX measures in _Measures
  -> multi-page PBIR report
```

### Evidence
- CSV file headers, Power Query source definitions, TMDL relationships, `_Measures.tmdl`, and report page structure.

### Classification
- OBSERVED FACT for the project implementation.

### Finding
The business flow is not a single enterprise data warehouse pipeline; it is a compact, purpose-built analytical model designed to support portfolio operations analysis.

### Classification
- INFERENCE grounded in the observed structure.

## 14. Learning Objectives Demonstrated

### Finding
This project demonstrates a range of Power BI learning objectives:

- translating a business problem into a data model
- creating synthetic data for a realistic portfolio scenario
- using CSV-based source ingestion and type conversion
- building a multi-table semantic model with property, date, and operational fact tables
- modeling occupancy, revenue, pipeline, lease, maintenance, and marketing data together
- writing DAX measures for portfolio KPIs and operational metrics
- creating a structured, multi-page dashboard to tell a business story
- applying time intelligence and operational scorecards

### Evidence
- The project files and model objects provide direct evidence for each item.

### Classification
- OBSERVED FACT plus INFERENCE.

## 15. Claude / AI Boundary

### Creator-provided history
The creator states that the original freelance-style requirements were shared with Claude to help understand the business and analytical problem.

### Directly observed implementation
The actual project files clearly show the portfolio property-management analytics model, synthetic data tables, DAX, and PBIR report pages.

### Unknown
The project does not provide evidence of which specific prompt or AI workflow created each table, measure, or chart. It also does not provide a complete requirement document or an exact AI-generated design specification. Therefore, it is not possible to attribute particular implementation details to Claude with evidence.

### Classification
- CREATOR-PROVIDED HISTORY for the AI-assisted understanding workflow.
- UNKNOWN for exact AI-generated deliverables and implementation attribution.

## 16. Freelance / Client Boundary

### Finding
The project was inspired by a property-management problem found on a freelance platform. The creator used that scenario as a real-world-style learning exercise while learning Power BI.

### Evidence
- This is direct creator-provided context.

### Classification
- CREATOR-PROVIDED HISTORY.

### Finding
The project should not be represented as the actual client’s delivered Power BI solution, private data, or a verified business implementation.

### Evidence
- Creator-provided context explicitly says so.
- The project contains synthetic datasets and no client data evidence.

### Classification
- CREATOR-PROVIDED HISTORY plus OBSERVED FACT.

### Finding
It should not imply that the project had actual client impact, access to the original company’s systems, or real property portfolio performance data.

### Classification
- CREATOR-PROVIDED HISTORY / UNKNOWN for real-world business impact.

## 17. Implemented vs Planned

### IMPLEMENTED
- PBIP, semantic model, and report structure are present.
- Eight synthetic CSV sources are in the project root.
- Property portfolio tables for property, occupancy, financial, lead, lease, maintenance, marketing, and AI call data are implemented.
- DAX measures covering revenue, occupancy, pipeline, finance, and maintenance are present.
- Multi-page report with seven distinct page groupings exists.
- Date relationships and time intelligence are implemented.

### PARTIALLY IMPLEMENTED
- The original freelance requirement is only partially reconstructable from the project files.
- Some business assumptions appear to be inferred from the model rather than documented in the folder.
- Campaign and AI receptionist logic appear implemented but not fully documented in a formal requirement file.

### PLANNED / DESIGNED
- The broader idea of “a real-world-style property-management challenge from a freelance platform” is directly described by the creator.
- Some original design decisions may have been shaped by that requirement, but the project does not preserve the original brief.

### UNKNOWN
- Exact original freelance project text
- Original client identity and data
- Full requirement specification
- Exact data-generation method
- Verified business outcomes or real client delivery status

## 18. Portfolio Relevance

### Finding
This project demonstrates a strong real-world-style property portfolio analytics scenario in Power BI. It shows the ability to turn a general operational problem into a synthetic but coherent analytical model.

### Evidence
- Multi-table model, DAX measures, and multi-page dashboard.

### Classification
- OBSERVED FACT plus INFERENCE.

### Finding
It is relevant as evidence of:

- property-management analytical modeling
- multi-table semantic modeling
- occupancy and financial KPI design
- lead/conversion pipeline logic
- maintenance and service operations analytics
- marketing and AI-contact-center metrics
- dashboard storytelling in Power BI

### Limitation
- Synthetic data only
- Learning/practice project
- No verified actual client delivery
- No verified business impact
- No production deployment evidence

### Classification
- CREATOR-PROVIDED HISTORY plus INFERENCE.

## 19. Limitations / Unknowns

### Finding
The following cannot be verified from the project files alone:

- the exact original freelance platform project or client brief
- the original client’s private data or exact business rules
- the exact synthetic-data generation workflow
- the exact AI prompts used to understand the business or generate data
- runtime DAX results or visual rendering in Power BI Desktop
- deployment or publishing status
- external connection behavior and refresh
- user interaction details beyond the stored report metadata
- whether the model was ever used in a real business process

### Evidence
- No external brief files, no prompt archive, no runtime execution, no deployment metadata in the project folder.

### Classification
- UNKNOWN / LIMITATION.

## 20. Evidence Summary

### Project boundary
- `Property.pbip` — project entry point
- `Property.Report/` — PBIR report definition
- `Property.SemanticModel/` — TMDL semantic model
- `Properties.csv`, `DailyOccupancy.csv`, `FinancialData.csv`, `LeadsPipeline.csv`, `LeaseData.csv`, `MaintenanceTickets.csv`, `MarketingCampaigns.csv`, `AIReceptionistCalls.csv` — source data
- `Property.pbix` — binary final artifact

### Model evidence
- `Property.SemanticModel/definition/model.tmdl` — model structure and query order
- `relationships.tmdl` — relationships joining operational tables to properties/date tables
- `tables/Properties.tmdl` — property dimension
- `tables/DailyOccupancy.tmdl` — occupancy fact table
- `tables/FinancialData.tmdl` — monthly financial fact table
- `tables/LeadsPipeline.tmdl` — lead and conversion fact table
- `tables/LeaseData.tmdl` — lease lifecycle fact table
- `tables/MaintenanceTickets.tmdl` — maintenance operational fact table
- `tables/MarketingCampaigns.tmdl` — marketing campaign fact table
- `tables/AIReceptionistCalls.tmdl` — call operations fact table
- `tables/_Measures.tmdl` — deployment of business measures
- `tables/Expense Breakdown Table.tmdl` — calculated table for expense categorization

### Report evidence
- `Property.Report/definition/pages/pages.json` — page ordering
- `Property.Report/definition/pages/*/page.json` — page names
- `Property.Report/definition/pages/*/visuals/*/visual.json` — visual types and layout metadata
- `Property.Report/definition/report.json` — theme information and custom visuals

### Audit boundary
- This audit separates creator-provided history from implementation evidence.
- The project was built as a synthetic property-management learning exercise.
- The files support the model and report content directly; they do not demonstrate a real client delivery or actual commercial business impact.

---

### Final factual statement
The project represents a synthetic property portfolio dashboard built as a practice exercise. It models occupancy, revenue, lead conversion, lease activity, maintenance operations, marketing performance, and AI receptionist call handling. The semantic model contains multiple operational fact tables connected to a property dimension and date tables, and the report includes a multi-page analytical dashboard. The project is educational and synthetic, not evidence of a real client implementation or real business performance.
