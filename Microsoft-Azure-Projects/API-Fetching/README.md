# API Fetching with Azure Data Factory

Two documented pipelines that fetch Google search results through **SearchAPI.io** and land JSON responses in **ADLS Gen2**.

| Project | Purpose | Report |
| --- | --- | --- |
| Google News | Fetch India-focused news results and save timestamped JSON in date-based folders | [News pipeline](Google_News_API_Azure_Pipeline.pdf) |
| Google Shopping | Fetch filtered product results and save a timestamped JSON snapshot | [Shopping pipeline](Google_Shopping_API_Azure_Pipeline.pdf) |

## Workflow

```text
SearchAPI.io REST endpoint → ADF Copy Data → ADLS Gen2 JSON file
```

The reports cover REST and ADLS linked services, source and sink datasets, query parameters, dynamic output naming, previews and successful-run checks. Both include inspection of the resulting JSON in storage.

## Skills demonstrated

REST API ingestion, ADF Copy Activity, ADLS Gen2, JSON, query filtering and dynamic expressions.

## Interview discussion points

- Explain base URL and relative URL configuration.
- Compare date-based News folders with the Shopping snapshot destination.
- Discuss API limits, pagination, retries and secure credential handling as future improvements.

The PDFs document learning exercises; pipeline exports and a deployed recurring schedule are not included.

[All Azure projects](../README.md) · [Portfolio](../../README.md)
