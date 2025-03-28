---
title: "Securing iOS devices"
weight: 5
description: "This section describes the design decisions associated with securing iOS endpoints configured according to guidance in ASD's Blueprint for Secure Cloud."
---

Intune provides ability to configure iOS configuration settings for securing, configuring and applications on iOS devices. These configurations are managed via Mobile Device Management (MDM) as an Intune policy. MDM enables the organisation to deploy consistent configuration on enrolled iOS devices.

MDM provides the capability to configure iOS devices. These devices must be configured to meet ASD's iOS Secure Hardening guide to ensure the device can access and store the organisations data. These configurations can be categories as:

* **Security** – Ensure device has up to date and secure authentication policies and encryption devices that meets ASD's Secure iOS guide. 
* **Branding** – The organisations branding for lock screen, wallpapers, and reporting if the device is lost can be configured.
* **Device features** – Configures device features, for example, AirDrop and Bluetooth pairing, within iOS devices.

Using Intune together with Apple Business Manager provides the ability to restrict applications deployed to iOS devices. They improve the user experience during the onboarding process and remove the requirement for an Apple ID and the public Apple App Store. When restricting application deployments, the App Store is blocked and all application management is completed through the Intune Company Portal. All applications must be licenced within Apple Business Manager and use device based licensing. 

{{% alert title="Design decisions" color="warning" %}}

| Decision point                                                | Design decision                                                                                                                                            | Justification                                                                                                                                                                                                                           |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mobile Device Management                                      | Mobile devices will be managed using Intune.                                                                                                               | Leveraging the capabilities already available in the licensing agreement. Intune and Apple Business Manager will be adopted to manage mobile devices.                                                                                   |
| Security policies and hardening requirements                  | Security policies will be enforced on all mobile devices managed by the organisation.                                                                      | Security policies will be configured in line with ASD's Security Configuration Guide – Apple iOS 16 Devices.                                                                                                                            |
| Apple Business Manager Enrolment Token App Delivery           | Organisation licenced apps purchased under the Volume Purchase Program (VPP) are installed directly to devices, without needing an Apple ID on the device. | Configured inline with ASD's iOS hardening guidance, simplifies management and improves user experience with device onboarding.                                                                                                         |
| Public App Store access                                       | Disabled                                                                                                                                                   | Configured inline with ASD's iOS hardening guidance. Applications are installed under the VPP.                                                                                                                                          |
| Device Features                                               | Configured                                                                                                                                                 | Device features configured in line with ASD's hardening guidance.                                                                                                                                                                       |
| **Security**                                                  |                                                                                                                                                            |                                                                                                                                                                                                                                         |
| Supervised Mode                                               | Enable                                                                                                                                                     | Organisation iPhones are managed devices. This is in line with the ASD's iOS Secure Configuration Hardening guide for PROTECTED devices.                                                                                                |
| Device passcode                                               | Device passcode of 14 characters or above. Alphanumeric in nature and must contain a minimum of 1 special character.                                       | iOS devices, by default, is encrypted once a passcode is provided to the device. Configured in line with ISM requirements on password length.                                                                                           |
| Biometrics                                                    | Disable                                                                                                                                                    | This is in line with ASD's iOS Secure Configuration Hardening guide for PROTECTED devices.                                                                                                                                              |
| Mobile Device Management                                      | Enable                                                                                                                                                     | Mobile Device Management provides the organisation better auditing tools on the device. In line with ASD's iOS Secure Configuration Hardening guide for PROTECTED devices.                                                              |
| Maximum Auto-Lock                                             | 2 minutes                                                                                                                                                  | Auto Lock will lock a device if it is inactive for specified time.                                                                                                                                                                      |
| Virtual Private Network (VPN)                                 | Configured                                                                                                                                                 | Per-app VPN will be set up to secure communication between the device and the organisations data. This is in line with ASD's iOS Secure Configuration Hardening guide.                                                                  |
| **Branding**                                                  |                                                                                                                                                            |                                                                                                                                                                                                                                         |
| Lock Screen and background branding                           | Configured                                                                                                                                                 | Organisation branding will be applied to endpoints. It is recommended that organisations include the contact information of the relevant IT Support in the event that a device is lost.                                                 |
| **Device Features**                                           |                                                                                                                                                            |                                                                                                                                                                                                                                         |
| Disable Screenshot and screen recording                       | Disable                                                                                                                                                    | Disablement of screenshot and screen recording, disable users from taking a snapshot of protected documents.                                                                                                                            |
| Allow iCloud backup, document data and Keychain               | Disable                                                                                                                                                    | The organisations data on mobile devices must be uploaded into the organisations tenant. This is done to prevent accidental information being backed up to iCloud or another unsecure data store.                                       |
| Managed Open-In                                               | Enable                                                                                                                                                     | Managed Open-In is enabled to segregate between corporate managed and personal application in an iOS device. This in line with ASD's iOS Secure Configuration Hardening guide for PROTECTED devices.                                    |
| Allow documents from managed sources in unmanaged destination | Disable                                                                                                                                                    | The organisations data cannot be moved between managed and unmanaged application destination. This is to prevent PROTECTED from being transferred to an unmanaged application or location.                                              |
| Treat AirDrop as unmanaged destination                        | Enable                                                                                                                                                     | AirDrop provides the ability to wirelessly transfer documents between Apple devices. Setting AirDrop as an unmanaged destination prevents users from accidentally transferring organisation data to unsecure applications or locations. |
| Restricted Application List                                   | Configured                                                                                                                                                 | Unapproved application installs will be alerted upon. App Store is also disabled as applications will be delivered through the VPP.                                                                                                     |

{{% /alert %}}

### Related information

#### Security & Governance

* [Enterprise Mobility]({{<ref "security-and-governance/system-security-plan/enterprise-mobility.md">}})
* [Authentication Hardening]({{<ref "system-hardening-authentication">}})
  

#### Design

* [Entra ID Protection]({{<ref "design/platform/identity/protection.md">}})
* [Endpoint management]({{<ref "design/platform/client">}})

#### Configuration

* [iOS and iPadOS]({{<ref "configuration/intune/apps/by-platform/ios-ipados.md">}})
* [ASD iOS Hardening]({{<ref "configuration/intune/devices/apple-updates/asd-ios-hardening.md">}})

#### References

* None identified
