---
copyright:
  years: 2025
lastupdated: "2026-02-24"

keywords: troubleshoot, project import, project export
subcollection: watsonx-bi



---

{:codeblock: .codeblock}
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}


# Troubleshooting project import and export
{: #troubleshoot_import_export}

Use these solutions to help resolves problems that you might encounter when you import or export a project.
{: #shortdesc}

## Export issues
{: #export}

The following issues might occur when you export a project.

### Export fails due to project size

If the error message **Project too large** displays, your project exceeds the 500 MB size limit. To reduce project size:
- Remove unused data assets.
- Delete old BI visualizations.
- Clear job run history (if applicable).
- Remove term assignment models if not needed.

### Export fails due to inclusion of uploaded files

Uploaded files cannot be imported. If your project export fails and the project includes uploaded files, complete the following steps:

1. Document which files are uploaded.
2. Remove uploaded file references from the project.
3. Export the project.
4. After import, reupload the files manually.

## Import issues
{: #import}

The following issues might occur when you import a project.

### Import fails with validation error

If your import fails with a validation error, the ZIP file might be corrupted or contain unsupported content. Before you import the project again:
- Verify that the .zip file is not corrupted.
- Make sure that no uploaded files are present in the `/assets/` directory.
- Check that the .zip file was exported from a compatible version of watsonx BI.
- Verify that the .zip file contains required files: `project.json` and `assetrelationships.json`.

### Metrics don't appear after import

SMetrics can take several minutes to initialize. If your metrics don't appear after import:
- Wait 5-10 minutes and refresh the page.
- Check that data models are properly linked to metadata imports.
- Verify that metadata enrichment areas are configured.
- Make sure that connection credentials are entered for all data sources.

### Connection credentials not working

If connection credentials aren't working after you import a project, you might need to reenter your credentials.
- For personal connections, credentials must always be reentered after import.
- For shared connections, verify that the credentials were included in the export.
- Check that the data source is accessible from your current environment.
- Verify that your user account has proper permissions on the data source.

### Relationships between assets are broken

Relationships should be automatically reconstructed. If relationships between your assets are broken after import:
- Verify that all required assets were included in the export.
- Check that connection credentials are properly configured.
- Review the `assetrelationships.json` file in the .zip to confirm relationships were exported.
- Contact support if relationships are consistently not reconstructed.

### Performance considerations

If you import projects that are larger than 100 MB or have many relationships, the import operation might take longer than expected. 

#### Large projects (>100 MB)
- Import might take 10-15 minutes.
- Metrics initialization might take up to 30 minutes.
- Consider importing during off-peak hours.

#### Projects with many relationships
- Relationship reconstruction adds processing time.
- Allow extra time for semantic data models with complex dependencies.
- Monitor the import progress indicator.

## Further help

If you continue to experience issues:
1. Check the export or import logs for specific error messages.
2. Verify that your user role has sufficient permissions.
3. Make sure that your {{site.data.keyword.wxbia_short}} instance is up to date.
4. Contact IBM Support with the project name, error messages, and export or import timestamps.

