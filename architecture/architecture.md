# Retail Sales Medallion Architecture

## Overview

This project follows the Medallion Architecture pattern using Microsoft Fabric.

The data flows through multiple layers, where each layer has a specific
responsibility for ingestion, transformation, and analytics.

## Data Flow

```text
Source Data
     |
     v
+----------------------+
| Bronze Layer         |
| Fabric Lakehouse     |
| Raw / Ingested Data  |
+----------+-----------+
           |
           v
+----------------------+
| Silver Layer         |
| Fabric Lakehouse     |
| Cleaned Data         |
+----------+-----------+
           |
           v
+----------------------+
| Gold Layer           |
| Fabric Lakehouse     |
| Business-Ready Data  |
+----------+-----------+
           |
           v
+----------------------+
| Fabric Warehouse     |
| Analytical Storage   |
+----------+-----------+
           |
           v
+----------------------+
| Semantic Model       |
| Data Modeling        |
+----------+-----------+
           |
           v
+----------------------+
| Power BI             |
| Reports & Analytics  |
+----------------------+
