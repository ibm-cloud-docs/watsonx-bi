---
copyright:
  years: 2026
lastupdated: "2026-08-06"

keywords: language settings, spanish, AI responses
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Language settings for AI responses
{: #language_settings}

As an Administrator, you can set the language in which watsonx BI generates AI responses for all users in your account. The language setting applies only to AI-generated content. The language in which the user interface displays is determined by each user's browser locale and is not affected by this setting.  {: #shortdesc}

Spanish and Japanese are currently supported as alternative AI response languages.

Support for AI-generated responses in Japanese is a Technology Preview feature. Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important}

By default, watsonx BI generates AI responses in English. You can change the language so that AI-generated output is returned in Spanish or Japanese. The selected language applies account-wide, and all users receive AI-generated responses in that language.

The language setting controls all AI-generated text output including:

- SQL step titles
- AI-generated reasoning steps
- Final answer summaries
- Suggested questions
- Metdata enrichment for new assets

## Limitations and considerations
{: #language_limitations}

Review the following limitations before you change the language setting:

Existing assets are not updated

:  The new language applies only to assets that are created or enriched after you change the setting. Existing assets retain the language in which they were originally enriched.

Mixed-language data can reduce accuracy

:  AI response accuracy can be affected when data is in one language and the filters in a user query are in another language. Ensure that your data language is consistent with the AI response language that you select.

Changes apply immediately to all users

:  After you save the setting, all subsequent AI responses are generated in the new language for all users in the account.

Samples remain in English

:  Samples content is available only in English, regardless of the language selected.


## Setting the language for AI responses
{: #choosing_language}

You can configure the language setting during the initial setup of watsonx BI or at any time from the **AI configuration** page.

You must have administrator access to the account.
{: note}

To set the language for AI responses, complete the following steps:

1. In watsonx BI, go to **Configurations and settings** > **AI configuration**.

2. In the **Language settings** section, select the language in which you want AI to generate responses.

3. Save your changes.

AI responses are now generated in the selected language for all users in the account.
