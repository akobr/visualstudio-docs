---
title: "Overload resolution failed because no accessible &#39;&lt;method&gt;&#39; is most specific for these arguments:&lt;error&gt;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8b41fa0-a64b-4e74-8443-be3afd2b6f11
caps.latest.revision: 9
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
# Overload resolution failed because no accessible &#39;&lt;method&gt;&#39; is most specific for these arguments:&lt;error&gt;
You have made a call to an overloaded method, but the compiler has found two or more overloads with parameter lists to which your argument list can be converted, and it cannot select among them.  
  
 The compiler attempts to match the data types in the calling argument list and the overload parameter list as closely as possible. It requires a widening conversion from every one of your arguments to its corresponding parameter, whether the type checking switch ([Option Strict Statement](../Topic/Option%20Strict%20Statement.md)) is `On` or `Off`.  
  
 If the compiler finds more than one overload satisfying the widening requirement, it then looks for the overload that is most specific for the argument data types, that is, that calls for the least amount of widening. It generates this error message when one overload is more specific for one argument's data type while another overload is more specific for another argument's data type. For more information and an example, see [Overload Resolution](../Topic/Overload%20Resolution%20\(Visual%20Basic\).md).  
  
 **Error ID:** BC30521  
  
### To correct this error  
  
1.  Review all the overloads for the method and determine which one you want to call.  
  
2.  In your calling statement, make the data types of the arguments match the data types of the parameters defined for the desired overload. You might have to use the [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) to convert one or more data types to the defined types.  
  
## See Also  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Considerations in Overloading Procedures](../Topic/Considerations%20in%20Overloading%20Procedures%20\(Visual%20Basic\).md)   
 [Overload Resolution](../Topic/Overload%20Resolution%20\(Visual%20Basic\).md)   
 [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)   
 [Overloaded Properties and Methods](../Topic/Overloaded%20Properties%20and%20Methods%20\(Visual%20Basic\).md)   
 [Option Strict Statement](../Topic/Option%20Strict%20Statement.md)   
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)