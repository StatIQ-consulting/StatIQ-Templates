# Stat IQ Quarto Report Templates

This Quarto extension provides custom templates for HTML, PDF, and DOCX reports tailored for Stat IQ Consulting. The templates ensure a consistent and professional look across all Stat IQ Consulting reports.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Default YAML Configuration](#default-yaml-configuration)
- [Template Options](#template-options)
- [Troubleshooting](#troubleshooting)

---

## Installation

To install the Stat IQ Quarto templates, use one of the following commands:

- **To create a new project with a working document using the template**:

  ```bash
  quarto use template StatIQ-consulting/StatIQ-Templates
  ```

  This command creates a new document pre-configured with the Stat IQ template, so you can get started immediately.

- **To add the template to an existing project**:

  ```bash
  quarto add template StatIQ-consulting/StatIQ-Templates
  ```

  This installs the template, allowing you to apply the Stat IQ format to your current project.

## Usage

After installation, add the following YAML header to your Quarto document to use the Stat IQ template:

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

## Default YAML Configuration

The default YAML header includes the following options:

```yaml
---
title: "Document Title" # Document type, e.g., Analysis Report, Project Quotation, etc.
subtitle: "Project Title" # Specify the project or report title.
author: "Stat IQ Consulting | [Consultant's Name]" # Customize with the consultant's name.
format:
  StatIQ-html: default # Applies the custom HTML template.
  StatIQ-pdf: default # Applies the custom PDF template.
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
- **Fonts Not Loading**: Verify the fonts are available in `_extensions/statiq/Ubuntu/`.
- **PDF Layout Issues**: Adjust layout settings in `statiqPDF.tex` if alignment or spacing issues arise.

## License

This extension is developed by Stat IQ Consulting for internal use. Redistribution is prohibited.
