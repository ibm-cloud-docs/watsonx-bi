---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: Google BigQuery

subcollection: watsonx-bi



---
{{site.data.keyword.attribute-definition-list}}

# Google BigQuery
{: #google_big_query}

Google BigQuery is a fully managed, serverless data warehouse that enables scalable analysis over petabytes of data. {: #shortdesc}

## Create a connection to Google BigQuery
{: #create_google_big_query}

To create a connection, you need to choose an authentication method. Choices include an authentication with or without workload identity federation.

### Without workload identity federation
{: #without_workload_google_big_query}

- Account key (full JSON snippet): The contents of the Google service account key JSON file

- Client ID, Client secret, Access token, and Refresh token

### With workload identity federation
{: #with_workload_google_big_query}

You use an external identity provider (IdP) for authentication. An external identity provider uses Identity and Access Management (IAM) instead of service account keys. IAM provides increased security and centralized management. You can use workload identity federation authentication with an access token or with a token URL.

You can configure a Google BigQuery connection for workload identity federation with any identity provider that complies with the OpenID Connect (OIDC) specification and that satisfies the Google Cloud requirements that are described in [Prepare your external IdP](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-providers#oidc){: external}. The requirements include:

- The identity provider must support OpenID Connect 1.0.

- The identity provider's OIDC metadata and JWKS endpoints must be publicly accessible over the internet. Google Cloud uses these endpoints to download your identity provider's key set and uses that key set to validate tokens.
- The identity provider is configured so that your workload can obtain ID tokens that meet these criteria:
  - Tokens are signed with the RS256 or ES256 algorithm.
  - Tokens contain an aud claim.

#### Workload Identity Federation with access token connection details
{: #with_workload_access_tokens}

- Access token: An access token from the identity provider to connect to BigQuery.

- Security Token Service audience: The security token service audience that contains the project ID, pool ID, and provider ID. Use this format:

``` 
{
  //iam.googleapis.com/projects/PROJECT_NUMBER/locations/global/workloadIdentityPools/POOL_ID/providers/PROVIDER_ID
}

```
- Service account email: The email address of the Google service account to be impersonated. For more information, see [Create a service account for the external workload](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-clouds#create_a_service_account_for_the_external_workload).

- Service account token lifetime (optional): The lifetime in seconds of the service account access token. The default lifetime of a service account access token is one hour. For more information, see [URL-sourced credentials](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-providers#url-sourced-credentials).

- Token format: Text or JSON with the Token field name for the name of the field in the JSON response that contains the token.

- Token field name: The name of the field in the JSON response that contains the token. This field appears only when the Token format is JSON.

- Token type: AWS Signature Version 4 request, Google OAuth 2.0 access token, ID token, JSON Web Token (JWT), or SAML 2.0.

#### Workload Identity Federation with token URL connection details
{: #with_workload_url}

- Security Token Service audience: The security token service audience that contains the project ID, pool ID, and provider ID. Use this format:

   ```
  //iam.googleapis.com/projects/PROJECT_NUMBER/locations/global/workloadIdentityPools/POOL_ID/providers/PROVIDER_ID
  ```
  {: pre}

For more information, see [Authenticate a workload using the REST API](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-clouds#rest).

- Service account email: The email address of the Google service account to be impersonated. For more information, see [Create a service account for the external workload](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-clouds#create_a_service_account_for_the_external_workload).

- Service account token lifetime (optional): The lifetime in seconds of the service account access token. The default lifetime of a service account access token is one hour. For more information, see [URL-sourced credentials](https://cloud.google.com/iam/docs/workload-identity-federation-with-other-providers#url-sourced-credentials).

- Token URL: The URL to retrieve a token.

- HTTP method: HTTP method to use for the token URL request: GET, POST, or PUT.

- Request body (for POST or PUT methods): The body of the HTTP request to retrieve a token.

- HTTP headers: HTTP headers for the token URL request in JSON or as a JSON body. Use format: "Key1"="Value1","Key2"="Value2".

- Token format: Text or JSON with the Token field name for the name of the field in the JSON response that contains the token.

- Token field name: The name of the field in the JSON response that contains the token. This field appears only when the Token format is JSON.

- Token type: AWS Signature Version 4 request, Google OAuth 2.0 access token, ID token, JSON Web Token (JWT), or SAML 2.0.

## Server proxy (optional)
{: #server_proxy_google_big_query}

Select **Server proxy** to access the Google BigQuery data source through an HTTPS proxy server. Depending on its setup, a proxy server can provide load balancing, increased security, and privacy. The proxy server settings are independent of the authentication credentials and the personal or shared credentials selection.

- Proxy host: The hostname or IP addess of the HTTPS proxy server. For example, proxy.example.com or 192.0.2.0.

- Proxy port: The port number to connect to the HTTPS proxy server. For example, 8080 or 8443.
- Proxy username and Proxy password.

## Other properties
{: #other_props_google_big_query}

- Project ID (optional) The ID of the Google project.

- Output JSON string format: JSON string format for output values that are complex data types (for example, nested or repeated).

  - Pretty: Values are formatted before sending them to output. Use this option to visually read a few rows.
  - Raw: (Default) No formatting. Use this option for the best performance.
  
- Metadata discovery: The setting determines whether comments on columns (remarks) and aliases for schema objects such as tables or views (synonyms) are retrieved when assets are added by using this 
connection.

## Permissions
{: #permissions_google_big_query}

The connection to Google BigQuery requires the following BigQuery permissions:

- bigquery.job.create
- bigquery.tables.get
- bigquery.tables.getData

Use one of three ways to gain these permissions:

- Use the predefined BigQuery Cloud IAM role bigquery.admin, which includes these permissions;
- Use a combination of two roles, one from each column in the following table; or
- Create a custom role. See [Create and manage custom roles](https://cloud.google.com/iam/docs/creating-custom-roles).

| First role | Second role |
|-------|-------------|
|bigquery.dataEditor| bigquery.jobUser|
|bigquery.dataOwner |	bigquery.user
| bigquery.dataViewer	|  |
{: caption="Predefined roles - Google BigQuery" caption-side="bottom"}

For more information about permissions and roles in Google BigQuery, see [Predefined roles and permissions](https://cloud.google.com/bigquery/docs/access-control).

