---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: cognos analytics, cognos, FM
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Connecting to on-premises resources with Satellite Connector
{: #satellite}

You need a [Satellite Connector](https://cloud.ibm.com/docs/satellite){: external} to securely connect {{site.data.keyword.wxbia_short}} as a Service to an on-premises resource. A Satellite Connector is a deployment model that enables only the secure communications from IBM Cloud to on-premises resources with a light-weight container that is deployed on your container platform hosts, such as Docker hosts. {: shortdesc}

## Prerequisites
{: #prereq_satellite}

- You must have Administrator access to the Satellite service in IAM access policies (assigned in **Access (IAM) > Users**):

   - Service: Satellite

   - Roles and actions: 

      - Satellite Cluster Creator 
      - Satellite Link Administrator
      - Satellite Link Source Access Controller

- You must be assigned to a user group. The user group name is required to create a Satellite Connector (Resource group field).

- You need to ensure that your environment meets the [minimum requirements](https://cloud.ibm.com/docs/satellite?topic=satellite-understand-connectors&interface=ui#min-requirements){: external} to run the Satellite Connector agent.

### 1. Create a Satellite Connector
{: #_step1_create_satellite_conn} 

Creating a Satellite Connector is the first step in establishing a connection.

1. From {{site.data.keyword.satelliteshort}} console{: external}, click **Create connector**.

2. Enter a unique name for your Connector. The default value is connector.

4. (Optional) Enter one or more tags that can help you organize resources throughout your account by filtering by tags from your resource list. 

5. Assign a resource group to your connector. The default value is Default.

6. (Optional) Describe what this Connector is used for. 

7. For **Managed from**, select **Dallas**.

8. In the **Summary** panel, review your order details, and then click **Create connector**. {: #create-connector-steps}

   You might see an error after creating the connector. You can ignore this error and proceed.
   {: note}

Under the list of Connectors, you can see the connector that you created. You might need to click **Refresh** to update the list of connectors

### 2. Create user endpoint
{: #step2_user__endpoint}

After creating a connector, you must set up an agent.

1. Click the connector that you created. 

2. Copy the connector ID for use later.

3. Click **Create endpoint**. 

4. Click **Agent location** and click **Next**.

5. Enter the following **Resource details** and click **Next**:

      - A name for the endpoint

      - Destination FQDN or IP - enter **w.ibm.com** in this field.

      - Destination port - enter **443** in this field,

6. On the **Protocol** tab, enter **TLS** in the **Source protocol** field and click **Next**.

7. On the **Connection settings** tab, set the inactivity timeout to **600** and click **Create endpoint**. 

8. You can now see the newly created endpoint. Click the endpoint to copy the **Endpoint address**. 

   This endpoint address is the cloud endpoint to access the on-premises service (such as Cognos Analytics) and is required later. 

### 3. Create a service ID
{: #step3_serviceID}

1. Navigate to Access (IAM) from your Cloud account or from the Navigation menu in {{site.data.keyword.wxbia_short}}. 

2. Under **Service IDs**, click **Create service ID**.

3. Enter a name for the service ID. 

4. Under API keys, click **Create** to create API keys for this service ID. 

5. Enter the following information and click **Create**.

   a. Enter a name for the API key.

   b. In the **Leaked action** field, select **Disable the leaked key**. 

6. Download the API key file for use later. This API key is used by the Connector agent.

### 4. Install agent
{: #step4_inst_agent}

Each Satellite Connector needs at least one agent running on the remote location to establish a secure connection to a data source. You can install the agent as a Docker image.

You need to ensure that your machine has docker that is installed or snap install docker.

1. Run the installation command to install ibmcloud CLI. 

   curl -fsSL https://clis.cloud.ibm.com/install/linux | sh    

2. After installing the ibmcloud CLI, use the following plug-ins:

   ```
   ibmcloud plugin install ks
   ```
   {: codeblock}

   ```
   ibmcloud plugin install cr
   ```
   {: codeblock}

3. Download oc client on local from https://mirror.openshift.com/pub/openshift-v4/clients/ocp/4.10.8/.

   ```
   scp openshift-client-linux.tar.gz root@epmsatelliteagent1.fyre.ibm.com:/tmp
   ```
   {: codeblock}

3. Extract file openshift-client-linux.tar.gz.

   ```
   tar zxvf /tmp/openshift-client-linux.tar.gz
   ```
   {: codeblock}

4. Move oc and kubectl into user/bin directory

   ```
   mv oc /usr/bin
   mv kubectl /usr/bin
   ```
    {: codeblock}

5. Create two configuration files in the following file structure: 

   - /root/agent/env-files
   - env.txt
  

 6. The agent configuration file (env.txt) has the following parameters: 

      ```
      SATELLITE_CONNECTOR_ID
      SATELLITE_CONNECTOR_IAM_APIKEY
      SATELLITE_CONNECTOR_REGIONh 
      SATELLITE_CONNECTOR_TAGS
      ```
      {: codeblock}

      | Parameter | Required | Description
      |-------|-------------|---------|
      |SATELLITE_CONNECTOR_IAM_APIKEY| Y | Your service id API key. For security purposes, the API key is stored in a file named apikey. Set this parameter to the location of the apikey file. For example, SATELLITE_CONNECTOR_IAM_APIKEY=/agent-env-files/apikey|
      |SATELLITE_CONNECTOR_ID | Y | The ID of the Satellite Connector that the agent is bound to. | 
      |SATELLITE_CONNECTOR_TAGS| N | A string that identifies your agent. This string can be any value that you find useful. |
      |SATELLITE_CONNECTOR_REGION	| Y | Specifies the region for the nearest Satellite Connector data center. For {{site.data.keyword.wxbia_short}}, the valid SATELLITE_CONNECTOR_REGION value is: us-south Dallas, TX, USA |
      {: caption="Configuration file parameters"}


7. Pull the agent image by logging in to IBM Cloud® Container Registry or to the repository directly from Docker with your API key.

   ```
   ibmcloud cr region-set icr.io
   ```
   {: codeblock}

   ```
   docker login -u iamapikey -p <your apikey> icr.io
   ``` 
   {: codeblock}

8. Pull the latest version of the published image. 

   docker pull icr.io/ibm/satellite-connector/satellite-connector-agent:latest

9. Run the agent image by viewing the available versions of the agent image: 

   ```
   ibmcloud cr images --include-ibm |egrep -i "tag|satellite"
   ```
   {: codeblock}


10. Start Docker.

    ```
      docker run -d --env-file ~/agent/env-files/env.txt -v ~/agent/env-files:/agent-env-files icr.io/ibm/satellite-connector/satellite-connector-agent:latest
    ```
    {: codeblock}

11. Verify that the tunnel gets established to your Connector by looking at the logs of the container.

      ```
      docker logs CONTAINER-ID
      ```
      {: codeblock}

12. Stop Docker.

      ```
      docker stop CONTAINER-ID
      ```
      {: codeblock}
   

### 5. Verify agent running state
{: #step5r_veryify_agent}

1. Go to [Satellite - IBM Cloud](https://cloud.ibm.com/satellite/overview){: external} and click **Connectors**. 

2. Select the connector that you created earlier. 

   Under **Active agents**, you now see the agent that is running.

3. Go to **User endpoints** to check the endpoint details.

You can also verify through the https://cloud.ibm.com/shell console. Enter: 

```
curl https://c-01.private.us-south.link.satellite.cloud.ibm.com:34115/epm/app-dev/bi/v1/disp
```
{: codeblock}

If you're connecting to Cognos Analytics on Premises and the response contains **developer.cognos.com**, it indicates that the request to the private endpoint reached your {{site.data.keyword.wxbia_short}} account.
 {: tip}

### 6. Invite users to your project
{: #step6_invite}

You can now invite other users to your project. All users in the project can then [create a connection to Cognos Analytics](/docs/watsonx-bi?topic=watsonx-bi-cognos){: external} to import their FM packages. 

For more information, see [Adding collaborators to a project](/docs/watsonx-bi?topic=watsonx-bi-managing_projects){: external}.

