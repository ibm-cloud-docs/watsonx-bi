---
copyright:
  years: 2026
lastupdated: "2026-02-03"
keywords: download, download response, share resposne
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}



# Downloading responses and data from a conversation
{: #download_response}

You can download the answer and its associated components, such as visualizations, tabular data, and diagnostic information, that were generated in response to your current question. This feature helps you save and share insights from your queries. {: #shortdesc}

You can download the following components of a generated response:

| **Content type**      | **Definition** | **File format** |
|------------------------|-----------------|-----------------|
| **Text response**      | The text answer generated in response to your question. Only the text answer is downloaded. Visualizations generated with the response and insights are not included. | `.txt` |
| **Visualizations**      | The chart generated to answer your question. If you're using Chain of Thought reasoning, multiple visualizations might be generated to answer your question, which you can download at the same time. Insights are not included. |`.png` |
| **Tabular data**       | Tabular data is the data table used by the large language model to generate the response. |`.csv` |
| **Diagnostic information**    | Diagnositc information includes details such as the steps the AI took to respond, associated SQL, and the response ID (or Support ID). Only Data analysts can download diagnostic information. 
{: note}| `.json` |

If you select multiple components, a ZIP file with the chosen items downloads. 

## Limitations
{: #limitations_download_response}

- You can download content only from a response where the large language model (LLM) generated a query. 

- Only Data analysts and administrative users can download diagnostic information. 

- You cannot upload a tabular data file that was downloaded from a response to generate insights. 

