---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords: activity tracking events
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Activity tracking events for {{site.data.keyword.wxbia_short}}
{: #at_events}


{{site.data.keyword.cloud_notm}} services, such as {{site.data.keyword.wxbia_full_notm}}, generate activity tracking events. {: shortdesc}

Activity tracking events can report on activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use the events to investigate abnormal activity and critical actions and to comply with regulatory audit requirements.

You can use {{site.data.keyword.atracker_full_notm}}, a platform service, to route auditing events in your account to destinations of your choice. You can do route auditing events by configuring targets and routes that define where activity tracking events are sent. For more information, see [About {{site.data.keyword.atracker_full_notm}}](/docs/atracker?topic=atracker-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

## Events for conversations
{: #events_conv}

| Action | Description |
   |-------|-------------|
   | watsonx-intelligence.conversation.create | Creates a conversation |
   | watsonx-intelligence.conversation.delete | Deletes a conversation |
   | watsonx-intelligence.conversation.update | Updates the conversation when a user changes the name of the conversation |
   | watsonx-intelligence.conversation.list | Lists conversations that the user created in the **Conversations** page|
   | watsonx-intelligence.conversation-message.list | Displays a selected conversation's messages |
   | watsonx-intelligence.conversation-message.send | Posts a message in the conversation when a user asks a question or stops response generation |
 {: caption="List of events for conversations" caption-side="bottom"}
 
