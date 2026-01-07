---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: Db2

subcollection: watsonx-bi


---
{{site.data.keyword.attribute-definition-list}}

# IBM Db2 
{: #db2}

IBM Db2 is a data source that contains relational data. {: #shortdesc}

## Supported versions
{: #supp_db2}

- IBM Db2 10.1 and 11.5

## Create a connection to Db2
{: #create_db2}

To create the connection, you need these connection details:

For IBM Db2 on-premise connection, you might need to remove applied filters to see it in the list of supported connector types. Click the **Filter** icon and deselect **watsonx BI**.
{: note}

- Database
- Username and password
- Port number

- Application name (optional) - The name of the application that is currently using the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client accounting information (optional) - The value of the accounting string from the client information that is specified for the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client hostname (optional) - The hostname of the machine on which the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client user (optional) - The name of the user on whose behalf the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- SSL certificate (if required by your database server)

### Credentials
{: #db2_credentials}

If you select **Shared**, enter a username and password for the server.

If you select **Personal**, you have two choices:

- Enter your username and password for the server.

- Select platform login credentials. You can use this option only if the Db2 service is hosted on the instance of platform that you are connecting to.

For Private connectivity, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

