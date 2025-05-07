---
title: FAQs for deleting user data
description: A Microsoft Viva Glint administrator can delete user data from the platform in such a manner that complies with Microsoft standards. 
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.custom: CELA-approved
ms.date: 02/25/2025
---

# FAQs for deleting user data

A Microsoft Viva Glint administrator can delete user data from the platform in such a manner that complies with Microsoft standards. 

**Q: When will user records be deleted from Viva Glint?** <br>
**A:** When Viva Glint receives the delete signal from a Data Subject Request (DSR) or Microsoft Entra ID for a user, they're not immediately deleted. A user's employee record is in a soft-deleted state in accordance with [Microsoft's data handling standards](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview). During this period, the employee record may be modified from its soft-deleted state and updated to the status provided in the Human Resource Information System (HRIS) file per the client's User Data control setting at **Disregard Employee IDs** of previously deleted employees. After this period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at **Delete survey data for deleted users.** 

**Q: What does “all data related to the requester” mean?** <br>
**A:** This phrase refers to the user's first name, last name, employee ID, email address, and personal email address (if used) associated with survey responses and reporting. 

**Q: What is the impact of selecting "Erase all data related to the requester, excluding attributes and survey responses"?** <br>
**A:**  This option corresponds to User Data control in General Settings. **Delete survey data for deleted users** = Off. This setting deletes the user's first name, last name, employee ID, email address and personal email (if used) associated with survey responses and reporting. The user's other attributes and survey responses are retained. If the deleted user is a manager, this impacts the manager hierarchy reporting as the manager's name is now listed as **Deleted User** and **Deleted User's Team** for any associated cycles. The reporting for other attributes isn't impacted.

**Q: What is the impact of setting "Delete survey data for deleted users" as "Off" in User Data control in General Settings?** <br>
**A:** This setting deletes the User's first name, last name, employee ID, email address and personal email (if used) associated with survey responses and reporting. The User's other attributes and survey responses are retained. If the deleted user is a manager, this change impacts the manager hierarchy reporting as the manager's name is listed as **Deleted User** and **Deleted User's Team** for any associated cycles. The reporting for other attributes **isn't impacted.**

**Q: What is the impact of selecting "Erase all data related to the requester, including survey responses"?**<br>
**A:**  This option corresponds to User Data control in General Settings. "Delete survey data for deleted users" = On. This setting deletes the User's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted user is a manager, this change impacts the manager hierarchy reporting as the manager's name is listed as **Deleted User** and **Deleted User's Team** for any associated cycles. The reporting for all associated attributes **is impacted**, including response rates.

**Q: What is the impact of setting "Delete survey data for deleted users" as "On" in User Data control in General Settings?** <br>
**A:**  This setting deletes the User's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted user is a manager, this impacts the manager hierarchy reporting as the manager's name is listed as **Deleted User** and **Deleted User's Team** for any associated cycles. The reporting for all associated attributes is impacted, including response rates.



