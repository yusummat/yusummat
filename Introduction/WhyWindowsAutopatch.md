# Why Windows Autopatch?
Windows Autopatch helps IT admins to keep your organization's devices updated. Before learning Windows Autopatch, let’s quickly look back exisiting Windows update management tools, WSUS and Configuration manager.
(12/28/2023 Added Windows Update for Business part since Windows Autopatch is based on WUfB service.)

## Comparison with WSUS
Windows Server Update Services (WSUS) is a server role that allows IT administrators to manage and distribute updates to Windows clients in a corporate environment. WSUS downloads updates from Microsoft Update or an intranet server and distributes them to client computers. IT administrators can approve or decline updates before they are installed on client computers. This ensures that only approved updates are installed on client computers, which helps to maintain system stability and security. 
WSUS also helps to reduce network bandwidth usage by downloading updates once and distributing them to client computers, rather than having each client computer download updates from the internet.
IT administrators need to check new updates and decide which updates should or shouldn't be instolled on client computers.
This is one of the popular methods.

## Comparison with Configuration manager
CM provides a centralized console for managing software updates, which allows IT administrators to deploy software updates to client computers in a controlled and automated manner.
IT administrators are required in-depth knowledge to master CM such as Manual deployment, automatic deployment and phased deployment.

### [Appendix] Basic information about Windows Update for Business
Windows Update for Business is a cloud-base offering to keep the Windows client devices in your organization up to date. Windows Update for Business doesn't require on-premise servers such as WSUS server. The Windows clients will source contents from Windows Update for Business server over internet.
Here is basic information about Windows Update for Business so that you can understand how Windows Autopatch work with WUfB.

| Values| Description | Related Links |
|:---|:---|:---|
| **Scheduling** | IT admins can use Group Policy or MDM Solutions such as Microsoft Intune to configure the Windows Update for Business settings that contorol how and when devices are updated.  | [Configure When devices receive feature updates](https://learn.microsoft.com/en-us/windows/deployment/update/waas-configure-wufb#configure-when-devices-receive-feature-updates) |
| **Delivery Optimization** | Delivery Optimization is available. Windows clients can source content from other devices on their local network that have already downloaded the updates.| [What is Delivery Optimization?](https://learn.microsoft.com/en-us/windows/deployment/do/waas-delivery-optimization)|
| **Device Group** | By grouping devices with similar deferral periods, IT admins are able to cluster devices into deployment or validation groups, which can be as a quality control measure as updates are deployed. | [Example of deffering Quality Update](https://learn.microsoft.com/en-us/windows/deployment/update/waas-wufb-group-policy#example) |
| **Update** | Windows Update for Business provides management policies for several types of updates to the devices. | [Types of updates managed by Windows Update for Business](https://learn.microsoft.com/en-us/windows/deployment/update/waas-manage-updates-wufb#types-of-updates-managed-by-windows-update-for-business) |

