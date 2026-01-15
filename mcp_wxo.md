---
copyright:
  years: 2025
lastupdated: "2026-01-15"

keywords: mcp, model context protocol, watsonx Orchestrate
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# IBM watsonx BI remote Model Context Protocol (MCP) server
{: #remote_mcp}

IBM watsonx BI remote MCP server is a Model Context Protocol (MCP) compliant service that seamlessly connects AI agents with data in watsonx BI, enabling intelligent data and insight retrieval. 
{: #shortdesc}

A remote MCP server is hosted on IBM infrastructure and accessed over a network, making it easier to collaborate and reduces the need for manual setup and configuration.

Key features:

- **Access to the watsonx BI semantic layer**

  Access data grounded in the watsonx BI semantic layer and governed metric definitions.

- **Natural language interface**

  Query data in watsonx BI using natural language and receive responses with tabular data (data rectangle).


## Capabilities 
{: #capabilities_mcp}

The remote MCP server exposes one static tool:

**Tool name**: QUERY_DATA

**Description**: Search for data and insights from your enterprise data warehouse

**Requires**: Question in natural language used as an input to the QUERY_DATA tool

**Provides**: Description, data, and SQL


## Prerequisites
{: #prereq_mcp}

Before you use the remote MCP server, make sure that you have the following:

- Valid access credentials ([API key](/docs/account?topic=account-userapikey&interface=ui){: external}) 

- AI agent framework that supports the MCP protocol

- A working environment of watsonx BI with:
   - At least one project 
   - Enriched data assets  
   - AI model - Meta Llama 4 and IBM Granite-3-8b-instruct with [Chain of Thought reasoning](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external} 


## Connecting to the remote MCP Server
{: #connect_mcp}

Use the following endpoint to connect your AI agent to the watsonx BI remote MCP server:

[https://dataplatform.cloud.ibm.com/wxbi/v1/mcp](https://dataplatform.cloud.ibm.com/wxbi/v1/mcp){: external}

## Integrating with IBM watsonx Orchestrate
{: #integration_orchestrate}

The watsonx BI remote MCP server integrates with IBM watsonx Orchestrate. For more information, see the following: 

-	[MCP servers in IBM watsonx Orchestrate](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=tools-mcp-servers){: external}
-	[Importing tools from an MCP server in watsonx Orchestrate](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=servers-importing-tools-from-mcp-server#import-tools-MCP-server){: external}

## Limitations of remote MCP Server
{: #limitations_mcp}

-	Supports business intelligence queries only; asset overview questions are not supported
-	Responses are textual and include tabular data only
-	Visualizations are not supported
