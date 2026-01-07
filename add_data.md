---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: add data, connectors, connection
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Add data through a connection
{: #select}

To select the data you want to use to create metrics, you need to add the data to the semantic data model by creating a database connection. {: #shortdesc}

You can add a connection or, if you previously connected to a database in the project, use an existing connection to select data.  

## Adding data from a new connection 
{: #add}

1. Click **Create metrics** on the **Data and Metrics** tab and enter a name for the new semantic data model.

2. On the **Select data** page, select **New connection**. 

3. Select the data source type and connector that you want to use. 

   Click the **Filter** icon and select **watsonx BI** to view a list of compatible data sources. 
   {: note}

4. Enter the required details for the connection. Typically, you need to provide information like the hostname, port number, username, and password.  

5. If prompted, specify whether you want to use personal or shared credentials. You cannot change this option after you create the connection. The account owner sets the credential type for the connection. The default setting is Shared.

   - Personal: With personal credentials, each user must specify their own credentials to access the connection. Each user's credentials are saved but are not shared with any other users. Use personal credentials instead of shared credentials to protect credentials. For example, if you use personal credentials and another user changes the connection properties (such as the hostname or port number), the credentials are invalidated to prevent malicious redirection.

   - Shared: With shared credentials, all users access the connection with the credentials that you provide. Shared credentials might be retrieved by a user who has access to the connection asset. Because the credentials are shared, it is difficult to audit access to the connection to identify the source of data loss, or identify the source of a security breach.

6. Click **Test connection** and if the test succeeds, click **Create**.

7. Select the schema and data tables that you want to use and click **Add**.

8. (Optional) You can add more data through a new or existing connection from the **Select data** drop-down. 

9. Click **Next** to move to the next step, which is [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}.  

## Adding data from an existing connection 
{: #existing}

1. Click **Create metrics** on the **Data and Metrics** tab and enter a name for the new semantic data model. 

2. Select **Existing connection** on the **Select data** page. 

3. Select the database connection name.

4. Select the schema and data tables that you want to use and click **Add**.

5. (Optional) Add more data through a new or existing connection from the **Select data** list. 

6. Click **Next** to move to the next step, which is metadata enrichment.

## Supported connectors
{: #supported_connectors}

The following data sources are supported. 

- [Amazon Redshift](/docs/watsonx-bi?topic=watsonx-bi-amazon_redshift){: external}
- [Dremio](/docs/watsonx-bi?topic=watsonx-bi-dremio){: external}
- [Google BigQuery](/docs/watsonx-bi?topic=watsonx-bi-google_big_query){: external}
- [IBM Cognos Analytics](/docs/watsonx-bi?topic=watsonx-bi-cognos){: external} 
- [IBM Db2](/docs/watsonx-bi?topic=watsonx-bi-db2){: external}
- [IBM Informix](/docs/watsonx-bi?topic=watsonx-bi-informix){: external}
- [IBM Netezza Performance Server](/docs/watsonx-bi?topic=watsonx-bi-netezza){: external} 
- [IBM watsonx.data](/docs/watsonx-bi?topic=watsonx-bi-wxd){: external} 
- [MariaDB](/docs/watsonx-bi?topic=watsonx-bi-mariadb){: external} 
- [Microsoft Azure SQL Database](/docs/watsonx-bi?topic=watsonx-bi-microsoft_azure_sql){: external} 
- [Microsoft SQL Server](/docs/watsonx-bi?topic=watsonx-bi-microsoft_sql){: external} 
- [MySQL](/docs/watsonx-bi?topic=watsonx-bi-mysql){: external}
- [Oracle Database](/docs/watsonx-bi?topic=watsonx-bi-oracle){: external} 
- [PostgreSQL](/docs/watsonx-bi?topic=watsonx-bi-postgresql){: external}
- [Presto](/docs/watsonx-bi?topic=watsonx-bi-presto){: external} 
- [Salesforce API](/docs/watsonx-bi?topic=watsonx-bi-salesforce_api){: external} 
- [SingleStore DB](/docs/watsonx-bi?topic=watsonx-bi-singlestoredb){: external}
- [Snowflake](/docs/watsonx-bi?topic=watsonx-bi-snowflake){: external} 
- [Terradata database](/docs/watsonx-bi?topic=watsonx-bi-terradata){: external} 

For more information, see [Connectors](https://dataplatform.cloud.ibm.com/docs/content/wsj/manage-data/conn_types.html?context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=analytics&context=dph&context=analytics&context=cpdaas&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp){: external}.

## Next steps
{: #next}

- [Metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external} 

- [Generate metrics automatically](/docs/watsonx-bi?topic=watsonx-bi-generate_metrics){: external} 

- [Building metrics in the Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode){: external} 
