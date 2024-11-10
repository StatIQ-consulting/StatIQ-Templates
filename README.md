# Stat IQ Quarto Report Templates

This repository provides custom Quarto templates for Stat IQ Consulting, designed for generating consistent and professional HTML, PDF, and DOCX reports. The templates are set up with Stat IQ’s branding and are customizable for a streamlined reporting experience.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Rendering Reports](#rendering-reports)
- [File Naming Conventions](#file-naming-conventions)
- [Customization](#customization)
- [Default YAML Configuration](#default-yaml-configuration)
- [Template Options](#template-options)
- [Troubleshooting](#troubleshooting)

---

## Installation

To install and use the Stat IQ templates, you have two options:

- **To create a new project** with a working document using the template:
  ```bash
  quarto use template StatIQ-consulting/StatIQ-Templates
  ```

- **To add the template** to an existing project:
  ```bash
  quarto add template StatIQ-consulting/StatIQ-Templates
  ```

This will install the necessary template files and make them available in your project.

## Usage

To apply the Stat IQ templates, add the following YAML header to your Quarto document:

```yaml
---
title: "Document Title" # e.g., Analysis Report, Project Quotation, etc.
subtitle: "Project Title"
author: "Stat IQ Consulting | [Consultant's Name]"
format:
  StatIQ-html: default
  StatIQ-pdf: default
  StatIQ-docx: default
date: last-modified
bibliography: references.bib
execute: 
  echo: false # Hide code in output
---
```

## Rendering Reports

The **Render** buttons in RStudio and VS Code will not automatically render all formats unless the document is part of a Quarto website. To render all formats (HTML, PDF, and DOCX), use the `quarto render` command in the terminal:

```bash
quarto render Client_ReportType_V1_YYYYMMDD.qmd
```

This command will generate all specified formats in the YAML header.

## File Naming Conventions

To maintain consistency and ensure clarity, use the following file naming convention:

**Format**:
```
Client_ReportType_Version_YYYYMMDD.qmd
```

**Components**:
- **Client**: The name or initials of the client (e.g., `ABC`).
- **ReportType**: The type of report, such as `AnalysisReport`, `Quotation`, `Proposal`, etc.
- **Version**: The version number, formatted as `V1`, `V2`, etc.
- **YYYYMMDD**: The date the report was created or last modified in `YYYYMMDD` format.

**Example**:
```
ABC_AnalysisReport_V1_20241110.qmd
```

This structure helps organize reports by client, type, and version and makes it easy to identify the latest version at a glance.

## Customization

Each template offers customization options:

- **Logo and Branding**: Modify the `_extension.yml` file to change the logo path and sidebar content.
- **Color Scheme**: Adjust colors in `statiqPDF.tex` for PDF reports and in `custom.scss` for HTML.
- **Font**: By default, the templates use the Ubuntu font, but you can update font paths in `statiqPDF.tex` if you need different fonts.

## Default YAML Configuration

The default YAML configuration includes the following options:

```yaml
---
title: "Document Title" # Document type, e.g., Analysis Report, Project Quotation, etc.
subtitle: "Project Title" # Specify the project or report title.
author: "Stat IQ Consulting | [Consultant's Name]" # Customize with the consultant’s name.
format:
  StatIQ-html: default # Applies the custom HTML template.
  StatIQ-pdf: default  # Applies the custom PDF template.
  StatIQ-docx: default # Applies the custom DOCX template.
date: last-modified # Automatically updates to the last modified date.
bibliography: references.bib # Bibliography file for references.
execute: 
  echo: false # Suppresses code output in the final document.
---
```

## Template Options

- **`title`**: Main title of the document.
- **`subtitle`**: Project or report-specific title.
- **`author`**: Lists Stat IQ Consulting and can include the consultant’s name.
- **`date`**: Set to `last-modified` by default.
- **`bibliography`**: Path to the `.bib` file for references.
- **`execute`**: Set to `false` to hide code output in the report.

## Troubleshooting

- **Logo Not Displaying**: Ensure `logo.png` is in the correct path as specified in `_extension.yml`.
- **Fonts Not Loading**: Verify that the fonts are available in `_extensions/statiq/Ubuntu/`.
- **PDF Layout Issues**: Adjust layout settings in `statiqPDF.tex` if alignment or spacing issues arise.

## License

This extension was developed by Stat IQ Consulting and is intended for internal use, but redistribution is prohibited.
