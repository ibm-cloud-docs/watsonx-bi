---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: Microsoft SQL

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# Microsoft SQL Server
{: #microsoft_sql}

Microsoft SQL Server is a relational database management system.


## Supported versions
{: #supp_microsoft_sql}

Microsoft SQL Server 2022

## Create a connection to Microsoft SQL Server
{: #create_microsoft_sql}

To create the connection, you need these connection details:

- Database name - You don't have to specify the database. With no database specified, you can import metadata from every database that is available for that connection.
- Hostname or IP address
- Port number or Instance name - If the server is configured for dynamic ports, use the Instance name.
- Username and password
- Domain name - If the Microsoft SQL Server has been set up in a domain that uses NTLM (New Technology LAN Manager) authentication, select Use Active Directory and enter the name of the domain that is associated with the username and password.
- SSL certificate, if required by the database server

For **Private connectivity**, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

## Restriction
{: #restriction_microsoft_sql}

Except for NTLM authentication, Windows Authentication is not supported.
