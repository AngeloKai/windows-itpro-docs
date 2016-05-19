---
title: User Account Control Run all administrators in Admin Approval Mode (Windows 10)
description: Describes the best practices, location, values, policy management and security considerations for the User Account Control Run all administrators in Admin Approval Mode security policy setting.
ms.assetid: b838c561-7bfc-41ef-a7a5-55857259c7bf
ms.pagetype: security
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: brianlic-msft
---
# User Account Control: Run all administrators in Admin Approval Mode
**Applies to**
-   Windows 10
Describes the best practices, location, values, policy management and security considerations for the **User Account Control: Run all administrators in Admin Approval Mode** security policy setting.
## Reference
This policy setting determines the behavior of all User Account Control (UAC) policies for the entire system. This is the setting that turns UAC on or off.
### Possible values
-   **Enabled**
    Admin Approval Mode and all other UAC policies are dependent on this option being enabled. Changing this setting requires restarting the system.
-   **Disabled**
    Admin Approval Mode and all related UAC policies are disabled.
    **Note**  
    If this security setting is configured to **Disabled**, the Security Center notifies the user that the overall security of the operating system has been reduced.
     
### Best practices
-   Enable this policy to allow all other UAC features and policies to function.
### Location
Computer Configuration\\Windows Settings\\Security Settings\\Local Policies\\Security Options
### Default values
The following table lists the actual and effective default values for this policy. Default values are also listed on the policy’s property page.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Server type or GPO</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Default Domain Policy</p></td>
<td align="left"><p>Not defined</p></td>
</tr>
<tr class="even">
<td align="left"><p>Default Domain Controller Policy</p></td>
<td align="left"><p>Not defined</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stand-Alone Server Default Settings</p></td>
<td align="left"><p>Enabled</p></td>
</tr>
<tr class="even">
<td align="left"><p>DC Effective Default Settings</p></td>
<td align="left"><p>Enabled</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Member Server Effective Default Settings</p></td>
<td align="left"><p>Enabled</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client Computer Effective Default Settings</p></td>
<td align="left"><p>Enabled</p></td>
</tr>
</tbody>
</table>
 
## Policy management
This section describes features and tools that are available to help you manage this policy.
### Restart requirement
A restart of the computer is required before this policy will be effective when changes to this policy are saved locally or distributed through Group Policy.
### Group Policy
All auditing capabilities are integrated in Group Policy. You can configure, deploy, and manage these settings in the Group Policy Management Console (GPMC) or Local Security Policy snap-in for a domain, site, or organizational unit (OU).
## Security considerations
This section describes how an attacker might exploit a feature or its configuration, how to implement the countermeasure, and the possible negative consequences of countermeasure implementation.
### Vulnerability
This is the setting that turns UAC on or off. If this setting is disabled, UAC is not used, and any security benefits and risk mitigations that are dependent on UAC are not present on the computer.
### Countermeasure
Enable the **User Account Control: Run all users, including administrators, as standard users** setting.
### Potential impact
Users and administrators must learn to work with UAC prompts and adjust their work habits to use least privilege operations.
## Related topics
[Security Options](security-options.md)
 
 