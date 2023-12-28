# Windows Feature Updates
Windows feature updates aims to keep Windows devices protected against behavioral issues, and to provide new features to boost end-user productivity.

*Regitering Windows LTSC devices is supported, however, only quality updates will be provided by Windows Autopatch.

## Policies for the default release
Windows Autopatch's default Windows feature update release is a service-driven release that enforces the minimum WIndows OS version.
| Policy name | Description | Link |
|:---|:---|:---|
| Deferrals | You can defer a Feature Update for up to 14 days for all pre-release channels and up to 365 days for the General Availability Channel.  | [Policy CSP - Update - DeferFeatureUpdatesPeriodInDays](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#deferfeatureupdatesperiodindays) |
|　Deadlines | Before the deadline passes, users will be able to schedule restarts, and automatic restarts can happen outside of active hours. When set to 0, updates will download and install immediately。| [Policy CSP - Update - ConfigureDeadlineForFeatureUpdates](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#configuredeadlineforfeatureupdates) |
|　Grace periods |Minimum number of days from update installation until restarts occur automatically. Update/ConfigureDeadlineForFeatureUpdates is configured but this policy is not, then the value configured by Update/ConfigureDeadlineGracePeriod will be used. | [Policy CSP - Update - ConfigureDeadlineGracePeriodForFeatureUpdates](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-update#configuredeadlinegraceperiodforfeatureupdates)|
## The rings in Autopatch groups
Windows Autopatch automatically configures these policies differently across deployment rings to gradually release the update. By default, there are 5 deployment rings with different settings as below.
| Azure AD group | Phase mapping | Feature update ver. | First deployment ring availability | Support end date |
|:---|:---|:---|:---|:---|
|Windows Autopatch -DSS Policy [Test] | Phase 1 | Windows 10 21H2 | May 9, 2023 | June 11, 2024 |
|Windows Autopatch -DSS Policy [First] | Phase 2 | Windows 10 21H2 | May 16, 2023 | June 11, 2024 |
|Windows Autopatch -DSS Policy [Fast] | Phase 3 | Windows 10 21H2 | May 23. 2023 | June 11, 2024 |
|Windows Autopatch -DSS Policy [Broad] | Phase 4 | Windows 10 21H2 | May 30, 2023 | June 11, 2024 |

*Gradual rollout settings are not vailable in the default Windows Update feature policy. If the date of the final group availability has pased, all remaining devices are offered the update as soon as possible.
