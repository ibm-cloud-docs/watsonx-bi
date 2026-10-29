---
copyright:
  years: 2025, 2026
lastupdated: "2026-10-29"
keywords: conversation, scope, chat, topic, data source
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Changing the scope of the conversation
{: #scope}

You can change the scope of a conversation by selecting the data that you want to ask about from the list in the input box and entering your question. {: #shortdesc}

{{site.data.keyword.wxbia_full_notm}} uses the selected scope to answer your questions and provide insights. This feature allows you to narrow the focus of the conversation to specific data sources.

You can set the scope of a conversation to:



Metrics catalog

:   The **Metrics catalog** is a centralized repository of published metrics that you can access. If you are a Data analyst, metrics that you publish appear here. The conversation scope is set to **Metrics catalog** by default.

A specific project

:   You can choose from projects that you created or projects that you have access to.

Sample data

:   If you installed sample data during setup, you can set the scope of the conversation to the sample data set. You can install sample data at any time from **Configuration and settings**. 

You can also ask questions about an uploaded file or a metric from the **Metrics catalog**. These options don't appear in the scope list by default. 

- To start a conversation about a specific uploaded file, select **Ask a question** for the file from **Data and Metrics > Data sources**. The file must be successfully enriched before it is available for conversation. 

- To start a conversation about a specific metric, select **Ask a question** for the metric from **Metrics catalog**.

In either case, a new conversation opens with the selected file or metric set as the current scope. After the conversation opens, the scope list also includes Metrics catalog, Sample data (if installed), and any projects that you have access to, allowing you to change the scope of subsequent questions as needed.


## Selecting a scope 
{: #scope_change}

Where applicable, items in the scope list include descriptions to help you understand the context of each item at a glance. 

You can also open items directly from the scope list in a new tab to preview them before continuing your conversation. For example:

- Opening a project opens the data platform project view, including its assets.

- Opening Metrics catalog opens displays your metrics in a new tab.

By default, the conversation scope is set to **Metrics catalog**. To change the scope, select an item from the list in the input box. Only **one** selection can be active at a time.

When you change the scope and ask your question, the conversation canvas displays the scope change. The selected scope remains until you change it again.

A scope change applies only to new questions. The scope of a previous or saved conversation doesn't change when you change the scope in the input box.
{: note}

## Limitations
{: #limitations_scope}

- If no published metrics are available, only one suggested question is displayed in the conversation.

- Uploaded files must be successfully enriched before they're available for conversation through Ask a question.

- Uploaded files and metrics can be selected as a conversation scope only when you start a conversation by using **Ask a question** from the corresponding file or metric.
