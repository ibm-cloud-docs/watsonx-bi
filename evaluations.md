---
copyright:
  years: 2026
lastupdated: "2026-10-08"

keywords: evaluations, evaluation questions, SQL, accuracy

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Evaluating data and metrics accuracy
{: #evaluations}
[Cloud]{: tag-blue}

Use evaluations to verify that business questions can be answered accurately by using your enriched data and metrics. An evaluation consists of one or more business questions, each with an SQL query that returns the expected results. The SQL query serves as the reference answer during evaluation.{: #shortdesc}

Before a business question can be used in an evaluation, it must be validated. Validation confirms that the SQL query runs successfully and returns the expected results. Validated questions are marked **Valid** and can be added to one or more evaluations.

When you run an evaluation, watsonx BI answers each business question by using the semantic data model and any available metrics. Metrics provide governed, centralized definitions of business concepts, such as revenue, customer count, or retention rate. Questions that rely on business-specific calculations or definitions might require metrics to produce accurate and consistent results.

Watsonx BI compares the generated answers with the results that are returned by the reference SQL queries to evaluate accuracy.

## Before you begin
{: #prereq_evaluation}

Make sure that:

-  Your project contains:

   - A semantic data model that uses data from a connection. 

   - Metrics, if the evaluation questions rely on business-specific calculations or definitions.

- The questions that you want to evaluate have a validated SQL query and are marked **Valid**.

- You have Editor or Admin access to the project. If you have **View** access to a project, you can view only the details of an existing evaluation and cannot create or edit an evaluation in that project. 


## Creating an evaluation
{: #create_evaluation}

1. From **Data and metrics**, click the **Evaluations** tab.

1. Click **New evaluation**.

1. Enter a name for the evaluation.

1. Click **Select evaluation questions** to add one or more questions to the evaluation. 

   You can [create a new question](/docs/watsonx-bi?topic=watsonx-bi-evaluations#create_question) or select from existing ones. 

1. Click **Run evaluation**.

The evaluation is added to the evaluations list. 

After an evaluation runs, you can view its execution status, run duration, the number of questions that passed, and other evaluation details. You can also: 

-  Open the evaluation to view detailed results, including the questions that passed, failed, or ended with an error. For questions that weren't answered successfully, hover over the **Result** field to see the reason. 

-  Re-run the evaluation to verify the impact of changes to your semantic data model, metrics, or business questions. 

-  Delete the evaluation.

## Creating and managing business questions
{: #create_question}

When you create a business question, you define both the question and the SQL query that provides the expected answer.

1. Click **Manage questions** on the **Evaluations** tab.

1. Click **Add question**.

1. Enter a business question in natural language.

   Example: Which products generated the highest net revenue this year, excluding canceled orders?

1. If your project has more than one semantic data model, select the semantic data model that is associated with the data that you are asking about. 

1. Select the connection that contains the data that is required to answer the business question.

1. Enter an SQL query that returns the expected answer for the question.

1. Run the SQL query to validate it.

1. Save the question.

The validated question is added to the question repository and can be used in multiple evaluations.

From **Manage questions**, you can view, edit, or delete existing questions. To edit a business question, open it or select it, and then choose **Edit question** from the menu.

When you edit a business question, the changes are not applied to existing evaluations that already include that question. Existing evaluations continue to use the version of the question that was included when the evaluation was created. You can use the updated business question in new evaluations.
{: note}


## SQL query requirements
{: #eval_sql}

Each business question must include a valid SQL query. The query result serves as the expected answer and is used during evaluation.

Ensure that the SQL query:

- Accurately answers the business question.

- Returns the expected result set.

- Runs successfully against the associated data source.


## Best practices
{: #best_practices_eval}

- Ensure that the project contains the metrics that are required to answer the evaluation questions.

- Review evaluation results after you add, remove, or modify metrics.

- Rerun evaluations whenever significant changes are made to project data, metrics, or semantic data models.

## Troubleshooting evaluation results
{: #troubleshoot_eval}


The evaluation doesn't return the expected answer

:   If an evaluation consistently fails, verify that the project contains the metrics that are needed to answer the question. If a question depends on business-specific logic, create or update metrics to ensure that watsonx BI uses consistent definitions and calculations.

:   For example, consider a streaming service dataset that contains user information, viewing history, and geographic data. A data analyst might create evaluation questions such as:

:   - How many users under 18 are in Canada?
:   - How many users worldwide watched Hannah Montana?
 
:   These business questions have clear answers that can be expressed in SQL. During evaluation, the SQL query that is provided serves as the expected answer. The evaluation compares the results that are generated by watsonx BI with the results that are returned by the reference SQL query.

:   If the required business logic isn't represented in the semantic data model or metrics, watsonx BI might not generate the expected answer. Adding or refining metrics can improve evaluation accuracy and help establish a consistent source of truth for commonly asked business questions.

The evaluation failed

:   Confirm that:

:   - The project contains a semantic data model that uses data from a connection.
:   - The associated connection is available.
:   - The evaluation contains at least one valid business question.
:   - Required metrics and enriched data are present in the project.

The SQL query returns different results than watsonx BI

:  Review the SQL query and ensure that it reflects the intended business logic. Differences can occur when filters, aggregations, date ranges, or joins in the reference SQL query don't match the logic that is represented in the semantic data model or metrics.
