---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: snowflake
subcollection: watsonx-bi


---
{{site.data.keyword.attribute-definition-list}}

# Snowflake
{: #snowflake}

Snowflake is a cloud-based data storage and analytics service.{: #shortdesc}

## Create a connection to Snowflake
{: #create_snowflake}

You can create a connection to Snowflake using two methods:

### Common connectivity
{: #connectivity_snowflake}

To create the connection, you need the following connection details:

- Account name: The full name of your account
- Database name
- Role: The default access control role to use in the Snowflake session
- Warehouse: The virtual warehouse
- Okta URL endpoint: If your company uses native Okta SSO authentication, enter the Okta URL endpoint for your Okta account. 

  Example: https://<okta_account_name>.okta.com

  Leave this field blank if you want to use the default authentication of Snowflake. For information about federated authentication provided by Okta, see [Native SSO - Okta only](https://docs.snowflake.com/en/user-guide/admin-security-fed-auth-use#native-sso-okta-only).

### Credentials
{: #credentials_snowflake}

Authentication method:

- Username and password
- Key-Pair: Enter the contents of the private key and the key passphrase (if configured). These properties must be set up by the Snowflake administrator. For information, see [Key Pair Authentication & Key Pair Rotation](https://docs.snowflake.com/en/user-guide/key-pair-auth) in the Snowflake documentation.
