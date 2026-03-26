---

copyright:
  years: 2025
lastupdated: "2026-03-25"

keywords: postgresql

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# PostgreSQL connection 
{: #postgresql}

PostgreSQL is an open source and customizable object-relational database.{: #shortdesc}

## Supported versions 
{: #supp_postgresql}

- PostgreSQL 13, 14, 15, 16, 17 and 18.


## Create a connection to PostgreSQL
{: #create_postgresql}

If you have set up an integrated cloud service, select the service instance to automatically fill in the fields in the connection form. Confirm that all the fields are complete.

To create the connection, you need these connection details:

- Database name 

- Hostname or IP address
- Port number
- Username and password
- SSL certificate (if required by the database server)

Select Server proxy to access the PostgreSQL data source through a server proxy. Depending on its setup, a server proxy can provide load balancing, increased security, and privacy. The server proxy settings are independent of the authentication credentials and the personal or shared credentials selection. The server proxy settings cannot be stored in a vault.

- Proxy hostname or IP address: The proxy URL. For example, https://proxy.example.com.

- Server proxy port: The port number to connect to the proxy server. For example, 8080 or 8443.
- The Proxy username and Proxy password fields are optional.

For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.
