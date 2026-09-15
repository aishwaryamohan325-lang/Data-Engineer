# Azure Data Factory — Control Flow

Two exercises demonstrating pipeline orchestration and conditional processing.

## Exercise 1: Activities and triggers

[View the walkthrough](ADF-Control-Flow-Activity-1.pdf)

Covers Copy Data mappings, Delete activity logging, manual/schedule/tumbling-window/storage-event triggers, Set Variable, Append Variable, Get Metadata and Execute Pipeline. The report includes configuration and successful-run screenshots.

## Exercise 2: Conditional file routing

[View the walkthrough](ADF-Control-Flow-Activity-2.pdf)

```text
Get Metadata (child items)
    → ForEach file
        → If file name contains 'temp'
            → True: Copy activity
            → False: Copy activity
```

The exercise first checks branching with variables, then replaces those steps with copy activities. Screenshots show pipeline validation, successful runs and files in the output container.

## Discussion points

Compare trigger types, explain `childItems` and dynamic expressions, and discuss how retries, duplicate files and parallel execution would be handled beyond this exercise.

[All Azure projects](../README.md)
