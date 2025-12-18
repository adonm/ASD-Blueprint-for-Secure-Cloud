---
title: "Data access"
weight: 10
description: "This section describes the configuration of Copilot data access settings associated with systems built according to the guidance provided by ASD's Blueprint for Secure Cloud."
---

{{% alert title="Instruction" color="dark" %}}

The below pages outline the _as built_ configuration for ASD's _Blueprint for Secure Cloud_ (the Blueprint) for the Microsoft 365 portal at the following URL:

<https://admin.microsoft.com/#/copilot/settings/DataAccess>

The settings described on these pages provide a baseline implementation for a system configured using the Blueprint. Any implementation implied by these pages should not be considered as prescriptive as to how an organisation must scope, build, document, or assess a system.

Implementation of the guidance provided by the Blueprint will differ depending on an organisation’s operating context and organisational culture. Organisations should implement the Blueprint in alignment with their existing change management, business processes and frameworks.

Placeholders such as `<ORGANISATION.GOV.AU>`, `<BLUEPRINT.GOV.AU>` and `<TENANT-NAME>` should be replaced with the relevant details as required.

{{% /alert %}}

{{% alert title="Anthropic subprocessing" color="info" %}}

According to Message Centre announcement [MC1193290](https://admin.microsoft.com/?ref=MessageCenter/:/messages/MC1193290), Anthropic models will be enabled by default for commercial tenants from 7 Jan 2026. This update introduces Anthropic as a Microsoft subprocessor for Copilot experiences.

Microsoft is working to proactively exclude government tenants to align with data sovereignty and regulatory compliance requirements.

At this time, agencies are advised to set this option to **DISABLED** to ensure these models are only enabled following a formal suitability evaluation within their specific risk context.

{{% /alert %}}

### AI providers operating as Microsoft subprocessors

| Item                                          |                                         Value |
| --------------------------------------------- | --------------------------------------------: |
| Available subprocessors for your organization | Disable Anthropic as a Microsoft subprocessor |

### AI providers for other large language models

| Item      |       Value |
| --------- | ----------: |
| Anthropic | Not checked |

### Agents

| Item                                                               |       Value |
| ------------------------------------------------------------------ | ----------: |
| Choose who can access agents                                       |    No users |
| Choose who can share agents with the entire organization           |    No users |
| Choose which types of apps and agents users are allowed to install |             |
| - Allow apps and agents created by Microsoft                       | Not checked |
| - Allow apps and agents created by external publishers             | Not checked |
| - Allow apps and agents built by your organization                 | Not checked |

### Related information

#### Security and governance

- None identified

#### Design

- None identified

#### Configuration

- None identified

#### References

- [Anthropic as a subprocessor for Microsoft Online Services](https://learn.microsoft.com/en-au/copilot/microsoft-365/connect-to-ai-subprocessor)
- [Coming Soon: Anthropic models will be available by default in Copilot experiences](https://admin.microsoft.com/?ref=MessageCenter/:/messages/MC1193290)
- [Data access](https://learn.microsoft.com/en-au/copilot/microsoft-365/microsoft-365-copilot-page#data-access)
