# Incremental Load with Azure Data Factory

A watermark-based exercise that selects new or changed rows from **Azure SQL Database** and writes them to **ADLS Gen2** as CSV.

[View the project report](Incremental_Load_ADF.pdf)

## Objective

Avoid copying the full source table on every run by tracking the last loaded modification timestamp.

## Workflow

```text
Lookup stored watermark → Lookup source maximum timestamp
    → Copy rows within the watermark range
    → Update the stored watermark
```

The Copy activity selects rows where `LastModifytime > old watermark` and `LastModifytime <= new watermark`. A Stored Procedure activity records the new watermark for the next run.

## Evidence

The report documents the watermark table, update procedure, linked services, two lookups, dynamic query and CSV sink. Its initial debug run read and wrote five rows, followed by inspection of the output file. A subsequent delta-only run is described as expected behavior rather than shown as a separate verified run.

## Skills demonstrated

ADF orchestration, Azure SQL, Lookup and Copy activities, stored procedures, dynamic expressions and incremental ingestion.

## Interview discussion points

- Explain why the lower bound is exclusive and the upper bound inclusive.
- Explain why the watermark should advance only after a successful copy.
- Discuss retries, late-arriving changes, identical timestamps and source deletions as considerations beyond this exercise.

This folder contains documentation; pipeline exports and runnable SQL scripts are not included.

[All Azure projects](../README.md) · [Portfolio](../../README.md)
