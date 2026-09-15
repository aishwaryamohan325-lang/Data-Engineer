# Azure Databricks — ADLS Gen2 and Key Vault

A documented exercise in reading cloud files and retrieving protected credentials.

[View the project report](Azure-Databricks-ADLS-KeyVault-Project.pdf)

## Workflow

1. Configure access from Databricks to ADLS Gen2 using a storage account key.
2. Read a CSV through an `abfss` path and inspect the Spark DataFrame.
3. Create Azure Key Vault secrets and a Key Vault-backed Databricks secret scope.
4. Retrieve a secret with `dbutils.secrets.get` and verify redacted output.
5. Read another file from the storage container.

## Evidence and scope

The report documents a 150-row file read, secret-scope configuration, redacted secret retrieval and a subsequent file read. It covers a learning environment, including broad network access used during testing. It does not establish a production security design or demonstrate that every storage read uses the retrieved secret.

## Discussion points

Explain the difference between direct key configuration and secret retrieval, which permissions are needed, and how a production version could improve identity, network restrictions and credential rotation.

[All Azure projects](../README.md)
