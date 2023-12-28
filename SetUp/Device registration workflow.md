# Device Registration Workflow

![image](https://github.com/yusummat/notes/assets/142761448/29d6b788-ab36-496d-86a3-97bbdc9f7e4d)
*Quated from [Microsoft Learn](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/deploy/windows-autopatch-device-registration-overview#detailed-device-registration-workflow-diagram) 

## IT Admin task
1. Add target devices to [**Windows Autopatch Device Registration group**](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/deploy/windows-autopatch-groups-overview)
   ![image](https://github.com/yusummat/notes/assets/142761448/79ee5954-f8da-44c5-9788-fedd838c8ab4)

2. Confirm the registration has successfully completed
  ![image](https://github.com/yusummat/notes/assets/142761448/b8e2a121-3df2-4032-9434-066858cde048)


## When registration fails...
![image](https://github.com/yusummat/notes/assets/142761448/adbe2355-1fce-4ad4-8199-fcab6707ea5c)

1. Check if the device is enrolled into Intune
2. Make sure it's a Windows Device with eligible Windows lisence
3. If the device is co-managed by Configuration manager and Intune, check if **Windows Update policies**, **Device Configuration** and **Office Click to run** are co-managed.    
  *Please refer to the [workflow diagram](https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/deploy/windows-autopatch-device-registration-overview#detailed-prerequisite-check-workflow-diagram) for details
![image](https://github.com/yusummat/notes/assets/142761448/b15299b0-62d1-4633-85cc-17558a847885)
