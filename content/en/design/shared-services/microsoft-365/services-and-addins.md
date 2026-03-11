---
title: "Services and add-ins"
weight: 30
description: "This section describes the design decisions associated with services and add-ins for system(s) built using ASD's Blueprint for Secure Cloud."
---

Microsoft 365 centrally manages services and add-ins and can can enhance both the way in which information is accessed and the way in which organisation conducts their business. Enabling services and add-ins also introduces risks to the environment therefore the organisation. Out of the box, several services and add-ins are configured within the portal.

The below design decisions are based on general requirements and consider the location of the hosting application. Organisations should undertake a risk assessment of each of the services and add-ins to ensure alignment with the organisational risk appetite.

{{% alert title="Design decisions" color="warning" %}}

| Decision point                     | Design decision                        | Justification                                                                                                                                                                                                                                                                                                                          |
| ---------------------------------- | -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Azure Speech Services              | Enabled                                | Enabling the organisation-wide language model enables Azure Speech service to gather data from emails and other locations to improve Microsoft 365 applications which use Azure Speech services. The Azure Speech service has been IRAP assessed as part of Azure and enables greater accessibility features as part of the Blueprint. |
| Bookings                           | Disabled                               | Exposes a public web page that provides access to user calendars for 3rd parties. There is no requirement to enable the feature as other methods of collaboration are in use.                                                                                                                                                          |
| Briefing email from Microsoft Viva | Enabled                                | Enabled by default to improve productivity, individual users can unsubscribe if desired.                                                                                                                                                                                                                                               |
| Calendar                           | Disabled                               | External sharing is disabled to prevent potential data spills.                                                                                                                                                                                                                                                                         |
| Cortana                            | Disabled                               | Aligns with ASD's Windows 10 & 11 hardening guidance to disable Windows web results and Cortana thereby limiting the risk of accidental disclosure of sensitive information.                                                                                                                                                           |
| Microsoft communication to users   | Disabled                               | Prevent direct communications from Microsoft to users. Communication to users should instead occur via the organisation IT team.                                                                                                                                                                                                       |
| Microsoft Graph Data Connect       | Disabled                               | API connectivity with Azure Data Factory is not currently in scope of the Blueprint.                                                                                                                                                                                                                                                   |
| Microsoft Teams                    | Enabled                                | Enables both internal and external collaboration.                                                                                                                                                                                                                                                                                      |
| Microsoft To Do                    | Disabled                               | Reduces the risk of user entering sensitive data into external task management lists.                                                                                                                                                                                                                                                  |
| Microsoft Viva Insights            | Enabled                                | Provides users with details about their usage of Microsoft 365.                                                                                                                                                                                                                                                                        |
| Microsoft 365 Group                | Disabled                               | Only Administrators should add guests to a tenant.                                                                                                                                                                                                                                                                                     |
| Microsoft 365 installation options | Enabled                                | Manage update and deployment of Office components.                                                                                                                                                                                                                                                                                     |
| Microsoft 365 on the web           | Third-party storage services: Disabled | Prevents users opening files in third-party storage services thereby reducing the risk of information disclosure or download of malicious content.                                                                                                                                                                                     |
| Modern Authentication              | Enabled                                | Modern authentication is a group of technologies that combines authentication, authorisation, and conditional access policies to secure a Microsoft 365 tenant. Enabling Modern Authentication enables Multi Factor Authentication.                                                                                                    |
| News                               | Disabled                               | Prevent the display of Microsoft 365 content and external news articles together in Edge.                                                                                                                                                                                                                                              |
| Reports                            | Disabled                               | Disable data reporting to Microsoft on Microsoft 365 usage.                                                                                                                                                                                                                                                                            |
| SharePoint                         | Enabled                                | Only people within the organisation - no external sharing allowed                                                                                                                                                                                                                                                                      |
| Sway                               | Disabled                               | External collaboration will be conducted in Teams or SharePoint online.                                                                                                                                                                                                                                                                |
| User consent to apps               | Disabled                               | Require administrators to provide consent.                                                                                                                                                                                                                                                                                             |
| User owned apps and services       | Disabled                               | Applications will be delivered via the Business Store, there is no need to have the Official Store enabled.                                                                                                                                                                                                                            |

{{% /alert %}}

### Self-service trials and purchases

Microsoft 365 allows users to trial and buy third-party add-ins directly. By default, any user can use a credit card to bypass formal procurement and administrative approval.

This decentralised approach creates security and governance risks. It allows unvetted applications into the environment, reduces visibility for IT teams, and may result in data being stored or processed outside of Australia.

{{% alert title="Design decisions" color="warning" %}}

| Decision point                    | Design decision                                                 | Justification                                                                          |
| --------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Self-service trials and purchases | Self-service trials and purchases are disabled for all products | To maintain consistency and reduce risk, only administrators can purchase applications |

{{% /alert %}}

#### Related design decisions

- None identified

### Related information

#### Security and governance

- None identified

#### Design

- [Microsoft 365 Organisation Residency](/design/shared-services/microsoft-365/residency)

#### Configuration

- [Services](/configuration/microsoft-365/settings/services)

#### References

- [Manage self-service purchases and trials (for admins)](https://learn.microsoft.com/en-au/microsoft-365/commerce/subscriptions/manage-self-service-purchases-admins?view=o365-worldwide#use-the-microsoft-365-admin-center-to-allow-or-block-self-service-purchases-and-trials)
