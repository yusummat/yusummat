# How Windows Autopatch groups work?
Autopatch groups is a function app that is part of the device registration micro service within the Windows Autopatch service. There are 2 options for the organizations.

## Windows Autopatch Groups
![image](https://github.com/yusummat/notes/assets/142761448/1403a593-77d3-4a85-81dd-018c78e8bbc7)

With an Autopatch group creation, Windows Autopatch service uses Microsoft Graph to create Azure AD and policy assignments. Once Azure AD groups are created in the Azure AD Service, Intune is used to assign the software update policies to these groups and provide the number of devices that need software update policies to the Windows Update for Business (WUfB) service.

*Quated from [High-level architencture diagram overview](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/deploy/windows-autopatch-groups-overview#high-level-architecture-diagram-overview)

## 2 Options for Autopatch groups
While the Default Autopatch group is intended to serve organizations that are looking to align to Windows Autopatch's default update management process without requiring more customizations, the Custom Autopatch groups are intended to help organizations represent their organization structure more precisely so that they can keep their own update deployment cadence in the service.

|Autopatch groups|Delete/Rename deployment ring|Add/Remove deployment ring composition|Update deployment cadence|Minimum # of Autopatch groups|
|:--|:--|:--|:--|:--|
|The Default Autopatch group|No|Yes|Yes|5|
|Custome Autopatch group|Yes**|Yes|Yes|2|

**Both the Test and Last deployment rings can't be removed or renamed from the Default and Customer Autopatch groups. Autopatch groups don't support the use of one single deployment ring because you need at least 2 deployment rings for their gradual rollout.
