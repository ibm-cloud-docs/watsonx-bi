---
copyright:
  years: 2025
lastupdated: "2025-07-16"

keywords: watsonx.data
subcollection: watsonx-bi



---

 {{site.data.keyword.attribute-definition-list}}


# IBM watsonx.data
{: #wxd}

IBM watsonx.data is a governed data lakehouse optimized for data and AI workloads. Integrating IBM watsonx BI with watsonx.data brings the ability for any type of data (structured, semi-structured, and unstructured) to be directly accessible for AI and business intelligence, making it easier for data scientists and data analysts to use the data. {: #shortdesc}

IBM watsonx BI and watsonx.data integration support the following connectors:

- IBM watsonx.data Presto

- Presto

## Prerequisites
{: #prereq_wxd}

- A working watsonx BI environment

- A working watsonx.data environment

## Connecting to watsonx.data from watsonx BI
{: #connect_wxd}

You can add a connection from the **Data and Metrics** tab in watsonx BI when you create metrics.

1. On the **Data and Metrics** tab, click **Create metrics** and give your semantic data model a name.

2. On the **Add data** page, click **New connection**. 

3. Select **IBM watsonx.data Presto** or **Presto** from the list of data sources. 

4. Enter the connection information for the connector you chose:

   **IBM watsonx.data Presto**


   | Field | Description |
   |-------|-------------|
   | Name | Enter the name of the connection. |
   | Description | Enter a connection description. |
   | Select the environment | Do not select the checkbox. |
   | Hostname or IP address | Enter the {{site.data.keyword.lakehouse_short}} instance URL. For information about retrieving the Hostname, see [Getting connection information](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-get_connection){: external}. |
   | Port | Enter the port number. For information about retrieving the Port, see [Getting connection information](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-get_connection){: external}. |
   | Instance ID | Enter the instance ID. You can get the instance ID from the {{site.data.keyword.lakehouse_short}} instance home page (information icon). |
   | Instance name | Enter the {{site.data.keyword.lakehouse_short}} instance name. |
   | CRN | Enter the Cloud Resource Name. You can get the CRN from the {{site.data.keyword.lakehouse_short}} instance home page (information icon). |
   | Username | Enter your username (`ibmlhapikey_<EMAIL_ID>`). |
   | Password | Enter your password or IAM API key. To create an API key, see [Creating an API key](https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui#create_user_key){: external}. |
   | SSL is enabled | Select the checkbox. |
   | SSL Certificate | Download the certificate from the watsonx.data console by using a web browser and paste in this field. |
   | Engine's hostname or IP address | Enter the engine hostname available in the {{site.data.keyword.lakehouse_short}} console without port number and `:`. |
   | Engine ID | Enter the engine ID available in the {{site.data.keyword.lakehouse_short}} console. |
   | Engine's port | Enter the engine port number available with the engine hostname. |
   {: caption="New connection with IBM watsonx.data Presto" caption-side="bottom"}


  **Presto**

   | Field | Description |
   |-------|-------------|
   | Name | Enter the name of the connection. |
   | Description | Enter a connection description. |
   | Select the environment | Do not select the checkbox. |
   | Hostname or IP address | Enter the {{site.data.keyword.lakehouse_short}} instance URL. For information about retrieving the Hostname, see [Getting connection information](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-get_connection){: external}. |
   | Port | Enter the port number. For information about retrieving the Port, see [Getting connection information](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-get_connection){: external}. |
   | Username | Enter your username (`ibmlhapikey_<EMAIL_ID>`). |
   | Password | Enter your password or IAM API key. To create an API key, see [Creating an API key](https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui#create_user_key){: external}. |
   | SSL is enabled | Select the checkbox. |
   | SSL Certificate | Download the certificate from the watsonx.data console by using a web browser and paste in this field. |
   {: caption="New connection with Presto" caption-side="bottom"}


5. Test the connection, then click **Create**.

You can now select data from the newly created connection to watsonx.data and continue with the create metrics flow. For more information about creating metrics, see [Overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics). 
