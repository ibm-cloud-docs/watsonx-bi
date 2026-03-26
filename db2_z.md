---

copyright:
  years: 2025, 2026
lastupdated: "2026-03-25"

keywords: Db2, z/os

subcollection: watsonx-bi


---
{{site.data.keyword.attribute-definition-list}}

# IBM Db2 for z/OS connection
{: #db2_zos}

IBM Db2 for z/OS is an enterprise data server for IBM Z. It manages core business data across an enterprise and supports key business applications.{: #shortdesc}

## Supported versions
{: #supp_db2_zos}

- IBM Db2 for z/OS 12 and 13

## Prerequisites
{: #prereq_db2_zos}

A certificate file on the Db2 for z/OS server is required to use this connection. 

These steps must be done on the Db2 for z/OS server:

:   Obtain an IBM Db2 Connect Unlimited Edition license certificate file from [Db2 Connect licensing information](https://www.ibm.com/docs/en/db2/12.1.x?topic=connect-licensing-information) and [Installing the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/en/db2/12.1.x?topic=apis-installing-data-server-driver-jdbc-sqlj).

:   For installation instructions, see [Activating the license certificate file for Db2 Connect Unlimited Edition](https://www.ibm.com/docs/en/db2/12.1.x?topic=dswnls-activating-license-key-db2-connect-unlimited-edition-system-z).


## Create a connection to Db2 for z/OS
{: #create_db2_zos}

To create the connection, you need these connection details:


- Host name or IP address
- Port number
- Collection ID - The ID of the collections of packages to use
- Location - The unique name of the Db2 location you want to access
- Username and password
- Application name (optional) - The name of the application that is currently using the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/en/db2/12.1.x?topic=pecidscip-client-info-properties-support-by-data-server-driver-jdbc-sqlj). 

- Client accounting information (optional) - The value of the accounting string from the client information that is specified for the connection. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/en/db2/12.1.x?topic=pecidscip-client-info-properties-support-by-data-server-driver-jdbc-sqlj).

- Client hostname (optional) - The hostname of the machine on which the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/en/db2/12.1.x?topic=pecidscip-client-info-properties-support-by-data-server-driver-jdbc-sqlj).

- Client user (optional) - The name of the user on whose behalf the application that is using the connection is running. For information, see [Client info properties support by the IBM Data Server Driver for JDBC and SQLJ](https://www.ibm.com/docs/en/db2/12.1.x?topic=pecidscip-client-info-properties-support-by-data-server-driver-jdbc-sqlj).

- SSL certificate (if required by the database server)


