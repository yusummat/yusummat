# Windows Quality Updates
Windows Autopatch deploys the [Monthly security updates](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/windows-monthly-updates-explained/ba-p/3773544) that are released on the second Tuesday of each month. Since the security update releases are cumulative, they include both new and previously released security fixes along with non-security content introduced in the prior month's optional non-security preview.
## MDM policies to controll Windows Quality Updates
| Policy | Description | Link |
|:---|:---|:---|
| Deferrals | You can defer receiving quality updates for up to 30 days. To prevent quality updates from being received on their scheduled time, you can temporarily pause quality updates. The pause will remain in effect for 35 days or until you clear the start date field. | [Policy CSP - Update - DeferQualityUpdatesPeriodInDays](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#deferqualityupdatesperiodindays) |
|Deadlines | Number of days before quality updates are installed on devices automatically regardless of active hours. Before the deadline passes, users will be able to schedule restarts, and automatic restarts can happen outside of active hours. | [Policy CSP - Update - ConfigureDeadlineForQualityUpdates](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#configuredeadlineforqualityupdates) |
|Grace periods | Minimum number of days from update installation until restarts occur automatically for quality updates. This policy only takes effect when Update/ConfigureDeadlineForQualityUpdates is configured. | [Policy CSP - Update - ConfigureDeadlineGracePeriod](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#configuredeadlinegraceperiod)|
## The rings in Autopatch groups
Windows Autopatch automatically configures these policies differently across deployment rings to gradually release the update. By default, there are 5 deployment rings with different settings as below.
| Azure AD group | Quality updates deferral in days | Deadline for quality updates in days | Grace period | 
|:---|:---|:---|:---|
|Windows Autopatch -Test | 0 | 0 | 0 |
|Windows Autopatch -Ring1 | 1 | 2 | 2 |
|Windows Autopatch -Ring2 | 6 | 2 | 2 |
|Windows Autopatch -Ring3 | 9 | 5 | 2 |
|Windows Autopatch -Last | 11 | 3 | 2 |

![image](https://github.com/yusummat/notes/assets/142761448/1c2e5421-483f-46cf-b74d-ab16e29b8d5c)

