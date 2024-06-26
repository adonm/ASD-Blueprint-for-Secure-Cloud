---
title: "GRANT - Protected Location Access"
weight: 10
type: docs
description: "This page describes the configuration of policies for conditional access within Microsoft Entra ID associated with systems built according to the guidance provided by ASD's Blueprint for Secure Cloud."
---

{{% alert title="Instruction" color="dark" %}}
 
The below tables outline the *as built* configuration for ASD's *Blueprint for Secure Cloud* (the Blueprint) for the Entra ID portal blade at the following URL:

https://entra.microsoft.com/#view/Microsoft_AAD_ConditionalAccess/ConditionalAccessBlade/~/Policies
 
The settings described in these tables should be used to provide reference to a baseline implementation for a system configured using the Blueprint. Any implementation implied by these pages should not be considered as prescriptive as to how an organisation must scope, build, document, or assess a system.

Implementation of the guidance provided by the Blueprint will differ depending on an organisation’s operating context and organisational culture. Organisations should implement the Blueprint in alignment with their existing change management, business processes and frameworks.

Placeholders such as `<ORGANISATION.GOV.AU>`, `<BLUEPRINT.GOV.AU>` and `<TENANT-NAME>` should be replaced with the relevant details as required.
 
{{% /alert %}}

### Name

| Item |                             Value |
| ---- | --------------------------------: |
| Name | GRANT - Protected Location Access |

### Assignments

#### Users

| Item                    |                          Value |
| ----------------------- | -----------------------------: |
| **Include**             |                      All users |
| **Exclude**             |                                |
| Guest or external users |                    Not checked |
| Directory roles         |                    Not checked |
| Users and groups        | grp-Conditional_Access_Exclude |

#### Target Resources

| Item                                                             |                  Value |
| ---------------------------------------------------------------- | ---------------------: |
| Select what this policy applies to                               | Authentication context |
| **Select the authentication contexts this policy will apply to** |                        |
| Official Sensitive Locations - Managed Device Only               |            Not checked |
| Protected Location Access                                        |                Checked |
| Official Sensitive Location Access                               |            Not checked |

#### Conditions

| Item                   |                                  Value |
| ---------------------- | -------------------------------------: |
| **User risk**          |                         Not configured |
| **Sign-in risk**       |                         Not configured |
| **Device platforms**   |                                        |
| *Include*              |                             Any device |
| *Exclude*              |                                        |
| - Android              |                                Checked |
| - iOS                  |                                Checked |
| - Windows Phone        |                            Not checked |
| - Windows              |                            Not checked |
| - macOS                |                                Checked |
| - Linux                |                                Checked |
| **Locations**          |                                        |
| Include                |                     Selected locations |
| Select                 | Multifactor authentication trusted IPs |
| **Client apps**        |                         Not configured |
| **Filter for devices** |                         Not configured |

### Access Controls

#### Grant

| Item                                                |                                Value |
| --------------------------------------------------- | -----------------------------------: |
| Control access enforcement to block or grant access |                         Grant access |
| Require multifactor authentication                  |                              Checked |
| Require authentication strength                     |                          Not checked |
| Require device to be marked as compliant            |                              Checked |
| Require Microsoft Entra hybrid joined device        |                          Not checked |
| Require approved client app                         |                          Not checked |
| Require app protection policy                       |                          Not checked |
| Require password change                             |                          Not checked |
| Acceptable Use Policy                               |                          Not checked |
| For multiple controls                               | Require one of the selected controls |

#### Session

| Item                                      |       Value |
| ----------------------------------------- | ----------: |
| Use app enforced restrictions             | Not checked |
| Use Conditional Access App Control        | Not checked |
| Sign-in frequency                         | Not checked |
| Persistent browser session                | Not checked |
| Customize continuous access evaluation    | Not checked |
| Disable resilience defaults               | Not checked |
| Use Global Secure Access security profile | Not checked |

### Enable policy

| Item          | Value |
| ------------- | ----: |
| Enable policy |    On |

### Related information

#### Security & Governance

* [Multi-factor Authentication]({{<ref "multi-factor-authentication">}})
* [Authentication Hardening]({{<ref "system-hardening-authentication">}})
* [Essential Eight - Restrict Administrative Privileges]({{<ref "security-and-governance/essential-eight/restrict-administrative-privileges.md">}})
* [Essential Eight: Restrict Microsoft Office Macros]({{<ref "restrict-microsoft-office-macros.md">}})

#### Design

* [Conditional access]({{<ref "design/platform/identity/conditional-access">}})

#### Configuration

* [Microsoft Intune - Profile Configurations]({{<ref "configuration/intune/devices/configuration-profiles">}})
* [Entra ID Protection]({{<ref "configuration/entra-id/protection">}})

#### References

* [Configure Microsoft Entra multifactor authentication settings](https://learn.microsoft.comentra/identity/authentication/howto-mfa-mfasettings)
* [System-preferred multifactor authentication - Authentication methods policy](https://learn.microsoft.com/entra/identity/authentication/concept-system-preferred-multifactor-authentication)
* [Protecting authentication methods in Microsoft Entra ID](https://learn.microsoft.com/entra/identity/authentication/concept-authentication-default-enablement)

