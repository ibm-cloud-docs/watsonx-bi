---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: monitor enrichment, enrichment error, job, log
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# Monitoring enrichment jobs
{: #monitor_enrichment}

You can check the details for any metadata enrichment runs or monitor an active job run by viewing the run metrics. {: #shortdesc}

To view details of a metadata enrichment job that is running during the metric creation process:

1. Click the **View metadata import and enrichment jobs** button. A **Jobs** page opens in a new tab.

2. Select the metadata enrichment job that you want to review.

3. The **Job details** page, shows the number of completed and failed runs, and the configured job schedule.

4. Select a particular run and review the run details. The following run details are provided for a job run:

   - The job run status
   - The duration, start and end times
   - Who started the run
   - A link to the associated job
   - A link to the associated metadata enrichment
   - Basic information about the enrichment settings such as the selected enrichment options, number of categories to use for data class, term, and classification assignment, sampling method used, and algorithms that are used for term analysis and assignment

Here, you can also pause and resume the job run. 

Depending on job type, more information about the actual run is provided on the **Run metrics** and **Log** tabs.

You can also access the details for the most recent metadata enrichment job run from the metadata enrichment asset. You can click the **View metrics** link in the **Job details** section in the information panel or the **Details of job run** link in the asset details panel.

## Understanding the run details
{: #understanding_run}

On the **Run metrics** tab in the job run details, you can monitor the progress of an active run of the metadata enrichment job or check the status information for a completed job run.

The **Summary** section shows the overall progress of the enrichment:

- The total number of assets that were enriched.

- The numbers of completed, in progress, and failed - assets. For failed assets, a link to the failure details is provided.

- The percentage of assets for which enrichment is done.

The **Objectives** section shows the progress for the individual enrichment options in the order in which they are processed.

In addition to the progress bar for the overall process of each enrichment task, you can see how many data assets are in which status while the task is processed. A data asset can have these statuses:

- In progress: The asset is being processed or waiting to be processed.

- Completed: The enrichment task is successfully completed for the asset.

- Skipped: The asset was not processed because a prerequisite enrichment task failed. For example, term assignment might require profiling depending on the selected algorithms. During profiling, assets cannot have this status because profiling is usually the first step in an enrichment process.

- Failed: The enrichment task failed for the asset. If the count is not zero, you can click the number to see details about the failures.

For the **Analyze relationships** enrichment objective, the total number of tasks, the number of completed tasks, and the number of tasks with errors are shown. The total number of analysis tasks depends on the number of data assets that are analyzed. For every 1,000 data assets, an analysis task is created for calculating potential relationships.

For paused enrichments, the details on the dashboard are hidden for the time of the pause. On resuming the enrichment, the initial details reflect the enrichment status at the point of pausing the enrichment. While a job run is paused, the log might provide more detailed information about the actual status than the dashboard.

For canceled enrichments, the details reflect the enrichment status at the point when the run was canceled. 

## Understanding the job run log
{: #understand_run_log}

Logs are provided for all types of metadata enrichment jobs. To view the log for a job run, switch to the **Log** tab on the **Job run details** page. The log shows the job type, the job run ID, and details depending on the enrichment tasks.

-  The entry **Full metadata enrichment job run** or **Delta metadata enrichment job run** indicates a basic metadata enrichment job that is run with the configured enrichment options. 

   Full means that the enrichment is run on all data assets in the scope or on a manually selected set of data assets. Delta means that only those data assets are enriched that were added or modified after the last run of the enrichment, or for which the previous enrichment failed or was canceled. The scope of reruns determines whether a full or a delta metadata enrichment is run.

   For a metadata enrichment job, an asset summary and statistics for each enrichment task is shown. In addition, some details about the used term assignment model are included.

   You can pause and resume runs of this job type. The job run log then contains an entry that shows the start and end time of the pause. Only the last pause is listed in the log even if the job run was paused several times.

- The entry **Advanced profiling metadata enrichment job run** indicates a job for generating more accurate profiling results. In the dashboard, this type of job run is shown as **Profile data** task.

- The entry **Key analysis job run** indicates a job for key or relationship analysis. The type of analysis is identified by one of these entries:

   - Primary key detection task (taskID) 

   - Foreign key relationship detection task (taskID) 
   - Overlap key detection task (taskID) 

   No run details are provided for this job type.

If the list of errors in a metadata enrichment run is exceptionally long, only part of the job log might be displayed in the UI. In this case, download the entire log and analyze it in an external editor.
