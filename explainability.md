---
copyright:
  years: 2024
lastupdated: "2024-04-26"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Use of AI in Conversations 
{: #explainability}

The **AI** label in the user interface gives an overview of how AI works in **Conversations**. {{site.data.keyword.wxbia_full}} uses large language models (LLM) to answer your questions and provide recommendations, insights, and summaries for your governed business data. {: #shortdesc}

Governed business data is data that has gone through different processes, policies, and standards to define the availability, quality, and security of the data. These processes and standards determine the intended use of the organization's data, data owners, and data security measures.
{: note}

To respond to your BI question, the LLM analyzes and helps interpret your input. It can then match the interpreted input to your business data (such as column names, measures, or filters) and generates a query to retrieve the matched information to respond to your input. 

The LLM generates a text-based response, visualization, or both based on the matched information to respond to your question. You can see each of these steps under **Steps taken by AI**. 

The LLM also monitors key metrics and helps to identify changes in the business data. When you click a metric in the **Key metrics** panel to open it, notice that the AI can summarize and help explain the identified changes in your metrics.



{{site.data.keyword.wxbia_short_cap}} uses large language models (LLMs) that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}
