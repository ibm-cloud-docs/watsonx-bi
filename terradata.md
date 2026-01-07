---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: terradata

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Terradata connection 
{: #terradata}

Teradata provides database and analytics-related services and products.


## Supported versions 
{: #supp_terradata}

Teradata databases 15.10, 16.10, 17.00, 17.10, and 17.20


## Create a connection to Terradata
{: #create_terradata}

To create the connection, you need these connection details:

- Database (optional) - If you do not enter a database name, you must enter the catalog name, schema name, and the table name in the properties for SQL queries.

- Hostname or IP address
- Port (optional)
- Client character set (optional) - Do not enter a value unless you are instructed by IBM support. The character set value overrides the Teradata JDBC drivers normal mapping of the Teradata session character sets. Data corruption can occur if you specify the wrong character set. If no value is specified, UTF16 is used.
- Query band expression (optional): Semicolon-separated list of name-value pairs to use in the generated query band statement for the session. A query band is a set of user-defined parameters that can be set on a session, a transaction, or both to identify the originating source of a query. After you define a query band, it is passed to the Teradata database as a list of name=value pairs in a single quoted string. For example, 'ProjectName=dstage1'.
- Authentication method: Select the security mechanism to use to authenticate the user:
  - TD2 (Teradata Method 2): Use the Teradata security mechanism.
  - LDAP: Use an LDAP security mechanism for external authentication.
- Username and password
- SSL certificate (if required by the database server)

For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.
