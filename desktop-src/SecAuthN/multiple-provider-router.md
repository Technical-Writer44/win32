---
Description: The Multiple Provider Router (MPR) handles communication between the Windows operating system and the installed network providers. It enables Windows to present an integrated network to the user.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Multiple Provider Router
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Multiple Provider Router

The [*Multiple Provider Router*](security.m_gly#-security-multiple-provider-router-gly) (MPR) handles communication between the Windows operating system and the installed network providers. It enables Windows to present an integrated network to the user.

When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through. It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.

For more information about WNet functions, see [Windows Networking](https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd).

 

 


