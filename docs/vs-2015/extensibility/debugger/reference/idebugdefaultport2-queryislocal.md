---
title: "IDebugDefaultPort2::QueryIsLocal | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugDefaultPort2::QueryIsLocal"
helpviewer_keywords: 
  - "IDebugDefaultPort2::QueryIsLocal"
ms.assetid: 1a42e774-c6ed-419a-a0e3-cab5778652ca
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugDefaultPort2::QueryIsLocal
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugDefaultPort2::QueryIsLocal](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugdefaultport2-queryislocal).  
  
This method determines whether this port is on the local machine.  
  
## Syntax  
  
```cpp#  
HRESULT QueryIsLocal(  
   void  
);  
```  
  
```csharp  
int QueryIsLocal();  
```  
  
## Return Value  
 Returns `S_OK` if this port is local (on the same machine as the caller) or `S_FALSE` if the port is on another machine.  
  
## See Also  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)

