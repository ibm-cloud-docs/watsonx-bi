---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: MariaDB

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# MariaDB
{: #mariadb}

MariaDB is an open source relational database. You can use the MariaDB connection to connect to either a MariaDB server or to a Microsoft Azure Database for MariaDB service in the cloud.{: #shortdesc}


## Supported versions
{: #supp_mariadb}

- MariaDB server: 10.5.5

- Microsoft Azure Database for MariaDB: 10.3

## Create a connection to MariaDB
{: #create_mariadb}

To create the connection, you need these connection details:

- Database (optional): If you do not enter a database name, you must enter the catalog name, schema name, and the table name in the properties for SQL queries.
- Hostname or IP address
- Port number
- Username and password
- SSL certificate, if required by the database server

For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

## MariaDB setup
{: #setup_mariadb}

Setup depends on whether you are connecting from a local MariaDB server or a Microsoft Azure Database for MariaDB database service in the cloud.

- MariaDB server: [Server Management](https://mariadb.com/docs/server/server-management  )
- Microsoft Azure Database for MariaDB: [Quickstart: Create an Azure Database for MariaDB server by using the Azure portal](https://learn.microsoft.com/en-us/previous-versions/azure/mariadb/quickstart-create-mariadb-server-database-using-azure-portal)
