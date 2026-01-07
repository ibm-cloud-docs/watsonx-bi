---

copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: salesforce api

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Salesforce.com connection 
{: #salesforce_api}

Salesforce.com is a cloud-based software company which provides customer relationship management (CRM). The Salesforce.com connection supports the standard SQL query language to select, insert, update, and delete data from Salesforce.com products and other supported products that use the Salesforce API. {: #shortdesc}

## Supported versions 
{: #supp_salesforce_api}

Salesforce.com version 61.

## Other supported products that use the Salesforce API
{: #use_salesforce_api}

- Salesforce AppExchange
- FinancialForce
- Service Cloud
- ServiceMax
- Veeva CRM

## Create a connection to Salesforce.com
{: #create_salesforce_api}

To create the connection, you need these connection details:

- The username to access the Salesforce.com server.

- The password and security token to access the Salesforce.com server. In the **Password** field, add your security token to the end of your password. For example, "MypasswordMyAccessToken". For information about access tokens, see [Reset Your Security Token](https://help.salesforce.com/s/articleView?id=xcloud.user_security_token.htm&type=5).

- The Salesforce.com server name. The default is "login.salesforce.com".


## Restriction
{: #restriction_salesforce_api}

You can only use this connection for source data. You cannot write to data or export data with this connection.

## Known issue
{: #knownissue_salesforce_api}

The following objects in the SFORCE schema are not supported: 

APPTABMEMBER, CONTENTDOCUMENTLINK, CONTENTFOLDERITEM, CONTENTFOLDERMEMBER, DATACLOUDADDRESS, DATACLOUDCOMPANY, DATACLOUDCONTACT, DATACLOUDANDBCOMPANY, DATASTATISTICS, ENTITYPARTICLE, EVENTBUSSUBSCRIBER, FIELDDEFINITION, FLEXQUEUEITEM, ICONDEFINITION, IDEACOMMENT, LISTVIEWCHARINSTANCE, LOGINEVENT, OUTGOINGEMAIL, OUTGOINGEMAILRELATION, OWNERCHANGEOPTIONINFO, PICKLISTVALUEINFO, PLATFORMACTION, RECORDACTIONHISTORY, RELATIONSHIPDOMAIN, RELATIONSHIPINFO, SEARCHLAYOUT, SITEDETAIL, USERAPPMENUITEM, USERENTITYACCESS, USERFIELDACCESS, USERRECORDACCESS, VOTE.
