---
title: "User access"
weight: 05
description: "This section describes the configuration of Copilot user access settings associated with systems built according to the guidance provided by ASD's Blueprint for Secure Cloud."
---

{{% alert title="Instruction" color="dark" %}}

The below pages outline the _as built_ configuration for ASD's _Blueprint for Secure Cloud_ (the Blueprint) for the Microsoft 365 portal at the following URL:

<https://admin.microsoft.com/#/copilot/settings/UserAccess>

The settings described on these pages provide a baseline implementation for a system configured using the Blueprint. Any implementation implied by these pages should not be considered as prescriptive as to how an organisation must scope, build, document, or assess a system.

Implementation of the guidance provided by the Blueprint will differ depending on an organisation’s operating context and organisational culture. Organisations should implement the Blueprint in alignment with their existing change management, business processes and frameworks.

Placeholders such as `<ORGANISATION.GOV.AU>`, `<BLUEPRINT.GOV.AU>` and `<TENANT-NAME>` should be replaced with the relevant details as required.

{{% /alert %}}

### Pin Microsoft 365 Copilot Chat

| Item                  |                                         Value |
| --------------------- | --------------------------------------------: |
| In Microsoft 365 apps | Do not pin Copilot Chat in Microsoft 365 apps |

### Pin Microsoft 365 Copilot apps to the Windows taskbar

| Item                                        |                                                                                  Value |
| ------------------------------------------- | -------------------------------------------------------------------------------------: |
| Choose how users pin on the Windows taskbar | Do not pin the Microsoft 365 Copilot app and its companion apps to the Windows taskbar |

### Opal (Frontier)

| Item                       |    Value |
| -------------------------- | -------: |
| Choose who can access Opal | No users |

### Microsoft 365 Copilot self-service purchases

| Item                                                    |        Value |
| ------------------------------------------------------- | -----------: |
| Microsoft 365 Copilot self-service trials and purchases | Do not allow |

### Related information

#### Security and governance

- None identified

#### Design

- None identified

#### Configuration

- None identified

#### References

- [User access](https://learn.microsoft.com/en-au/copilot/microsoft-365/microsoft-365-copilot-page#user-access)
