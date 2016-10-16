---
title: "Line continuation character &#39;_&#39; must be preceded by at least one white space and must be the last character on the line"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 32caf62f-52e4-4acd-b40f-5af65e42e643
caps.latest.revision: 4
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Line continuation character &#39;_&#39; must be preceded by at least one white space and must be the last character on the line
You can use the line-continuation character, which is an underscore (_), to break a long line of code over several lines in your file. The underscore must be immediately preceded by a space and immediately followed by a line terminator (carriage return). For example:  
  
```  
Dim books As XDocument = _  
    XDocument.Load(My.Application.Info.DirectoryPath & _  
                 "\..\..\Data\books.xml")  
```  
  
 **Error ID:** BC30999  
  
### To correct this error  
  
1.  Ensure that the line continuation character (_) is the last character on a line of code.  
  
2.  Ensure that there is a space before the line continuation character, separating it from any other code on the line.  
  
## See Also  
 [How to: Break and Combine Statements in Code](../Topic/How%20to:%20Break%20and%20Combine%20Statements%20in%20Code%20\(Visual%20Basic\).md)