---
title: "Compiler Error CS1955"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38a8542d-da53-4739-b807-46c8c077363c
caps.latest.revision: 8
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
# Compiler Error CS1955
Non-invocable member 'name' cannot be used like a method.  
  
 Only methods and delegates can be invoked. This error is generated when you try to use empty parentheses to call something other than a method or delegate.  
  
### To correct this error  
  
1.  Remove the parentheses from the expression.  
  
## Example  
 The following code generates CS1955 because the code is trying to invoke a field and a property by using the method call operator [()](../Topic/\(\)%20Operator%20\(C%23%20Reference\).md). You cannot call a field or property, but you can access the value it stores by using the member access operator ( [.](../Topic/.%20Operator%20\(C%23%20Reference\).md) ).  
  
```  
// cs1955.cs  
class A  
{  
    public int x = 0;  
    public int X  
    {  
        get { return x; }  
        set { x = value; }  
    }  
}  
  
class Test  
{  
    static int Main()  
    {  
        A a = new A();  
        a.x(); // CS1955  
        a.X(); // CS1955  
        // Try this line instead:  
        // int num = a.x;  
    }  
}  
```