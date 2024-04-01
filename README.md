# Microsoft Defender for Cloud

## Implementing Microsoft Defender for Cloud

Introduction:
Microsoft Defender for Cloud is a security solution provided by Microsoft that helps protect your cloud resources in Azure. It offers advanced threat protection and security monitoring capabilities. In this lab, I will learn how to configure and implement Microsoft Defender for Cloud in Azure.


<details>
  
  <summary>
    
### Task 1: Configure Microsoft Defender for Cloud
    
  </summary>
  
To configure Microsoft Defender for Cloud, follow these steps:

- Sign in to the Azure portal `https://portal.azure.com/` using an account with Owner or Contributor role in the Azure subscription.

- In the Azure portal, use the search box at the top to search for "Microsoft Defender for Cloud" and press Enter.

- On the Microsoft Defender for Cloud | Getting started blade, click Upgrade.

- In the Install agents tab, scroll down and click Install agents.

- In the Select workspaces with enhanced security features section, enable the Microsoft Defender plan by selecting your Log Analytics Workspace, then click the Upgrade button.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/d25115b6-ffd5-44f9-9ee9-932fac1712bc" height="80%" width="80%" alt="Enable Defender for Cloud on LAW"/>

- Navigate to Microsoft Defender for Cloud and click "Environment Settings" under the Management settings in the vertical menu bar.

- On the Environment Settings blade, click the relevant subscription.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/61156817-1e0a-4ce7-bc2b-8307bd4c8f91" height="70%" width="70%" alt="Environment Settings for Subscription"/>

- On the Defender plans blade, select "Enable all Microsoft Defender for Cloud Plans".
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/b2799abf-f73d-48a3-bd12-82717e2a98a2" height="70%" width="70%" alt="Enable All Plans for Subscription"/>


- Go back to the Environment Settings blade, expand until your subscription appears, and click the entry representing the Log Analytics workspace you created in the previous lab.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/4d5b4da7-c04a-4cd2-bd77-a13f3f2d3ecf" height="80%" width="80%" alt="Enable Defender Plans in Environment Settings"/>

- On the Settings | Defender plans blade, ensure that "Enable all Microsoft Defender for Cloud plans" is selected.
  
  <img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/b9ebc10e-c853-4510-83cd-0a74fe1cf32c" height="80%" width="80%" alt="Enable All Defender Plans"/>

- Select "Data collection" from the Microsoft Defender for Cloud | Settings blade. Choose "All Events" and click Save.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/61eefa36-7e44-4c91-99b8-bc16953553d5" height="90%" width="90%" alt="All Events for Data Collection"/>

</details>

#

<details> 
  
  <summary>
    
### Task 2: Review the Microsoft Defender for Cloud recommendations
    
  </summary> 
  
To review the Microsoft Defender for Cloud recommendations, follow these steps:

- Go back to the Microsoft Defender for Cloud | Overview blade in the Azure portal.

- Review the Secure Score tile to see the current score if available.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/05450b71-badd-4532-abb0-0435538125c1" height="70%" width="70%" alt="Secure Score (1)"/>


- Navigate to the Assessed resources section on the Overview blade.

- On the Inventory blade, select the entry for your virtual machine (myVM).

- On the Resource health blade, go to the Recommendations tab and review the list of recommendations for your virtual machine.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/c6432c90-d988-41e9-a243-a74c3526a56b" height="90%" width="90%" alt="Secuirty Recommendations for VM"/>
  
  </details>
  
  #

<details> 
  
<summary> 
  
### Task 3: Implement the Microsoft Defender for Cloud recommendation to enable Just in time VM Access
  
</summary> 
  
To implement the recommendation to enable Just in time VM Access on your virtual machine, follow these steps:

- Go back to the Microsoft Defender for Cloud | Overview blade in the Azure portal and select "Workload protections" under the Cloud Security tile.

- On the Workload protections blade, click the "Just-in-time VM access" tile in the Advanced protection section.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/67606466-d9c4-4183-a01b-9711ab074b13" height="90%" width="90%" alt="Workload Protection - Just-In-Time access"/>

- On the Just-in-time VM access blade, under the Virtual machines section, select "Not Configured" and then click the entry for your virtual machine (myVM).

- Click the "Enable JIT on 1 VM" option on the far right of the Virtual machines section.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/1bbd4a40-6e27-475f-a106-92f108c4db7d" height="90%" width="90%" alt="Enable JIT on VM"/>

- On the JIT VM access configuration blade, click the ellipsis button on the far right of the row referencing port 22, and then click Delete.
  
<img src="https://github.com/0xbythesecond/Microsoft-Defender-for-Cloud/assets/23303634/1e95d7f1-82c1-4041-981e-95bf185dd1e2" height="80%" width="80%" alt="JIT VM Access Configuration"/>  

- Click Save on the JIT VM access configuration blade.

- Monitor the progress of the configuration by clicking on the Notifications icon in the toolbar and viewing the Notifications blade.

  >**Note**: It may take some time for the implementation of recommendations to be reflected in the Secure Score. Periodically check the Secure Score to determine the impact of implementing these features.
  
</details>

Conclusion:
In this lesson, I have learned how to configure and implement Microsoft Defender for Cloud in Azure. By following the tasks, I have successfully onboarded Microsoft Defender for Cloud, reviewed recommendations, and implemented Just in Time VM Access. Microsoft Defender for Cloud provides enhanced security and threat protection for your cloud resources, helping one safeguard their Azure environment.
