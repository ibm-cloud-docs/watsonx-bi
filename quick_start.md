---
copyright:
  years: 2024
lastupdated: "2025-06-26"

keywords: quick start, provision, setup
subcollection: watsonx-bi

content-type: tutorial

---

{{site.data.keyword.attribute-definition-list}}


# Provisioning and setting up watsonx BI
{: #getting-started}
{: toc-content-type="tutorial"}

As an IBM Cloud account owner or Administrator, you sign up for IBM watsonx BI in the IBM Cloud account. {: #shortdesc}

These steps describe the typical tasks for an IBM Cloud account owner to set up the account for an organization:

## Step 1: Provision watsonx BI in your Cloud account
{: #step1}

You can provision watsonx BI by creating an instance of the service in your IBM Cloud account.

1. Log into your IBM Cloud account. 

2. Click **Create resource**.

3. Select **watsonx BI** from the catalog.

4. Accept the license agreement checkbox and click **Create**. 

The new service instance appears under **AI/Machine learning** in the **Resource list**. 

## Step 2: Set up watsonx BI
{: #step2}

You need to set up watsonx BI before other users that you invite to your Cloud account can use watsonx BI. 
{: requirement}

1. From the **Resource list**, select and launch the watsonx BI instance. 

2. Click **Start setup**.

3. Select a [Cloud Object Storage](https://dataplatform.cloud.ibm.com/docs/content/svc-welcome/cloud-object-storage.html?context=cpdaas&context=cpdaas&context=dph&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=dph&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=analytics&context=dph&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=analytics&context=dph&context=cpdaas&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=dph&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=dph&context=cpdaas&context=cpdaas&context=cpdaas&context=analytics&context=analytics&context=analytics&context=analytics&context=analytics&context=cpdaas&context=analytics&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=analytics&context=dph&context=analytics&context=analytics&context=cpdaas&context=analytics&context=cpdaas&context=cpdaas&context=cpdaas&context=analytics&context=cpdaas&locale=en&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp&audience=wdp%253Fcontext%253Dcpdaas){: external} instance and click **Next**.  

4. (Optional) Choose a [sample](/docs/watsonx-bi?topic=watsonx-bi-using_samples) to set up in your watsonx BI instance. 

5. (Optional) Invite members to use your instance of watsonx BI.

During the instance setup, watsonx BI enables access delegation for the selected Cloud Object Storage instance. This grants any user of your account the permission to create their own projects and build their metrics.
{: note}

When you use watsonx BI, make sure that the selected account in the account switcher in the header is the one that has access to watsonx BI. 

## Troubleshooting
{: #troubleshooting_setup}

 Here's a look at how to troubleshoot errors that you might encounter as you set up watsonx BI:

- **Error: You don't have access to watsonx BI. Contact your administrator to request access.**

  You or a user you invited to the Cloud account might see this error if: 

  | Scenario | Action  |
  |-------|-------------|
  | As a Cloud account owner, you do not have access to watsonx BI | Follow Steps 1 and 2 above to provision an instance and set up watsonx BI. |
  | You are part of a Cloud account that does not have access to watsonx BI | The Cloud account owner must provision an instance of watsonx BI in the account and set it up before you can use watsonx BI (Steps 1 and 2 above). |
  | You are part of a Cloud account with access to watsonx BI but you do not have access| Administrator must give you access to watsonx BI |
  | watsonx BI is provisioned but not set up in the Cloud account | The Cloud account owner must set up watsonx BI before users in the account can use watsonx BI (see Step 2). | 
  | watsonx BI has not been provisioned at all | Follow Steps 1 and 2 above to provision an instance and set up watsonx BI.|
  {: caption="Access errors when setting up watsonx BI " caption-side="bottom"}


- **Error: Unable to connect to watsonx BI with the current account [account name]. If this is the one you want to work with, please contact your administrator. Itherwise select the right one from the account list in the header.**

  You or a user you invited to the Cloud account might see this error if: 

   | Scenario | Action  |
   |-------|-------------|
   | You are a part of a Cloud account with access to watsonx BI, but your access was removed | The Cloud account owner can assign access to you for watsonx BI.|
   | You are a part of the Cloud account with access to watsonx BI but watsonx BI has not been set up on the account| The Cloud account owner must set up watsonx BI before you can use it (see Step 2).|
   |You are a part of multiple Cloud accounts and are trying to use watsonx BI with an account that doesn't have access | Select the right account in the account switcher that has access to watsonx BI and try again.
   {: caption="Access errors when setting up watsonx BI " caption-side="bottom"}

## Next steps
{: #next_provision}

- [Adding users to the account and assigning roles](/docs/watsonx-bi?topic=watsonx-bi-add_users_account)

- [Roles and permissions in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-roles)
