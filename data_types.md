---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: upload file, local file

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Validating data types before casting
{: #data_type_conversion}

Whether you connect to remote data in watsonx BI or work with an uploaded file, you might need to convert the values in your data to a different data type using the CAST function. {: #shortdesc}

If a value is stored in a character data type, the value has to be in specific formats for the CAST to be successful. Otherwise, the CAST function results in an error. 

The question that arises is, how do you validate data types before you CAST them.

## Expected data formats
{: #expected_data_formats}

- DATE YYYY-MM-DD   

  Where YYYY is from 0001 to 9999, MM is from 01 to 12, DD is from 01 to the last day of the month

- TIME HH:MI:SS[.fff]   

  Where HH is from 00 to 23, MI is from 00 to 59, SS is from 00 to 59 and fraction seconds from 0  

- TIMESTAMP YYYY-MM-DD HH:MI:SS[.fff] 

  Where same requirements of DATE and TIME parts apply

- NUMERIC 

  Values must be INTEGERS (such as 0, 123), DECIMAL (0.0, 23.45), or DOUBLE (1.0E0) with an optional leading (+ or -) sign

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

Conditionally converting the values requires a test that attempts to determine if the string value is in an appropriate format or not. You can use an expression in watsonx BI's modelling interface that leverages regular expression (REGEX) to validate if a value matches the ISO SQL format. 

You can then convert values that don't match the ISO SQL format. 

### Validate NUMBER and CAST
{: #validate_number}

Numeric values can have complex formatting that includes currencies, percentage signs, units of measure and other local specific usage of separators.

Use REGEX to check if a string matches the ISO SQL format before casting. 

IS_A_NUMBER is an expression that returns N when the string does not follow ISO-SQL literal format for a numeric. 


```
case when 0 = occurrences_regex ( '^[+-]?\d*\.?\d+(?:[eE][+-]?\d+)?$', VAL ) then 'N' else 'Y' end

```
{: codeblock}

You can conditionally convert the values that are not valid numbers to 0, for example, to represent an unknown number versus a null value. 

```
case when 'Y' = IS_A_NUMBER then CAST ( VAL, <numeric-type> ) else CAST ( NULL, <numeric-type> ) end
```
{: codeblock}


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


### Extracting a numeric value from a string
{: #extract_numbers}

Numeric values are more likely to include additional formatting including labels such as currencies or units of measure.

The REGEX support in dynamic query includes SUBSTRING_REGEX. It does not, however, support the means to specify which subgroup in a REGEX to retrieve.

The following example uses a less than obvious REGEX solution that does not use a subgroup.

```
substring_regex ( '(?<=[+-]?\s*)\d*\.?\d+(?:[eE][+-]?\d+)?(?=\s*(?:[A-Za-z]{2,4}|[^\w\s])?\b)', VAL  )
```
{: codeblock}


| Row ID | RNUM | VAL | Extract_Numeric_Part|
|-------|--------|------|-------------|
| 1 | 1 | 123| 123 |
| 2| 2| -456| 456|
| 3 | 3 | $1.23| 1.23|
| 4| 4| Plan missing | Null|
|5 | 5| **00| 00|
|6| 6| CDN 30| 30|


This approach attempts to remove some of the text that precedes or follows a numeric value but does not consider cultural (locale) specific methods of representing decimal places and thousand separators.

