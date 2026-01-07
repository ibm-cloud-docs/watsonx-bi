---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: dremio

subcollection: watsonx-bi

---
{{site.data.keyword.attribute-definition-list}}

# Dremio
{: #dremio}

Dremio is an open data lake platform. It supports all the major third-party data sources. You can connect to an instance on Dremio Cloud or Dremio Software (on-prem). {: #shortdesc}


## Supported versions
{: #supp_dremio}

Dremio 25

## Create a connection to Dremio
{: #create_dremio}

To create the connection, you need these connection details:

- Hostname or IP address: You can create a Dremio Cloud instance only in the European Union (EU) or the United States (US). Use "data.eu.dremio.cloud" for the EU and use "data.dremio.cloud" for the US. Dremio Software can be hosted anywhere.

- Port number: The default port for Dremio Cloud instances is 443 and for Dremio Software it is 32010.

- Authentication method:

  - To connect to Dremio Cloud, you need to use a Personal Access Token for authentication. Select **Port is SSL-enabled** and enter the Personal Access Token. To generate a Personal Access Token, see the instructions [Personal Access Tokens for Dremio Cloud](https://docs.dremio.com/cloud/security/authentication/personal-access-token/){: external}.

  - To connect to Dremio Software, you can use a username and password or you can use a Personal Access Token for authentication. To use a Personal Access Token, select **Port is SSL-enabled** and enter the Personal Access Token. To generate a Personal Access Token, see the instructions [Personal Access Tokens for Dremio Software](https://docs.dremio.com/current/security/authentication/personal-access-tokens/){: external}.

- SSL certificate:
  - Select **Port is SSL-enabled** to connect to Dremio Cloud.

  - Select **Port is SSL-enabled** and enter an SSL certificate if you want to connect to Dremio Software with SSL.

## Dremio setup
{: #setup_dremio}

Dremio can be set up in various deployments, see [Dremio Cluster Deployment](https://docs.dremio.com/25.x/get-started/cluster-deployments/). To set up Dremio Cloud, see [Dremio Cloud](https://docs.dremio.com/cloud/).

## Restriction
{: #restriction_dremio}

You can use this connection only for reading data. You cannot write data or export data with this connection.
