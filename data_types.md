---
copyright:
  years: 2025
lastupdated: "2025-10-10"

keywords: upload file, local file

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Validating data types before CASTING for improved query generation
{: #data_type_conversion}

Whether you connect to remote data in watsonx BI or work with an uploaded file, you might need to convert or CAST column data from one type to another to ensure compatibility and improve query generation. {: #shortdesc}

The question that arises is, how do you validate data types before you CAST them.

## Examples of data type issues that can cause query failure
{: #example_issues}

Here are two examples of data type issues that can cause query generation to fail in watsonx BI:

**Formatting changes DATE data type to INTEGER**

You are working with a file which has data values that are dates. 

The application that exported the data might have formatted the string in such a way that the resulting values aren't true dates. For example, a date formatted to an integer "20250100". 

To remediate this issue, you need to CAST the values to DATE data type.

**Column values are of mix data types**

Your data has column values that include more than one data type:

|Value| 
|----|
|1.23|
|5|
|6.0|
|$23.5|
|Plan missing|
|99.0+|

To remediate this issue, you need to convert or CAST all of these values to one data type. 

## Validating data types and casting conditionally
{: #data_validation_casting}

You can use an expression in watsonx BI's modelling interface that leverages REGEX to validate if a value matches the ISO SQL format. 

You can then convert values that don't match the ISO SQL format. 


### Validate DATE and CAST
{: #validate_date}

Use REGEX to check if a string matches the ISO SQL date format before casting. 

REGEX checks the date range but does not factor in leap years.
{: note}

IS_A_DATE is an expression that returns N when the string does not follow ISO-SQL date literal format.


```
case when 0 = occurrences_regex ( '^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01])$', VAL) then 'N' else 'Y' end 
```
{: codeblock}

You can conditionally convert the values that are not dates to 0001-01-01, for example, to represent an unknown date versus a null value. 

```
case when 'Y' = IS_A_DATE then CAST ( VAL, DATE ) else CAST ( NULL, DATE ) end
```
{: codeblock}


### Validate TIME and CAST
{: #validate_time}

Use REGEX to check if a string matches the ISO SQL time format before casting.

IS_A_DATE is an expression that returns N when the string does not follow ISO-SQL date literal format.

```
case when 0 = occurrences_regex ( '^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01])$', VAL) then 'N' else 'Y' end 
```
{: codeblock}

You can conditionally convert the values that are not TIME data type to 00:00:00, for example, to represent an unknown time versus a null value.

```
case when 'Y' = IS_A_TIME then CAST ( VAL, TIME ) else CAST ( NULL, TIME ) end
```
{: codeblock}


### Validate TIMESTAMP and CAST
{: #validate_timestamp}

Use REGEX to check if a string matches the ISO SQL timestamp format before casting.

IS_A_TIMESTAMP is an expression that returns N when the string does not follow ISO-SQL date literal format. 

```
case when 0 = occurrences_regex ( '^(?:[1-9]\d{3}-(?:(?:0[1-9]|1[0-2])-(?:0[1-9]|1\d|2[0-8])|(?:0[13-9]|1[0-2])-(?:29|30)|(?:0[13578]|1[02])-31)|(?:[1-9]\d(?:0[48]|[2468][048]|[13579][26])|(?:[2468][048]|[13579][26])00)-02-29) (?:[01]\d|2[0-3]):[0-5]\d:[0-5]\d(?:\.\d+)?$', VAL     ) then 'N' else 'Y' end
```
{: codeblock}

You can conditionally convert the values that are not timestamps to 0001-01-01 00:00:00, for example, to represent an unknown timestamp versus a null value.

```
case when 'Y' = IS_A_DATE then CAST ( VAL, DATE ) else CAST ( NULL, DATE ) end
```
{: codeblock}


