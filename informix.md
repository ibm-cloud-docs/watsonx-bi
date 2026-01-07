---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: informix

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# IBM Informix connection 
{: #informix}

IBM Informix is a database that contains relational, object-relational, or dimensional data. You can use the Informix connection to access data from an on-premise Informix database server or from IBM Informix on Cloud. {: #shortdesc}

## Supported versions (on-premise)
{: #supp_informix}

- Informix 14.10 and later. This version does not support the Progress DataDirect JDBC driver, which is used by the Informix connection. The Informix connection supports Informix 14.10 features that are comparable to previous Informix versions, but not the new features. Issues related to DataDirect's JDBC driver are not supported.

- Informix 14.10

- Informix 15.0

## Create a connection to Informix
{: #create_informix}

To create the connection, you need these connection details:

- Database server name 
- Database name -  You don't have to specify the database. With no database specified, you can import metadata from every database that is available for that connection.
- Hostname or IP address
- Port number - The default is 1526.
- Username and password

On-prem Informix database servers: For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

## Informix setup
{: #setup_informix}

To set up Informix, see these topics:

- Informix on-prem: [Creating a database server after installation](https://www.ibm.com/docs/SSGU8G_14.1.0/com.ibm.inst.doc/ids_inst_023.htm)

- Informix on Cloud: [IBM Informix](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-informix_database)
