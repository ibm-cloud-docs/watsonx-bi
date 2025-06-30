---
copyright:
  years: 2024
lastupdated: "2025-06-26"

keywords: publish metrics
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Publish metrics (Data analysts only)
{: #publish_metrics}

As a Data analyst, you can publish metrics to the **Metrics catalog** and specify access permissions. Analytics consumers  can access metrics, which they have permissions to view without having to access the full project. {: #shortdesc}

1. From the **Data and Metrics** tab, open the semantic model with the metrics that you want to publish.

2. On the **Metrics overview** page, click **Publish metrics**.

3. Select the metrics and associated visualizations that you want to publish. 

4. Specify who can access the published metrics and add users. 

5. Click **Publish**.

You can view the published metrics in the **Metrics catalog**. 

From the **Metrics catalog**, you can now assign metrics to an Analytics consumer. Assigned metrics appear in the Analytics consumer's **Key metrics** panel where they can monitor changes in the data.

Analytics consumers can also view details of the metrics they have access to and pin them from the **Metrics catalog** to their **Key metrics** panel. For more information, see [Pinning metrics to Key metrics](/docs/watsonx-bi?topic=watsonx-bi-pin_metric){: external}. 

## Assigning metrics to Analytics consumers or Data analysts
{: #assign_metrics}

1. In the **Metrics catalog**, select the metric you want to assign to an Analytics consumer. 

2. Select the visualization that will display in the Analytics consumer's **Key metrics** panel and click **Assign to members**.

3. Select the users that you want to assign the metric to and click **Save**. To add new users and groups, click **Add members**.

## Pinning to Key metrics
{: #pin_metrics}

If you're a Data analyst, you can also pin metrics to your own **Key metrics** panel. 

1. In the **Metrics catalog**, select the metric you want to pin. 

2. Select the visualization that will display in the **Key metrics** panel and click **Pin to Key metrics**.

Analytics consumers can also pin metrics from the **Metrics catalog** to their **Key metrics** panel in the same manner.
{: note}
