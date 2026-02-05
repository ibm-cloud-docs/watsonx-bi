---
copyright:
  years: 2026
lastupdated: "2026-02-03"
keywords: conversation, scope
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Changing the scope of the conversation
{: #scope}

You can change the scope of a conversation by selecting the data you want to ask about from the list in the input box and entering your question. {: #shortdesc}

{{site.data.keyword.wxbia_full_notm}} uses the selected scope to answer your questions and provide insights. This feature allows you to narrow down the focus of the conversation to selective data sources. 

You can set the scope of a conversation to:

- **All data**  

  Includes data assets, including metrics and uploaded files, in all of the projects that you have access to.

- **Mandatory metrics** 

  These are the metrics that were created for you by your organization and which appear in the **Key metrics** panel.

- **A specific project** 

  You can choose from projects that you created or those that you have access to.

-  **An uploaded file** - You can choose a file that you've uploaded and which has gone through metadata enrichment. 

- **A metric from the Metrics catalog** 

  When you choose to ask a question against a single metric from the **Metrics catalog**, you're automatically taken to **Conversations** with the scope set to the metric you selected.

- **Sample data** - If you installed sample data at the time of setup, you can ask set the scope of the conversation to just the sample data set. You can install sample data at any time from **Configuration and settings**. 

## Selecting scope 
{: #scope_change}

Where applicable, items in the scope list include descriptions to help you understand the context of each item at a glance. 

You can also open any item in a new tab to preview the data before continuing your conversation. For example:

- Launching a project opens the data platform project view, including its assets.

- Launching an uploaded file opens the file view in a new tab for quick review.

By default, the conversation scope is set to **All data**. To change the scope, select an item from the list in the input box. When you choose a specific item, the **All data** option is automatically disabled.

You can focus your conversation on either **All data** or a single item; only one selection can be active at a time.

When you change the scope and ask your question, a message displays in the conversation canvas to confirm the change in the scope. The selected scope remains until you change it again.

Scope change only applies to new questions that you ask. The scope of a previous or a saved conversation doesn't change when you change the scope in the input box.
{: note}
