---
title: "Services"
weight: 10
description: "This section describes the configuration of services in Microsoft 365 associated with systems built according to the guidance provided by ASD's Blueprint for Secure Cloud."
---

{{% alert title="Instruction" color="dark" %}}

The below tables outline the _as built_ configuration for ASD's _Blueprint for Secure Cloud_ (the Blueprint) for the Microsoft 365 portal at the following URL:

<https://admin.microsoft.com/Adminportal/Home?#/Settings/Services>

The settings described on these pages provide a baseline implementation for a system configured using the Blueprint. Any implementation implied by these pages should not be considered as prescriptive as to how an organisation must scope, build, document, or assess a system.

Implementation of the guidance provided by the Blueprint will differ depending on an organisation’s operating context and organisational culture. Organisations should implement the Blueprint in alignment with their existing change management, business processes and frameworks.

Placeholders such as `<ORGANISATION.GOV.AU>`, `<BLUEPRINT.GOV.AU>` and `<TENANT-NAME>` should be replaced with the relevant details as required.

{{% /alert %}}

### Account Linking

| Item                                                             |    Value |
| ---------------------------------------------------------------- | -------: |
| Allow users to connect their Microsoft Entra ID and MSA accounts | Disabled |

### Adoption Score

| Item                                             |                           Value |
| ------------------------------------------------ | ------------------------------: |
| **Insight calculations and display**             |                                 |
| Select users and groups for calculating insights | Include all users (recommended) |
| Turn on group-level insights                     |                       Unchecked |

### Azure Speech Services

| Item                                       |   Value |
| ------------------------------------------ | ------: |
| Allow the organization-wide language model | Checked |

### Bookings

| Item                                    |     Value |
| --------------------------------------- | --------: |
| Allow your organization to use Bookings | Unchecked |

### Calendar

| Item                                                                                                          |     Value |
| ------------------------------------------------------------------------------------------------------------- | --------: |
| Let your users share their calendars with people outside of your organization who have Office 365 or Exchange | Unchecked |

### Cortana

| Item                                                                                                                                                                     |     Value |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------: |
| Allow Cortana in Windows 10 (version 1909 and earlier), and the Cortana app on iOS and Android, to access Microsoft-hosted data on behalf of people in your organization | Unchecked |

### Developer Portal for Teams

| Item                                                                |     Value |
| ------------------------------------------------------------------- | --------: |
| Allow app usage for all custom apps to show in the Developer Portal | Unchecked |

### Dynamics 365 Customer Voice

| Item                      |     Value |
| ------------------------- | --------: |
| **Security**              |           |
| Prevent phishing attempts |   Checked |
| Collect names             |   Checked |
| Restrict survey access    | Unchecked |

### Microsoft 365 Groups

| Item                                                                                    |     Value |
| --------------------------------------------------------------------------------------- | --------: |
| Let group owners add people outside your organization to Microsoft 365 Groups as guests | Unchecked |
| Let guest group members access group content                                            | Unchecked |
| When there's no owner, email and ask active group members to become an owner            | Unchecked |

### Microsoft 365 installation options

| Item                                                    |    Value |
| ------------------------------------------------------- | -------: |
| **Feature updates**                                     |          |
| As soon as they're ready (Current Channel, recommended) | Selected |
| **Installation**                                        |          |
| Apps for Windows and mobile devices                     |          |
| - Office (includes Skype for Business)                  |  Checked |
| - Skype for Business (Standalone)                       |  Checked |
| Apps for Mac                                            |          |
| - Office                                                |  Checked |
| - Skype for Business (X El Capitan 10.11 or higher)     |  Checked |

### Microsoft 365 on the web

| Item                                                                                   |     Value |
| -------------------------------------------------------------------------------------- | --------: |
| Let users open files store in third-party storage services in Microsoft 365 on the web | Unchecked |

### Microsoft communication to users

| Item                                                                                                |     Value |
| --------------------------------------------------------------------------------------------------- | --------: |
| Let people in my organization receive emails from Microsoft about how to use Microsoft 365 products | Unchecked |

### Microsoft Forms

| Item                                                  |     Value |
| ----------------------------------------------------- | --------: |
| Send a link to the form and collect responses         |   Checked |
| Share to collaborate on the form layout and structure |   Checked |
| Share the form as the template that can be duplicated |   Checked |
| Share form result summary                             | Unchecked |
| Record named by default                               |   Checked |
| Include Bing search, YouTube videos                   | Unchecked |
| Add internal phishing protection                      |   Checked |
| Allow respondents to edit their responses             | Unchecked |

### Microsoft Graph Data Connect

| Item                                                                       |     Value |
| -------------------------------------------------------------------------- | --------: |
| Turn on Microsoft Graph Data Connect on or off for you entire organization | Unchecked |

### Microsoft Loop

| Item                                                                    |   Value |
| ----------------------------------------------------------------------- | ------: |
| Microsoft Loop workspaces are available to all users in my organization | Checked |

### Microsoft Planner

| Item                                                                                                               |     Value |
| ------------------------------------------------------------------------------------------------------------------ | --------: |
| Allow Planner users to publish their plans and assigned tasks to Outlook or other calendars through iCalendar feed | Unchecked |

### Microsoft Teams

| Item                                  |     Value |
| ------------------------------------- | --------: |
| Turn on Microsoft Teams for all users |   Checked |
| Allow guest access in Teams           | Unchecked |

### Microsoft To Do

| Item                                           |     Value |
| ---------------------------------------------- | --------: |
| Allow your users to receive push notifications | Unchecked |

### Microsoft Viva Insights

| Item                                              |     Value |
| ------------------------------------------------- | --------: |
| Personal and organization insights web experience |   Checked |
| Digest email                                      |   Checked |
| Insights Outlook add-in and inline suggestions    |   Checked |
| Meeting effectiveness surveys                     |   Checked |
| Schedule send suggestions                         |   Checked |
| Allow Microsoft to contact me about my feedback   | Unchecked |

### Modern Authentication

| Item                                                                               |     Value |
| ---------------------------------------------------------------------------------- | --------: |
| Turn on modern authentication for Outlook 2013 for Windows and later (recommended) |   Checked |
| Authenticated SMTP                                                                 | Unchecked |

### News

| Item                                                          |      Value |
| ------------------------------------------------------------- | ---------: |
| **General**                                                   |            |
| Industry                                                      |     _None_ |
| Topics                                                        |     _None_ |
| Exclude Content                                               |     _None_ |
| Allow user to customize their own topics                      |  Unchecked |
| Turn on industry news content in Microsoft Feed               |  Unchecked |
| **Industry updates**                                          |            |
| Send daily email updates                                      |  Unchecked |
| **Bing homepage**                                             |            |
| Include industry news                                         |  Unchecked |
| **Microsoft Edge new tab page**                               |            |
| Show Microsoft 365 content on the Microsoft Edge new tab page |  Unchecked |
| Show My Feed content on the Microsoft Edge new tab page       |  Unchecked |
| Users default to My Feed                                      | Unselected |
| Users default to Work Feed                                    | Unselected |

### Reports

| Item                                                                     |     Value |
| ------------------------------------------------------------------------ | --------: |
| Display concealed user, group, and site names in all reports             | Unchecked |
| Make report data available to Microsoft 365 usage analytics for Power BI | Unchecked |

### Self-service trials and purchases

| Item                                                   |    Value |
| ------------------------------------------------------ | -------: |
| Dynamics 365 Marketing                                 |          |
| - Do not allow                                         | Selected |
| Dynamics 365 Marketing Additional Application          |          |
| - Do not allow                                         | Selected |
| Dynamics 365 Marketing Additional Non-Prod Application |          |
| - Do not allow                                         | Selected |
| Dynamics 365 Marketing Attach                          |          |
| - Do not allow                                         | Selected |
| Microsoft 365 Copilot                                  |          |
| - Do not allow                                         | Selected |
| Microsoft 365 F3                                       |          |
| - Do not allow                                         | Selected |
| Microsoft ClipChamp                                    |          |
| - Do not allow                                         | Selected |
| Microsoft Purview Discovery                            |          |
| - Do not allow                                         | Selected |
| Power Apps per user                                    |          |
| - Do not allow                                         | Selected |
| Power Automate per user plan                           |          |
| - Do not allow                                         | Selected |
| Power Automate Per User with Attended RPA Plan         |          |
| - Do not allow                                         | Selected |
| Power Automate RPA                                     |          |
| - Do not allow                                         | Selected |
| Power BI Premium per user                              |          |
| - Do not allow                                         | Selected |
| Power BI Pro                                           |          |
| - Do not allow                                         | Selected |
| Planner Plan 1                                         |          |
| - Do not allow                                         | Selected |
| Project Plan 3                                         |          |
| - Do not allow                                         | Selected |
| Python in Excel                                        |          |
| - Do not allow                                         | Selected |
| Teams Exploratory Upgrade Request                      |          |
| - Do not allow                                         | Selected |
| Teams Exploratory                                      |          |
| - Do not allow                                         | Selected |
| Microsoft Teams Premium                                |          |
| - Do not allow                                         | Selected |
| Visio Plan 1                                           |          |
| - Do not allow                                         | Selected |
| Visio Plan 2                                           |          |
| - Do not allow                                         | Selected |
| Viva Goals                                             |          |
| - Do not allow                                         | Selected |
| Viva Learning                                          |          |
| - Do not allow                                         | Selected |
| Windows 365 Buisness                                   |          |
| - Do not allow                                         | Selected |
| Windows 365 Buisness with Windows Hybrid Benefit       |          |
| - Do not allow                                         | Selected |
| Windows 365 Enterprise                                 |          |
| - Do not allow                                         | Selected |

### SharePoint

| Item                                                           |    Value |
| -------------------------------------------------------------- | -------: |
| Only people in your Organization - no external sharing allowed | Selected |

### Sway

| Item                                                                                   |     Value |
| -------------------------------------------------------------------------------------- | --------: |
| Let people in your organization share their sways with people outside you organization | Unchecked |
| Let people in your organization look up people and security groups                     | Unchecked |
| Flickr                                                                                 | Unchecked |
| Pickit                                                                                 | Unchecked |
| Wikipedia                                                                              | Unchecked |
| YouTube                                                                                | Unchecked |

### User owned apps and services

| Item                                                      |     Value |
| --------------------------------------------------------- | --------: |
| Let users access the Office Store                         | Unchecked |
| Let users start trials on behalf of your organization     | Unchecked |
| Let users auto-claim licences the first time they sign in | Unchecked |

### Viva Learning

| Item                                                                                                                                                                  |     Value |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------: |
| Required Diagnostic Data. Send the minimum data necessary to Microsoft to keep Viva Learning secure, up-to-date, and performing as expected                           | Unchecked |
| Optional Diagnostic Data. Additional data that helps us make product improvements and provides enhanced information to help us detect, diagnose, and remediate issues | Unchecked |

### Whiteboard

| Item                                                                                                                            |     Value |
| ------------------------------------------------------------------------------------------------------------------------------- | --------: |
| Turn on Whiteboard for everyone in your org                                                                                     |   Checked |
| Neither - No diagnostic data about Whiteboard client software running on the devices in your organizations is sent to Microsoft |  Selected |
| Allow the use of optional connected experiences in legacy Whiteboard                                                            | Unchecked |
| Enable easy sharing of legacy whiteboards from Surface Hub                                                                      | Unchecked |

### Related information

#### Security and governance

- None identified

#### Design

- [Microsoft Forms](/design/shared-services/forms)
- [Microsoft Planner](/design/shared-services/planner)
- [Microsoft Whiteboard](/design/shared-services/whiteboard)
- [Services and Add-Ins](/design/shared-services/microsoft-365/services-and-addins)
- [Sharing and access controls](/design/shared-services/sharepoint-online/sharing)
- [Viva Learning](/design/shared-services/viva-learning)

#### Configuration

- [Sharing](/configuration/sharepoint-online/policies/sharing)

#### References

- None identified
