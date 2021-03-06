---
title: "&lt;, op&#233;rateur (r&#233;f&#233;rence C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
f1_keywords: 
  - "<_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "< (opérateur C#)"
  - "opérateur moins que (<) (C#)"
ms.assetid: 38cb91e6-79a6-48ec-9c1e-7b71fd8d2b41
caps.latest.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 14
---
# &lt;, op&#233;rateur (r&#233;f&#233;rence C#)
Tous les types numériques et d'énumération définissent un opérateur relationnel « inférieur à » \(`<`\) qui retourne `true` si le premier opérande est inférieur au second, et `false` dans le cas contraire.  
  
## Notes  
 Les types définis par l'utilisateur peuvent surcharger l'opérateur `<` \(consultez [opérateur](../../../csharp/language-reference/keywords/operator.md)\).  Si `<` est surchargé, [\>](../../../csharp/language-reference/operators/greater-than-operator.md) doit l'être également.  Lorsqu'un opérateur binaire est surchargé, l'opérateur d'assignation correspondant \(s'il y en a un\) est, lui aussi, implicitement surchargé.  
  
## Exemple  
 [!code-cs[csRefOperators#24](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-operator_1.cs)]  
  
## Voir aussi  
 [Référence C\#](../../../csharp/language-reference/index.md)   
 [Guide de programmation C\#](../../../csharp/programming-guide/index.md)   
 [Opérateurs C\#](../../../csharp/language-reference/operators/index.md)