---
title: "Connectors"
linkTitle: "Connectors"
weight: 50
description: "This section describes the configuration of connectors within Exchange Online associated with systems built according to guidance in ASD's Blueprint for Secure Cloud."
---

{{% alert title="Instruction" color="dark" %}}

The below tables outline the *as built* configuration for ASD's *Blueprint for Secure Cloud* (the Blueprint) for the Microsoft Exchange admin portal at the following URL:

<https://admin.exchange.microsoft.com/#/connectors>

The settings described on these pages provide a baseline implementation for a system configured using the Blueprint. Any implementation implied by these pages should not be considered as prescriptive as to how an organisation must scope, build, document, or assess a system.

Implementation of the guidance provided by the Blueprint will differ depending on an organisation’s operating context and organisational culture. Organisations should implement the Blueprint in alignment with their existing change management, business processes and frameworks.

Placeholders such as `<ORGANISATION.GOV.AU>`, `<BLUEPRINT.GOV.AU>` and `<TENANT-NAME>` should be replaced with the relevant details as required.

{{% /alert %}}

### Cloud-native configuration

The cloud-native connector configuration assumes Microsoft 365 is not configured with a 3rd party gateway for mail flow.

Organisations that are required to route traffic through a 3rd party mail gateway will require connectors to be configured.

#### Inbound mail connector

| Item           | Configuration |
| -------------- | ------------: |
| Not configured |           N/A |

#### Outbound mail connector

| Item           | Configuration |
| -------------- | ------------: |
| Not configured |           N/A |

### Hybrid configuration

#### Inbound mail connector

| Item                                                 |                                                                                                                                                                                                                            Configuration |
| ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| From                                                 |                                                                                                                                                                                                         Your Organization's email server |
| To                                                   |                                                                                                                                                                                                                               Office 365 |
| Description                                          |                                                                                                                                                                                                                                     None |
| Status                                               |                                                                                                                                                                                                                                       On |
| Retain internal Exchange email headers               |                                                                                                                                                                                                                                   Enable |
| Authenticating sent email | By verifying that the subject name on the certificate that the sending server uses to authenticate with Office 365 matches the domain entered in the text box below (recommended)           xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx |

#### Outbound mail connector

| Item                                                 |                                                                                                                                                                                                                  Configuration |
| ---------------------------------------------------- | -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| From                                                 |                                                                                                                                                                                                                     Office 365 |
| To                                                   |                                                                                                                                                                                               Your Organization’s email server |
| Description                                          |                                                                                                                                                                                                                           None |
| Status                                               |                                                                                                                                                                                                                             On |
| Retain internal Exchange email headers               |                                                                                                                                                                                                                         Enable |
| When to use the connector                            |                                                                                                                                                                          Only when email messages are sent to these domains: * |
| Routing method                                       |                                                                                                                                                            Route email messages through these smart hosts: Organisation.gov.au |
| Security restrictions                                | Always use Transport Layer Security (TLS) and connect only if the recipient’s email server certificate is issued by a trusted certificate authority (CA), and the subject name matches this domain: `mail.organisation.gov.au` |


### Related information

#### Security & Governance

* None identified
  
#### Design

* [Connectors and Data Loss Prevention Policies]({{<ref "design/shared-services/power-platform/connectors-dlp-policies.md">}})
* [Microsoft 365 Connectivity]({{<ref "design/shared-services/microsoft-365/microsoft365-connectivity.md">}})
  
#### Configuration

* None identified

#### References

* None identified
