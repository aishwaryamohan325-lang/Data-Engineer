# Azure Data Factory — Mapping Data Flows

Transformation exercises using weather CSV data and Azure SQL tables.

## Weather data transformation

[View the walkthrough](ADF-Data-Flow-Activity-2.pdf)

```text
Weather CSV → Derived Column (temp_F) → Select (remove city) → Blob output
```

Adds Fahrenheit temperature using `(temperature_c * 1.8) + 32`, adjusts the output columns and writes the result to storage. The report shows previews, a successful pipeline run and the output CSV.

## SQL transformations

[View the walkthrough](ADF-Data-Flow-Screenshots.pdf)

- Filter the Employee table to the IT department, sort it and write to Blob Storage.
- Join Employee and Departments sources, then write the joined output to Blob Storage.

The report includes SQL and storage setup, linked services, transformation previews and run evidence.

## Discussion points

Explain transformation order, join keys, output schema checks and how null values or unmatched rows could affect results.

[All Azure projects](../README.md)
