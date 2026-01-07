---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# Oracle
{: #oracle}

Oracle is a multi-model database management system. {: #shortdesc}

## Supported versions
{: #supp_oracle}

- Oracle Database 19c and 21c

## Create a connection to Oracle
{: #create_oracle}

To create the connection, you need these connection details:

- Service name or Database (SID)
- Hostname or IP address
- Port number
- Username and password
- SSL certificate (if required by the database server)
- Alternate servers: A list of alternate database servers to use for failover for new or lost connections.
  Syntax: (servername1[:port1][;property=value[;...]][,servername2[:port2][;property=value[;...]]]...)

  The server name (servername1, servername2, and so on) is required for each alternate server entry. The port number (port1, port2, and so on) and the connection properties (property=value) are optional for each alternate server entry. If the port is unspecified, the port number of the primary server is used.

  If the port number of the primary server is not specified, the default port number 1521 is used.

  The optional connection properties are the ServiceName and SID.

- Metadata discovery: The setting determines whether comments on columns (remarks) and aliases for schema objects such as tables or views (synonyms) are retrieved when assets are added by using this connection.

- Select **Use proxy server** to access the Oracle data source through a server proxy. Depending on its setup, a server proxy can provide load balancing, increased security, and privacy. The server proxy settings are independent of the authentication credentials and the personal or shared credentials selection. The server proxy settings cannot be stored in a vault. You will need:
  -  Proxy hostname or IP address: The proxy URL. For example, https://proxy.example.com.
  -  Server proxy port: The port number to connect to the proxy server. For example, 8080 or 8443.
  -  The Proxy username and Proxy password fields are optional.
  
- Private connectivity - For Private connectivity, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a secure connection.
