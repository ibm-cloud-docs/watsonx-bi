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

[Cloud]{: tag-blue} 

At the time of setting up watsonx BI, Administrators can choose the large language model (LLM) that is used in watsonx BI conversations for users in their organization.  {: #shortdesc}

As an Administrator, you can choose between the following:

- A combination of [Meta Llama 4](https://www.llama.com/docs/model-cards-and-prompt-formats/llama4/){: external} and IBM Granite-3-8b-instruct (Recommended)

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external}

The selected LLM name displays in the **AI** icon in **Conversations**. You can also view the LLM that was used to generate a query in response to your question under **Steps taken by AI**.

The ability to choose the large language model is not available in watsonx BI on IBM Software Hub 5.2.0. Watsonx BI on Software Hub 5.2.0 uses [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} to respond to your questions.
{: note}

## AI explainability
{: #ai_exp}

The **AI** icon in the user interface gives an overview of how AI works in **Conversations**. The LLMs are used by watsonx BI to provide recommendations, insights, and summaries for your governed business data.

Governed business data is data that has gone through different processes, policies, and standards to define the availability, quality, and security of the data. These processes and standards determine the intended use of the organization's data, data owners, and data security measures. 
{: note}

To respond to your BI question, the LLM analyzes and helps interpret your input. 

It can then match the interpreted input to your business data (such as column names, measures, or filters) and generates a query to retrieve the matched information to respond to your input. 

The LLM generates a text-based response, visualization, or both based on the matched information to respond to your question. You can see each of these steps under **Steps taken by AI**.

The LLM also monitors key metrics and helps to identify changes in the business data. Accordingly, the AI can analyze identified changes and update your metrics . When you click a metric in the **Key metrics** panel to open it, notice that the AI can summarize and help explain the identified changes in your metrics.
