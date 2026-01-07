---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: key concepts, understanding metadata enrichment, semantics
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Understanding metadata enrichment in watsonx BI
{: #concepts_enrichment}



Metadata enrichment is a critical step in watsonx BI that transforms raw data, which often lacks context, into a semantically rich dataset using AI. This process adds business-relevant metadata such as business terms and descriptions, making the data easier to explore and understand. {: #shortdesc}

Before you can ask questions about your data, the data must undergo metadata enrichment. Watsonx BI uses the following enriched metadata to answer questions. 

- Asset name 
- Asset description 
- Column name 
- Column description 
- Column identifier 
- Column data type, usage, aggregate, and nullable fields 
- Sampled columns 

While most of these might already be available in your data, others like asset and column names and descriptions are generated during the metadata enrichment process. 

There are two types of metadata enrichment in watsonx BI:

- Enrichment of assets 

  Enriched assets are used to create the semantic data model and they establish the foundation of business context that is used throughout watsonx BI.

- Enrichment of metric definitions 

  Whenever a new metric is created in the semantic model, watsonx BI also performs an enrichment of this metric. Enrichment at the metric level ensures that any new or modified definitions also carry clear and consistent metadata for conversational analysis.
  
  Metrics are used as a primary source during conversations and enrichment at the metric level does not overwrite what exists in the semantic data model. 

Together, enriched assets and metric definitions, create a transparent and explainable semantic layer, helping you trust and understand the data that you work with. 

Let's take a look at the differences between these enrichment types and how metadata is used by the conversational experience in watsonx BI. 

## Metadata enrichment of assets vs. metrics 
{: #enrichment_assets_metrics}

Metadata enrichment takes place in two areas of watsonx BI. 

1. Enrichment of assets - takes place when you connect to or upload your data. Watsonx BI automatically begins the metdata enrichment process of the selected assets. 

2. Enrichment of metric definitions - takes place automatically when you generate metric definitions. If you create metrics definition manually, you need to export them to kick off metadata enrichment. 

## Enrichment of assets 
{: #enrich_assets_explanation}

Metadata enrichment of assets is associated with the semantic data model and occurs after you connect to or upload your data.

During this process, watsonx BI uses AI to automatically assign business terms, from predefined or custom governance artifacts, and generate business-friendly names and descriptions for these base assets. 

Once enrichment completes, you can review, accept, or edit the AI-generated suggestions before they’re applied to the semantic data model.

You need to accept or edit AI-generated suggestions before they can be used in the semantic data model. If watsonx BI has more than 80% confidence that an AI-generated description is correct, it uses the description in the conversation automatically, even without explicit user approval. If the confidence score is below 80%, watsonx BI ignores the AI description and relies on existing metadata instead. 
{: note}

Since these enriched base assets serve as the foundation for the semantic data model and any metrics derived from it, it is worth dedicating time reviewing the metadata enrichment results to ensure that the following metadata is accurate and meaningful: 

- Asset name
- Asset description 
- Column name
- Column description

After metadata enrichment is complete, you can view the resulting semantic data model in the **Advanced mode** from the **Metrics overview** page. 

Metadata such as the column identifier, column data type, usage, aggregate, and nullable fields, and sampled columns are generated and applied to semantic data model automatically. You can make changes to these fields in the properties of the semantic data model. 
{: note}


## Enrichment of metric definitions
{: #enrich_metric_definitions}

You can generate metrics automatically or build them manually after the initial metadata enrichment of assets completes. 

If you're generating metrics automatically, watsonx BI exports the underlying metric definitions and enriches them automatically. If you're building metrics manually, you can export the metric definitions manually, which in turn, starts the metric definition enrichment process.  

Metrics inherit column descriptions that are defined in the enriched base assets. The metric description itself is generated using an LLM to suggest contextual explanations, useful when a metric combines new tables, transformations, or formulas beyond what existed originally. 

### Why enrich metric definitions separately? 

When you create or update metric definitions, they might include new calculations or modifications that were not part of the base assets. Therefore, running enrichment on metric definitions helps ensure that any new logic, relationships, or context introduced at the metric level are also properly described and surfaced in conversations. 

Metadata enrichment on metric definitions run automatically when you generate a metric definition. The metric definition also automatically exports to the project from where it is then used in conversations. When you build a metric definition manually, you need to export the definition, which then starts the enrichment at the metric definition level. 

Metadata enrichment at the metric level does not replace what was defined in the asset level enrichment.
{: important}

Watsonx BI considers metrics as the source of truth when you ask a question in the conversation. So, ensuring metrics are well defined helps improve accuracy. 

 
