# Preparing Custom Autopatch group
While the Default Autopatch group is intended to serve organizations that are looking to align to Windows Autopatch's default update management process without requiring more customizations, the Custom Autopatch groups are intended to help organizations represent their organization structure more precisely so that they can keep their own update deployment cadence in the service.


## Create Custom Autopatch groups
1. Go to the Microsoft Intune admin center, and select [Devices] from the left navigation menu.
2. Select [Release management] under **Windows Autpatch**.
![image](https://github.com/yusummat/notes/assets/142761448/1b28fefb-37ee-4d1c-b082-7e61411db22b)

3. Go to [Autopatch groups], and Click [+ Create].
![image](https://github.com/yusummat/notes/assets/142761448/fb788b26-c691-4fc2-a2a9-8acfa44f7afc)

4. Input the name of the group and go to **Next: Deployment rings**.
5. **Custom Autopatch group-Test** and  **Custom Autopatch group-Last** have been generated by default. As it is mentioned in [2 options for Autopatch groups](https://github.com/yusummat/notes/blob/main/Setup/UnderstandWindowsAutopatchGroups.md#2-options-for-autopatch-groups), both the Test and Last deployment rings can't be removed or renamed from the Default and Customer Autopatch groups. Autopatch groups don't support the use of one single deployment ring because you need at least 2 deployment rings for their gradual rollout. Add deployment rings as many as your organization needs by clicking [+ Add deployment ring].
![image](https://github.com/yusummat/notes/assets/142761448/80b5bab9-11c9-4d92-8461-f0f003ef58c4)

>[!Important]
>Add devices to each deployment ring using one or both of the following Autopatch group deployment ring distribution types (See section 6 and 7 below)
>　

6. ***Dynamic Distribution***
   
   i) Add a dynamic group to Dynamic group distribution by clicking [Add groups] next to **Dynamic group distribution**.

 　 ii) Click [Apply default dynamic group distribution]. You can manually enter the percentage of devices as needed. The percentage calculation for device must equal to 100%.
 
 　 iii) Add **Assigned group** to the Test and Last deployment rings, since these two don't support ***Dynamic Distribution***. 
![image](https://github.com/yusummat/notes/assets/142761448/40d3b1f7-dcb1-4447-a791-ad947cd05609)

7. ***Assign specific group to deployment ring***

   Click **Add group to ring** and assign a deployment ring group to each deployment rings.

![image](https://github.com/yusummat/notes/assets/142761448/5a97defd-1434-4ec9-9e22-a090267565cf)

8. Go to **Next:Windows update settings**
9. Select the horizontal ellipses (…) ,and then [Manage deployment cadence] to customize your gradual rollout of Windows quality and feature updates. Select [Save].
![image](https://github.com/yusummat/notes/assets/142761448/55f66154-1619-4f6e-876e-1ae009c23d4b)

10. Go to **Next:Review + create**.
11. Once the review is done, select [Create] to save your custom Autopatch group.

