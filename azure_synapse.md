---

copyright:
  years: 2026
lastupdated: "2026-07-10"

keywords: azure synapse

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# Microsoft Azure Synapse Analytics connection
{: #azure_synapse}

Microsoft Azure Synapse Analytics is a data warehouse analytics service provided as part of Microsoft Azure. {: #shortdesc}

This connection only supports the dedicated SQL pool.
{: note}

## Create a connection to Microsoft Azure Synapse Analytics
{: #create_synapse_connection}

To access your data in Microsoft Azure Synapse Analytics, create a connection to it. You need these details:

### Connection 
{: #connection_synapse}

- Database name

- Hostname or IP address

- Port number


### Credentials
{: #credentials_synapse}

Choose an authentication method:

Prerequisite for Entra ID authentication - Microsoft Entra ID is a cloud-based identity and access management service. To obtain connection values for the Entra ID authentication method, sign in to the [Microsoft Azure portal](https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?redirect_uri=https%3A%2F%2Fportal.azure.com%2Fsignin%2Findex%2F&response_type=code%20id_token&scope=https%3A%2F%2Fmanagement.core.windows.net%2F%2Fuser_impersonation%20openid%20email%20profile&state=OpenIdConnect.AuthenticationProperties%3D5yQBebvex6f4g9Xe_Cm13mtF0h5wTOVqDYavGxKhtmE3Ms-KIOBl3nNFqu6NIjiXQAbsX07xSdZlLlp_wiM0YQRn0EQ3byw91xFD6c_cF1k5uL61hBqa7E48--1ztG6PYigaTB_q4F_AnXEjEYcfwf2F6X17M0K8IjNC1yZJSP5x8UBTVjffV6AXlRoe0ViAn9xoRXF8YGyMM25sqLQYINZBkaHLgUx6B4zKGZuc3DEoDGS0YaDqnm7fqf8rXxHICWkaWTrc5WH3MURn2NF4WHU6fYKgwSlw151ya98EYKjUTQdH5oDukTzRUks0m77to5zNPcPKx_eIqhWX78N6WGBBVrQYjXvzRBBQEwBl7yxkkL4xG79iUIxZh43FV08csXljm5TW-k1dfmLLEcmzekLFyKlkwX_RTqA13tC1b5jF6lZVPLdbf6Sa7kzs8mlXCU7rWr6yrAQ59pasEEECu1q9NB9BSTS-lRFWNwGucU8&response_mode=form_post&nonce=638894979132594798.MTIyMmMyMmUtYzlkZC00ZGYwLTgwNDMtYzkzZjkyYjYwZjkwODQ5ZWY3ZmEtNjA2OS00OTZhLTlkMDUtNzFiZjc4MmZmNTk0&client_id=c44b4083-3bb0-49c1-b47d-974e53cbdf3c&site_id=501430&instance_aware=true&client-request-id=21ec90fc-c894-4534-bf73-504c1fdd798b&x-client-SKU=ID_NET472&x-client-ver=8.3.0.0&sso_reload=true){: external}. For information about Microsoft Entra ID, see: <br> - [What is Microsoft Entra ID?](https://learn.microsoft.com/en-us/entra/fundamentals/whatis) <br> - [Get Microsoft Entra ID tokens for service principals](https://learn.microsoft.com/azure/databricks/dev-tools/service-prin-aad-token) <br> [Microsoft Entra authentication with SQL documentation](https://learn.microsoft.com/en-us/azure/azure-sql/database/authentication-azure-ad-landing?view=azuresql){: external}
{: note}

- Username and password to access the database in Microsoft Azure Synapse Analytics

- Entra ID client secret credentials

  - Client ID: The client ID for authorizing access to Microsoft Azure. To find the Client ID for your application, select **Microsoft Entra ID**. From **App registrations**, select your application. Click **Copy** to copy the Client ID of your application. For more information, see [Register a Microsoft Entra app and create a service principal](https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal){: external}.

  - Client secret: The authentication key that is associated with the client ID for authorizing access to Microsoft Azure. To find the Client secret for your application, select **Microsoft Entra ID**. From **App registrations**, select your application. Go to **Certificates & secrets > Client secrets**. Click **Copy** to copy the existing Client secret or click **New client secret** to create a new Client secret and copy it. For more information, see [Register a Microsoft Entra app and create a service principal](https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal){: external}.

    
- Entra ID username password credential for the Microsoft Azure account

### Certificates
{: #certificates_synapse}

Port is SSL-enabled: Enable this option if the port you have chosen is configured to accept SSL connections.

If the Port is SSL-enabled option is enabled, fill in the following fields:

- SSL certificate: Enter the SSL certificate of the host to be trusted

- Hostname in SSL certificate: The hostname in SubjectAlternativeName or Common Name (CN) part of the SSL certificate

- Validate the SSL certificate: Enable this option to validate that the SSL certificate returned by the host is trusted

For Private connectivity, to connect to a database that is not externalized to the internet (for example, behind a firewall), you must set up a [secure connection](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

If you connect with IBM Cloud Satellite, you need to set the Proxy connection policy on the Azure server in order to connect to the Azure SQL Database. For more information, see [Azure SQL Database connectivity architecture](https://learn.microsoft.com/en-us/azure/azure-sql/database/connectivity-architecture?view=azuresql){: external}.
