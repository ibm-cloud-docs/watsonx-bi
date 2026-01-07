---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: upload file, local file

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Uploading a file
{: #upload}

You can upload supported file types to a project in {{site.data.keyword.wxbia_short}} and use it as a source of data to ask questions in **Conversations**. {: #shortdesc}

When you upload your file, the first 1000 rows of the file are scanned to determine metadata, such as column names and data types. Then, additional [enriched metadata](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external} is created by using the data in the file. After enrichment is complete, you can start asking questions about the data in the file. 

If the first 1000 rows are empty, these rows are treated as varchar or string columns in the query engine, even if numeric values exist in the subsequent rows. Empty rows might lead to errors when a query processes SUM on a varchar column. To avoid this issue, before you upload, sort the file so that the first 1000 rows are not empty and the data type can be correctly identified and treated.
{: tip}

You can find your uploaded files on **Data and Metrics > Data sources > Uploaded files** tab. They are also listed as data assets on the **Assets** page of your project.

All uploaded files in {{site.data.keyword.wxbia_short}} as a Service are stored in the Cloud Object Storage bucket that is associated with your project.
{: note}

## Uploading a file
{: #steps_upload}

1. Click the upload icon in the input box on **Conversations** or go to **Data and metrics > Data sources > Uploaded files**. 

2. On **Data and Metrics**, select the project that you want to upload the files to. 

3. Browse for the files on your local drive, and select one or more files to upload. You can also drop files into the drop zone. 

   Progress messages appear at different stages of the upload:

    - Preparing -  In this stage, {{site.data.keyword.wxbia_short}} prepares the data in the file for metadata enrichment. 

    - Enriching - The data in the file then undergoes [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich), which adds business context metadata to your data to prepare it for conversations. 

    - Ready - Metadata enrichment completes successfully.

4. Click the **Review** link to [review the enrichment results](/docs/watsonx-bi?topic=watsonx-bi-review). 
  
    Metadata enrichment adds business context to your data in the form of business terms, labels, and descriptions. Check to make sure that these additions are accurate and meaningful.

    Any changes that you make to the enrichment results save automatically.

   If the uploaded file has more than 10,000 rows, click **Review > Columns > Select a column**. Check the **Statistics** section in the **Details** panel to ensure that data sampling captured the distinct values. If certain columns are fewer than expected, click **Edit enrichment** and change **Sample size** to **Percentage**. Enter **10** in the **Percent of the data set** field and enter **10000** in the **Maximum number of rows** field. Click **Enrich all assets** to re-run enrichment.
   {: important}

5. (Optional) Click **Ask a question** to ask questions about the data in the uploaded file.

When a file successfully uploads to a project, it is listed as a data asset in the project view. 

You can use uploaded files as data sources in the [create metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics) flow and also define relationships between them for more complex, multi-step BI queries that might require data from two or more flat files. For more information, see [Data modeling {{site.data.keyword.wxbia_short}}](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data). 



## Managing uploaded files
{: #manage_file}

**Replacing an uploaded file**

You can update the contents of an uploaded file by adding a file with the same name and format to the project. IBM {{site.data.keyword.wxbia_short}} prompts you to specify whether you want to overwrite the existing file or create a new asset. In both cases, the data in the file undergoes metadata enrichment. 

**Deleting an uploaded file**

To delete an uploaded file, click the **Delete** option from the menu next to the uploaded file name. 

Deleting a file removes it from the project permanently. This action might impact semantic data models that were created with references to the deleted file.
{: important}

## Supported file types 
{: #supported_file}

The upload file feature in {{site.data.keyword.wxbia_short}} supports the following flat files:

### Delimiter-separated value files
{: #delimiter}

The following delimiter-separated value files are supported: 

- Comma separated (CSV)

- Tab separated (TSV)

The first row in the file needs to include the column names for each column in the data. All rows, including the header, need to use the same delimiter: comma or tab.

Column names in delimiter-separated value files must be unique.

Example of a CSV file: 

    Country,City
    Canada,Ottawa
    United Kingdom,London 

### Microsoft Excel files (xls and .xlsx)
{: #excel}

The supported Microsoft Excel file formats include .xls and .xlsx workbook files. 

The Excel file needs to have tabular data, consisting of simple columns with headers followed by the data. Column names in the file must be unique.

Only the data on the first tab of the Excel file is used for metadata enrichment.
{: note}

Excel files that contain the following are not supported: 

- Pivot tables

- Crosstabs
- Images
- Charts
- Merged cells
- Tables inside tables

You can upload an Excel file, which has two or more tabs but the asset preview displays only the first tab.

### Limitations
{: #limitations_uplaod}

- The file cannot be empty.

- The file name can't exceed 255 characters.

- The maximum size for files that you can upload in the user interface is 5 GB. 

- You can upload only 10 files at a time.

## Supported data formats
{: #supp_data_formats}

Each column in the uploaded file is scanned to determine whether it represents a character, numeric (integers, decimal, or double), temporal (date, timestamp, or time), or a Boolean data type. The file upload feature supports each of these data types. 

Supported column data formats include:

- Date data types

    - YYYY-MM-DD

    - YYYY/MM/DD
    - DD-MM-YYYY 
    - DD/MM/YYYY
    - MM-DD-YYYY
    - MM/DD/YYY

- Timestamp data types 

    - YYYY-MM-DD HH:mm:ss

    - YYYY-MM-DD HH:mm:ss.SS
    - YYYY-MM-DDTHH:mm:ss
    - YYYY-MM-DDTHH:mm:ss.SS
   
      Fractional seconds (ss in the pattern) can contain up to nine digits.
      {: note}



- Boolean data type with 'true' or 'false' values

- Values with just digits that represent an integer, big integer, double, or decimal type

- Empty values are treated as null type

Values representing dates and timestamps need to be in the following format:

- Values that represent a month must be between 1-12 

- Values that represent a day must be a valid day in the associated month.

- Values representing an hour must be between 1-24.

- Values representing a minute must be between 0-59.

- Time values that use up to 12 hours can be designated with AM (before noon) and PM (after noon)

- Column names must be unique

## Troubleshooting file upload errors
{: #troubleshooting_upload}

You might run into errors during the file upload process. Click the **View details** link under the error message for more details. 

Some errors can be avoided by revising the file and uploading again. For example, file upload can fail if the file is blank or contains a blank worksheet. File enrichment might fail if it contains a value that doesn't match the data type in the rest of the file, an unsupported data type, or if the file contains one or more rows that have a different number of columns than expected.

Other errors might require you to contact IBM support for further assistance. 

### Common errors
{: #common_upload_errors}

- FLP_InvalidFileType = FLP-101 Invalid file type

  You can run into this error when an unsupported file was uploaded. Only comma separated (csv), tab separated (tsv), and Excel (xls or xlsx) files are supported.

- FLP_UnsupportedDataType = FLP-102 Cannot create table for file ''{0}''. Unsupported type: ''{1}'' for column ''{2}''.Column in the file has a data type that is not supported

  A column in the file has a data type that is not a character, numeric, temporal, or Boolean data type, remove the column from the file and upload it again.

- FLP_ParquetUnsupportedType = FLP-106 Error writing parquet data for file ''{0}''. Unsupported type: ''{1}''.

  A column in the file has data type that is not a character, numeric, temporal, or Boolean data type, remove the column from the file and upload it again.

- FLP_DBUnsupportedTypes = FLP-107 The following data types detected in file ''{0}'' for the given columns are not supported: ''{1}''.

  A column in the file has a data type that is not a character, numeric, temporal, or boolean data type, remove the column from the file and upload it again.

- FLP_DuplicateColumns = FLP-108 Error writing parquet data for file ''{0}''. Duplicate column(s) detected: ''{1}''.

  Duplicate column names in the uploaded file are not supported. Ensure that all column names in the file are unique and upload the file again.

- FLP_ErrorConvertingTimestampTZUTC FLP-127 Invalid format for timestamp with timezone data: ''{0}''.

  A row in the uploaded file has a value in the column that cannot be converted to a timestamp, correct the value or delete the row, and upload the file again. 

### Metadata enrichment errors 
{: #mde_upload_errors}

You might encounter metadata enrichment errors if there is an issue with the data or if an error occurred in an enrichment objective. Examples:
  
- there was an error in profiling data and {{site.data.keyword.wxbia_short}} couldn't retrieve data values to process the metadata enrichment

- {{site.data.keyword.wxbia_short_cap}} was unable to retrieve data values to write and compute vectors to Cloud Object Storage

- {{site.data.keyword.wxbia_short_cap}} was unable to write vectors to Cloud Object Storage

If the file encounters metadata enrichment errors during upload:
  
1. Click the **Review** link to go to the metadata enrichment results.
  
2. Click **Enrich all assets** at the top of the page to re-run enrichment. If there are errors in data profiling or other enrichment objectives, re-running enrichment might resolve the error. 

If the errors persist, click the **View metrics** link in the **About this enrichment** panel to see the enrichment objectives that failed. You can also go to the **Log** tab to view more details. 

Depending on the errors, you might need to fix the data in the file and upload it again. 

