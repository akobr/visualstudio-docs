---
title: "MESSAGETYPE | Microsoft Docs"
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
  - "MESSAGETYPE"
helpviewer_keywords: 
  - "MESSAGETYPE enumeration"
ms.assetid: 800cc77d-3c27-4763-a9df-552a9384bd49
caps.latest.revision: 12
ms.author: "gregvanl"
manager: "ghogen"
---
# MESSAGETYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [MESSAGETYPE](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/messagetype).  
  
Specifies the message type and reason.  
  
## Syntax  
  
```cpp#  
enum enum_MESSAGETYPE {   
   MT_OUTPUTSTRING      = 0x0000001,  
   MT_MESSAGEBOX        = 0x00000002,  
   MT_TYPE_MASK         = 0x000000FF,  
   MT_REASON_EXCEPTION  = 0x00000100,  
   MT_REASON_TRACEPOINT = 0x00000200,  
   MT_REASON_MASK       = 0x0000FF00  
};  
typedef DWORD MESSAGETYPE;  
```  
  
```csharp  
public enum enum_MESSAGETYPE {   
   MT_OUTPUTSTRING      = 0x0000001,  
   MT_MESSAGEBOX        = 0x00000002,  
   MT_TYPE_MASK         = 0x000000FF,  
   MT_REASON_EXCEPTION  = 0x00000100,  
   MT_REASON_TRACEPOINT = 0x00000200,  
   MT_REASON_MASK       = 0x0000FF00  
};  
```  
  
## Members  
 MT_OUTPUTSTRING  
 Indicates that the message should be sent to the output window. This is mutually exclusive from `MT_MESSAGEBOX`.  
  
 MT_MESSAGEBOX  
 Indicates that the message should be shown in a message box. This is mutually exclusive from `MT_OUTPUTSTRING`.  
  
 MT_TYPE_MASK  
 A mask value to isolate the destination for the message.  
  
 MT_REASON_EXCEPTION  
 Indicates that a message box is being shown as a result of an exception. This is mutually exclusive from `MT_REASON_TRACEPOINT`.  
  
 MT_REASON_TRACEPOINT  
 Indicates that a message box is being shown as a result of hitting a tracepoint. This is mutually exclusive to `MT_REASON_EXCEPTION`.  
  
 MT_REASON_MASK  
 A mask value to isolate the reason for the message being shown.  
  
## Remarks  
 These values are returned from the [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md) and [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md) methods.  
  
 One of the reason values can be combined with one of the output destination values using a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)   
 [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md)

