# Bronze Layer - Metadata-Driven Pipeline

## Overview

The Bronze layer is responsible for ingesting source data into the Fabric
Lakehouse while preserving the source structure with minimal transformation.

The ingestion process is implemented using a metadata-driven pipeline.

## Pipeline Flow

```text
Lookup Metadata
       |
       v
Filter Active Sources
       |
       v
ForEach Source
       |
       v
Switch Process Type
       |
       +----> Process Type A
       |
       +----> Process Type B
       |
       +----> Process Type C
