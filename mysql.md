---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: MySQL

subcollection: watsonx-bi



---
{{site.data.keyword.attribute-definition-list}}

# MySQL
{: #mysql}

MySQL is an open-source relational database management system.{: #shortdesc}


## Supported versions
{: #supp_mysql}

- MySQL Enterprise Edition 5.0+

- MySQL Community Edition 4.1, 5.0, 5.1, 5.5, 5.6, 5.7

## Create a connection to MySQL
{: #create_mysql}

To create the connection, you need these connection details:

- Database (optional): If you do not enter a database name, you must enter the catalog name, schema name, and the table name in the properties for SQL queries.
- Hostname or IP address
- Port number
- Encoding (optional): The character encoding for your data. If not specified, the default character set of the database server is used. If you change the value, enter a valid character encoding, for example, UTF-8.
- Username and password
- SSL certificate, if required by the database server

Select **Server proxy** to access the MySQL data source through a server proxy. Depending on its setup, a server proxy can provide load balancing, increased security, and privacy. The server proxy settings are independent of the authentication credentials and the personal or shared credentials selection. The server proxy settings cannot be stored in a vault.

- Proxy hostname or IP address: The proxy URL. For example, https://proxy.example.com.
- Server proxy port: The port number to connect to the proxy server. For example, 8080 or 8443.
- The Proxy username and Proxy password fields are optional.

For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

