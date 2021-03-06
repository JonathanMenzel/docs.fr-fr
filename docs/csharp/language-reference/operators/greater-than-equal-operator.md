---
title: "&gt;=, op&#233;rateur (r&#233;f&#233;rence C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
f1_keywords: 
  - ">=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - ">= (opérateur C#)"
  - "opérateur supérieur ou égal à (>=) (C#)"
ms.assetid: 0db4dcaf-56a3-4884-a7ad-35f64978a58d
caps.latest.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 16
---
# &gt;=, op&#233;rateur (r&#233;f&#233;rence C#)
Tous les types numériques et d'énumération définissent un opérateur relationnel « supérieur ou égal à », `>=`, qui retourne `true` si le premier opérande est supérieur ou égal au second, et `false` dans le cas contraire.  
  
## Notes  
 Les types définis par l'utilisateur peuvent surcharger l'opérateur `>=`.  Pour plus d'informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).  Si `>=` est surchargé, [\<\=](../../../csharp/language-reference/operators/less-than-equal-operator.md) doit l'être également.  Les opérations sur les types intégraux sont en général autorisées sur énumération.  
  
## Exemple  
 [!code-cs[csRefOperators#39](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-equal-operator_1.cs)]  
  
## Voir aussi  
 [Référence C\#](../../../csharp/language-reference/index.md)   
 [Guide de programmation C\#](../../../csharp/programming-guide/index.md)   
 [Opérateurs C\#](../../../csharp/language-reference/operators/index.md)