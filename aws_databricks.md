---

copyright:
  years: 2025, 2026
lastupdated: "2026-04-01"

keywords: Databricks, aws

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# AWS Databricks connection
{: #aws_databricks}

AWS Databricks is a unified, cloud-based analytics platform on AWS that combines data warehousing and data lake capabilities.{: #shortdesc}


## Limitations
{: #limitations_aws_databricks}

Only structured relational databases are supported.


## Create a connection to AWS Databricks
{: #create_aws_databricks}

To access your data in AWS Databricks, create a connection to it. 

Enter these connection details and select an authentication method. 

### Connection details 
{: #connection_aws_databricks}

- Connection name 

- Hostname or IP address of the database

- Port number 

- HTTP path: Path of the endpoint for which the server is configured in HTTP transport mode.

- Keepalive interval: Interval in seconds between keepalive validation queries. Set to a value greater than 0 to enable keepalive.


### Credentials
{: #credentials_aws_databricks}

Choose an authentication method:

- Service principal credentials - A service principal is a specialized Databricks identity for automation and programmatic access. It provides secure, API-only access to Databricks resources without using individual user credentials. For more information, see [Manage service principals](https://docs.databricks.com/en/admin/users-groups/service-principals.html){: external}.

  - Client ID of service principal: The client ID of service prinicpal managed by Databricks on AWS.

  - Client secret of service principal: The authentication key that is associated with the client ID of service principal managed by Databricks on AWS.

- Username and password for the data source
