---
title: "Error: Site Uses IP Address | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.error.webdbg_siteusesipaddress"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "debugger, Web application errors"
ms.assetid: b2b8ddc8-746d-46e3-87a6-b956b1ee048d
caps.latest.revision: 11
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# Error: Site Uses IP Address
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [Error: Site Uses IP Address](https://docs.microsoft.com/visualstudio/debugger/error-site-uses-ip-address).  
  
This error occurs when the debugger tries to auto-attach to a Web application that is using an IP address. This occurs if you change **Web site identification** to **use specific IP address** in IIS.  
  
 For auto-attach to work, you need to create the project with the specific IP address rather than just the machine name. Otherwise, the debugger will change the machine name to localhost, which will cause a failure to send the debug verb to IIS.  
  
### To correct this error  
  
1.  Use manual attach instead (from the Debug menu, choose **Attach to Process**).  
  
     —or—  
  
2.  Change the **IIS Web site identification** setting.  
  
## See Also  
 [Debugging Web Applications: Errors and Troubleshooting](../debugger/debugging-web-applications-errors-and-troubleshooting.md)



