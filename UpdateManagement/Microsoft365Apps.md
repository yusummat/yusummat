# Update Microsoft 365 App for Enterprise with Windows Autopatch
All devices registere for Windows Autopatch receive updates from the **Monthly Enterprise Channel**. 
Unlike Windows updates, Windows Autopatch doesn't control the order in which updates are offered to devices across your organization. 
Therefore, Windows Autopatch doresn't use rings to control the rollout of these updates.

For organizations seeking greater controls, you can block Microsoft 365 App updates. 
Since Windows Autopatch doesn't provide Microsoft 365 App updates on your behalf, your organizations will have full controll over these updates.

## Prerequisites
-The device must have an internet connection

-The device is able to reach the Office Content Delivery Network (CDN)

-No policy conflict between Windows Autopatch policy and customer policies

-The device is required to check into the Intune service in the last 5 days before the update

-Microsoft 365 App will be closed for the update process to complete

## Allow or Block Microsoft 365 App updates
1. Go to Microsoft Intune admin center.
2. Navigate to the Devices > Release Management > Release settings.
3. Go to the [Microsoft 365 apps updates]. By default, the Allow/Block toggle is set to **Allow**.
4. Turn off the **Allow** toggle to opt out of Microsoft 365 App update policies.
   ![image](https://github.com/yusummat/notes/assets/142761448/e39dc5bb-0cbd-4734-9b5f-6903adf85fef)

5. Once the update is complete, you'll receive the notification.

## Configuration policies
Although Windows Autopatch doesn't control the order in which updates are offered to devices across your organization, device configuration policies are configurable. 

By default, there's a seven day update deadline that specifies how long the user has until the user must apply the update.
![image](https://github.com/yusummat/notes/assets/142761448/73dfd658-4c3b-4a8c-9a7c-7e3ee932e536)

Admins are able to add the policies, however, they may experience performance degradation when greater than 400 settings are added to a single policy.
![image](https://github.com/yusummat/notes/assets/142761448/6ef8284b-aa9f-4ca6-b498-4065be4db0ac)
