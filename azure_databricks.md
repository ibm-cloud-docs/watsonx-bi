---

copyright:
  years: 2025, 2026
lastupdated: "2026-04-01"

keywords: Databricks

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# Microsoft Azure Databricks connection
{: #azure_databricks}

Databricks is a big data analytics tool based on Apache Spark. {: #shortdesc}

## Supported versions
{: #supp_version_azure_databricks}

Databricks SQL engine version 4.0.0. For compatibility, use JDBC driver version 2.6.25 or later.


## Limitations
{: #limitations_databricks}

Only structured relational databases are supported.


## Create a connection to Databricks
{: #create_databricks}

To access your data in Microsoft Azure Databricks, create a connection to it. 

Enter these connection details and select an authentication method.

### Connection details 
{: #connection_databricks}


- Connection name 

- Hostname or IP address of the database

- Port number 

- HTTP path: Path of the endpoint for which the server is configured in HTTP transport mode.

- Keepalive interval: Interval in seconds between keepalive validation queries. Set to a value greater than 0 to enable keepalive.



### Credentials
{: #credentials_databricks}

Choose an authentication method:

Prerequisite for Entra ID authentication - Microsoft Entra ID is a cloud-based identity and access management service. To obtain connection values for the Entra ID authentication method, sign in to the [Microsoft Azure portal](https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?redirect_uri=https%3A%2F%2Fportal.azure.com%2Fsignin%2Findex%2F&response_type=code%20id_token&scope=https%3A%2F%2Fmanagement.core.windows.net%2F%2Fuser_impersonation%20openid%20email%20profile&state=OpenIdConnect.AuthenticationProperties%3D5yQBebvex6f4g9Xe_Cm13mtF0h5wTOVqDYavGxKhtmE3Ms-KIOBl3nNFqu6NIjiXQAbsX07xSdZlLlp_wiM0YQRn0EQ3byw91xFD6c_cF1k5uL61hBqa7E48--1ztG6PYigaTB_q4F_AnXEjEYcfwf2F6X17M0K8IjNC1yZJSP5x8UBTVjffV6AXlRoe0ViAn9xoRXF8YGyMM25sqLQYINZBkaHLgUx6B4zKGZuc3DEoDGS0YaDqnm7fqf8rXxHICWkaWTrc5WH3MURn2NF4WHU6fYKgwSlw151ya98EYKjUTQdH5oDukTzRUks0m77to5zNPcPKx_eIqhWX78N6WGBBVrQYjXvzRBBQEwBl7yxkkL4xG79iUIxZh43FV08csXljm5TW-k1dfmLLEcmzekLFyKlkwX_RTqA13tC1b5jF6lZVPLdbf6Sa7kzs8mlXCU7rWr6yrAQ59pasEEECu1q9NB9BSTS-lRFWNwGucU8&response_mode=form_post&nonce=638894979132594798.MTIyMmMyMmUtYzlkZC00ZGYwLTgwNDMtYzkzZjkyYjYwZjkwODQ5ZWY3ZmEtNjA2OS00OTZhLTlkMDUtNzFiZjc4MmZmNTk0&client_id=c44b4083-3bb0-49c1-b47d-974e53cbdf3c&site_id=501430&instance_aware=true&client-request-id=21ec90fc-c894-4534-bf73-504c1fdd798b&x-client-SKU=ID_NET472&x-client-ver=8.3.0.0&sso_reload=true){: external}. For more information about Microsoft Entra ID, see What is [Microsoft Entra ID?](https://learn.microsoft.com/en-us/entra/fundamentals/whatis) and [Get Microsoft Entra ID tokens for service principals](https://learn.microsoft.com/azure/databricks/dev-tools/service-prin-aad-token).
{: note}

- Entra ID client secret credentials

  - Tenant ID: The client ID for authorizing access to Microsoft Azure. 

  - Client ID of service principal: The client ID of service prinicpal for authorizing access to Microsoft Azure.

  - Client secret of service principal: The authentication key that is associated with the client ID for authorizing access to Microsoft Azure. 
    
- Entra ID token 

- Service principal credentials

- Username and password 
