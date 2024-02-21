# Conflicting Configuration

You can review the devices that are "Not Ready" state in the *Not Ready* tab.
![image](https://github.com/yusummat/yusummat/assets/142761448/9d8eb0d8-19bd-432d-98e1-145273aad0f1)

Some of the reasons why they are not ready are conflinting configurations. The specific registry values prevent Windows from updating properly. Those registry keys should be removed to resolve the conflict, however, other services could write back the registry keys. It's recommended that you review common sources for conflicting configurations to ensure your devices continue to receive Windows Updates.

## The most common sources of conflicting configurations are...
1) Active Directory Group Policy(GPO)
2) Configuration Manager Device client settings
3) Windows Update for Business (WUfB) policies
4) Manual registry updates
5) Local Group Policy settings applied during imaging(LGPO)

## Intune Remediation
Intune remediation helps detecting and remediating conflicting configurations.
Let's detect and remediate it by following the guidance in [the official documentation](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/references/windows-autopatch-conflicting-configurations#intune-remediation).

### How to detect...
1) Go to Endpoint Admin center and navigate to "Script and Remediation"
   ![image](https://github.com/yusummat/yusummat/assets/142761448/b81a907d-2f5d-4886-92b4-12c841030a1a)
2) Prepare Powershell scripts for detect and remediate by following [the guidance](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/references/windows-autopatch-conflicting-configurations#intune-remediation).
3) Upload and assign the powershell scripts to the target device, and then schedule it.
   ![image](https://github.com/yusummat/yusummat/assets/142761448/978e4465-bb4f-4640-a8fe-66ecc7298592)
4) The script will be executed at the scheduled time.
![image](https://github.com/yusummat/yusummat/assets/142761448/e5c146b3-68d2-414d-ac85-db6739453536)

