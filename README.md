# Retail Sales Data Engineering Platform

## Project Overview

An end-to-end retail data engineering and analytics solution built using
Microsoft Fabric.

The project implements Medallion Architecture to process retail sales data
through Bronze, Silver, and Gold layers, followed by data warehousing,
semantic modeling, and Power BI reporting.

## Architecture

Source Data
    ↓
Bronze Layer
    ↓
Silver Layer
    ↓
Gold Layer
    ↓
Warehouse
    ↓
Semantic Model
    ↓
Power BI Report

## Bronze Layer

The Bronze layer is responsible for ingesting and storing source data in its
raw or minimally transformed form.

### Components

- Fabric Lakehouse
- Data Pipeline
- Metadata-driven processing
- Lookup activity
- Filter activity
- ForEach activity
- Switch-based processing

The Bronze pipeline uses metadata to identify active sources and dynamically
process them.

## Silver Layer

The Silver layer is responsible for cleaning and transforming the ingested
data.

### Components

- Fabric Lakehouse
- PySpark Notebook
- Data transformation
- Data cleansing
- Data standardization
- Data quality preparation

## Gold Layer

The Gold layer contains business-ready data prepared for analytics and
reporting.

### Components

- Fabric Lakehouse
- PySpark Notebook
- Data Pipeline
- Fabric Warehouse
- Business-ready datasets

## Analytics Layer

The processed data is exposed through a semantic model and consumed by
Power BI for interactive analysis.

### Dashboard Analysis

The report provides analysis such as:

- Total sales amount
- Total quantity
- Order count
- Sales by category
- Sales by order date
- Sales by state
- Order status
- Customer and product details

## Technologies

- Microsoft Fabric
- Fabric Lakehouse
- Fabric Data Pipelines
- PySpark
- SQL
- Fabric Warehouse
- Semantic Models
- Power BI
- Medallion Architecture

## Key Data Engineering Concepts

- ETL / ELT
- Data ingestion
- Metadata-driven pipelines
- Medallion Architecture
- Data transformation
- Data modeling
- Data warehousing
- Business intelligence
- Analytical reporting

## Project Architecture

```text
Retail Sales Data
        │
        ▼
┌───────────────────┐
│ Bronze Layer      │
│ Lakehouse         │
│ Pipeline          │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ Silver Layer      │
│ Lakehouse         │
│ PySpark Notebook  │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ Gold Layer        │
│ Lakehouse         │
│ PySpark Notebook  │
│ Pipeline          │
│ Warehouse         │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ Semantic Model    │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ Power BI Report   │
└───────────────────┘
