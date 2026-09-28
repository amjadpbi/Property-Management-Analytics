# Property Management Analytics

A property-portfolio analytics model covering occupancy, leasing, maintenance, marketing, and financial performance.

## Project Overview
This project combines multiple operational data domains in a single Power BI model to support portfolio monitoring across properties, leases, vacancy, financials, maintenance, and activity KPIs.

## Business Context
This is a self-initiated analytics project built around a local property-management scenario. The data is modeled for learning and portfolio demonstration rather than for a live property-operating system.

## Problem
The project needed a single analytical view of property operations to compare occupancy, servicing activity, lead conversion, and financial health across the portfolio.

## Solution
The repository contains a PBIP project with a semantic model and report pages covering executive summary, sales pipeline, property operations, financial overview, AI receptionist activity, and marketing performance.

## Data
- Source type: CSV files
- Data nature: local simulated property portfolio dataset
- Key tables: Properties, DailyOccupancy, FinancialData, LeadsPipeline, LeaseData, MaintenanceTickets, MarketingCampaigns, AIReceptionistCalls

## Technical Approach
- load operational CSV datasets
- build relationships across property, financial, and activity tables
- develop portfolio and property-level measures in the semantic model
- produce report pages for KPI review and trend tracking

## Key Analytical Areas
- occupancy and utilization analysis
- lease and lead pipeline review
- maintenance and property operations monitoring
- marketing performance tracking
- financial overview and portfolio-level trends

## Evidence / Scope
The repository contains the Power BI project, semantic model, report assets, and source CSV files. The evidence supports a local analytical model built for portfolio reporting rather than a production property system.

## Limitations
- local synthetic/project dataset
- no live operational system integration evidence
- educational or demonstration scope

## Repository Structure
- Property.pbip — Power BI project file
- Property.Report — report definition
- Property.SemanticModel — semantic model definition
- *.csv files — operational source data
- PROJECT_AUDIT.md — evidence summary

## Tools & Technologies
- Power BI
- CSV data inputs
- DAX measures
- PBIP/PBIR semantic model

## Project Status
Self-initiated property analytics project with verified local project artifacts. No production deployment claims are made.
