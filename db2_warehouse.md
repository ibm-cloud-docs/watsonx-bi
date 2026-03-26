---

copyright:
  years: 2025, 2026
lastupdated: "2026-03-25"

keywords: Db2 warehouse

subcollection: watsonx-bi


---
{{site.data.keyword.attribute-definition-list}}

# IBM Db2 Warehouse connection
{: #db2_warehouse}

IBM Db2 Warehouse is an analytics data warehouse that gives you a high level of control over your data and applications. {: #shortdesc}

You can use the IBM Db2 Warehouse connection to connect to a database in these products:

IBM Db2 Warehouse in IBM Cloud
IBM Db2 Warehouse on-prem 

## Create a connection to Db2 Warehouse
{: #create_db2_warehouse}

To create the connection, you need these connection details:

- Database name
- Hostname or IP address of the database server
- Port number
- API key or Username and password

- Application name (optional) - The name of the application that is currently using the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client accounting information (optional) - The value of the accounting string from the client information that is specified for the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client hostname (optional) - The hostname of the machine on which the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- Client user (optional) - The name of the user on whose behalf the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/SSEPGG_11.5.0/Javadocs/src/tpc/imjcc_r0052001.html).

- SSL certificate (if required by your database server)

### Credentials
{: #db2_warehouse_credentials}

If you select **Shared**, enter either an API key or a username and password for the server.

If you select **Personal**, you have two choices:

- Enter your username and password for the server.

- Select platform login credentials. You can use this option only if the Db2 service is hosted on the instance of platform that you are connecting to.


## Authenticating with an API Key
{: #db2_warehouse_api}

You can use an API key to authenticate to Db2 Warehouse in IBM Cloud.

First add the user ID as an IAM user or as a service ID. For instructions, see the Console user experience section of the [Identity and access management (IAM) on IBM Cloud](docs/Db2whc?topic=Db2whc-iam#console-ux){: external} topic.

If users want to authenticate with Db2 Warehouse with an IAM API key, the administrator of the Db2 Warehouse instance can add the IAM users by using the User management console, and then the users can each create an API key for themselves by using the IAM access management console.

For Private connectivity, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

