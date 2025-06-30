---
copyright:
  years: 2025
lastupdated: "2025-06-27"

keywords: add data, connectors, connection
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Add data through a connection
{: #select}

To select the data you want to use to create metrics, you need to add the data to the semantic data model. You can do this by creating a database connection in the semantic data model. {: #shortdesc}

You can add a new connection or, if you previously connected to a database in the project, use an existing connection to select data. 

To do this, first click **Create metrics** on the **Data and metrics** tab and enter a name for the new semantic data model. 

## Adding data from a new connection 
{: #add}

1. On the **Select data** page, select **New connection**. 

2. Select the data source type and connector that you want to use. 

   Click the **Filter** icon and select **watsonx BI** to view a list of compatible data sources. 
   {: note}

3. Enter the required details for the connection. Typically, you need to provide information like the hostname, port number, username, and password.  

4. If prompted, specify whether you want to use personal or shared credentials. You cannot change this option after you create the connection. The credential type for the connection, either Personal or Shared, is set by the account owner. The default setting is Shared.

   - Personal: With personal credentials, each user must specify their own credentials to access the connection. Each user's credentials are saved but are not shared with any other users. Use personal credentials instead of shared credentials to protect credentials. For example, if you use personal credentials and another user changes the connection properties (such as the hostname or port number), the credentials are invalidated to prevent malicious redirection.

   - Shared: With shared credentials, all users access the connection with the credentials that you provide. Shared credentials can potentially be retrieved by a user who has access to the connection asset. Because the credentials are shared, it is difficult to audit access to the connection, to identify the source of data loss, or identify the source of a security breach.

5. Click **Test connection** and if the test succeeds, click **Create**.

6. Select the schema and data tables that you want to use and click **Add**.

7. (Optional) You can add more data through a new or existing connection from the **Select data** drop-down. 

8. Click **Next** to move to the next step, which is [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich).  

## Adding data from an existing connection 
{: #existing}

1. On the **Select data** page, select **Existing connection**.

2. Select the database connection name.

3. Select the schema and data tables that you want to use and click **Add**.

4. (Optional) You can add more data through a new or existing connection from the **Select data** drop-down. 

5. Click **Next** to move to the next step, which is metadata enrichment.

## Supported connectors
{: #supported_connectors}

The following data sources are supported. 

- Amazon Redshift
- Dremio
- Google BigQuery

- IBM DB2 
- IBM Informix
- IBM Netezza Performance Server
- IBM watsonx.data 
- MariaDB
- Microsoft Azure SQL Database
- Microsoft SQL Server
- MySQL
- Oracle Database

- PostgreSQL
- Presto
- Salesforce API
- SingleStore DB
- Snowflake
- Teradata database

For more information, see [Connectors](https://dataplatform.cloud.ibm.com/docs/content/wsj/manage-data/conn_types.html?context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=analytics&context=dph&context=analytics&context=cpdaas&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp){: external}.

## Next steps
{: #next}

- [Metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich)

- [Generate metrics automatically](/docs/watsonx-bi?topic=watsonx-bi-generate_metrics)

- [Building metrics in the Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode)
