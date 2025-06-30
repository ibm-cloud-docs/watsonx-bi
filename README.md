Documentation source repository for content published at https://cloud.ibm.com/docs/allowlist/watsonx-bi. This documentation has limited visibility as described in [Allowlisting a subcollection](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-allowlisting).

## Creating content

Follow these steps to contribute to this documentation.

:information_source: **Tip:** If you'd rather give feedback about the documentation, create an [issue](../../issues).

### Before you begin
Set up your local development environment:

- Visual Studio Code is the recommended editor. For more information, see [Choose an editor](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-setting-up-your-markdown-environment#choose-an-editor).
- You can install a Markdown linter in Visual Studio Code that works with IBM Cloud docs. For more information, see [Integrating the Markdown linter in VS Code](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-markdown-linter-vscode).

### Drafting content

All content starts from the `source` branch.

1.  Clone this repo if you have write privileges. Otherwise, fork the repo.
1.  Create a working branch from the `source` branch.
1.  Make your changes to the Markdown content.

    - IBM Cloud docs uses Markdown with a few custom extensions to source the docs. For tips about how to structure and style your docs with IBM Cloud Markdown, see [Authoring content in Markdown](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-create-content-md#create-content-author).
    - IBM Cloud docs also supports controlling content with tagging. For example, content within the <code>&lt;draft&gt;</code>&nbsp;<code>&lt;/draft&gt;</code> tags appears only in the https://test.cloud.ibm.com/docs/allowlist/watsonx-bi location and won't be included in pushes to production, which makes it a good way to preview changes that might not go live for a while. For more information, see [Controlling content with tagging](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-source-tagging).

1.  Commit your updates.
1.  Create a pull request from your branch or fork to `source`. One of this repo's maintainers will review and merge your pull request.

    1.  After the pull request is merged, a Jenkins job runs that commits content to the `draft` branch and opens a pull request to the `publish` branch.
    1.  After a few minutes, you can see your changes in the IBM Cloud docs framework. Changes to `draft` are available in the test location (https://test.cloud.ibm.com/docs/allowlist/watsonx-bi).

        :information_source: **Note:** You must be in an account that's been given visibility to the associated product or global catalog entry to view the docs in the IBM Cloud docs framework. For more information, see [How allowlisting works](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-allowlisting#how-allowlisting-works).
1.  The maintainer will merge the _Next publish push_ pull request.

    The `publish` branch is the final location for your documentation updates, which display in the production location at https://cloud.ibm.com/docs/allowlist/watsonx-bi. When you commit a change to the `source`, a pull request is automatically created from a branch called `next-publish-push` to the `publish` branch to publish your changes.

    The maintainer can then review and merge the pull request to push your changes to production.


## Monitoring

After a build is triggered by a commit or merge, you can monitor progress.

### Monitoring builds

The Slack channel #docs-watsonx-bi displays information about builds.

### Monitoring content quality

Content quality test cases are run against your documentation on a daily basis, and results are posted in your repo's Slack channel. For more information, see [Automated content quality test cases and the Content Quality Dashboard](https://test.cloud.ibm.com/docs-internal/writing?topic=writing-cqd).
