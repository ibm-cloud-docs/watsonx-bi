---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords: HA for watsonx BI, DR for watsonx BI
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}



# Understanding high availability and disaster recovery for {{site.data.keyword.wxbia_short}}
{: #ha-dr}

[High availability](#x2284708){: term} (HA) is the ability for a service to remain operational and accessible in the presence of unexpected failures. [Disaster recovery](#x2113280){: term} is the process of recovering the service instance to a working state.{: #shortdesc}

## High availability 
{: #ha-architecture}

{{site.data.keyword.wxbia_full}} is highly available in the Dallas (us-south) region.

### Responsibilities 
{: #ha_responsibilities}

To find out more about responsibility ownership for using IBM Cloud products between IBM and the customer, see [Shared responsibilities for IBM Cloud products](/docs/overview?topic=overview-shared-responsibilities){: external}.

### What level of availability does IBM Cloud offer?
{: #ha_avail}

The level of availability that you set up for your cluster impacts your coverage under the IBM Cloud high availability service level agreement terms. Service level objectives (SLOs) describe the design points that the IBM Cloud services are engineered to meet.

The SLO is not a warranty and IBM does not issue credits for failure to meet an objective. Refer to the SLAs for commitments and credits that are issued for failure to meet any committed SLAs. For a summary of all SLOs, see [IBM Cloud service level objectives](/docs/resiliency?topic=resiliency-slo){: external}.

### Location
{: #ha_loc}

For more information about the available region and data center locations, see [Service and infrastructure availability by location](/docs/overview?topic=overview-services_region).

## Disaster recovery 
{: #disaster-recovery-intro}

If a failure occurs, a failover design is established to keep your resources running without action on your part. 

For more information, see [How IBM Cloud ensures high availability and disaster recovery](/docs/resiliency?topic=resiliency-ha-redundancy#zero-downtime){: external} to learn more about the high availability and disaster recovery standards in IBM Cloud. You can also learn more about [Service Level Agreements](/docs/overview?topic=overview-slas){:    external}.

### Responsibilities
{: #disaster_resp}

To find out more about responsibility ownership for using IBM Cloud products between IBM and the customer, see [Shared responsibilities for IBM Cloud products](/docs/overview?topic=overview-shared-responsibilities){: external}.

### Disaster recovery strategy
{: #disaster_recover}

{{site.data.keyword.wxbia_short_cap}} is a highly available, regional service that runs in the Dallas (us-south) region. {{site.data.keyword.wxbia_short_cap}} exists in multiple availability zone with no single point of failure. Your data that is associated with your instance of {{site.data.keyword.wxbia_short}} is backed up and restored in your IBM Cloud Object Storage bucket.

IBM Cloud has business continuity plans in place to provide for the recovery of services within hours if a disaster occurs.

{{site.data.keyword.wxbia_short_cap}} provides mechanisms to protect your data and restore service functions. Business continuity plans are in place to achieve targeted recovery point objective (RPO) and recovery time objective (RTO) for the service.
