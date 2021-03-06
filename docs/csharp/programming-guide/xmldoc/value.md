---
title: "&lt;value&gt; (Guide de programmation C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
f1_keywords: 
  - "<value>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<value> (balise XML C#)"
  - "value (balise XML C#)"
ms.assetid: 08dbadaf-9ab6-43d9-9493-98e43bed199a
caps.latest.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 12
---
# &lt;value&gt; (Guide de programmation C#)
## Syntaxe  
  
```  
<value>property-description</value>  
```  
  
#### Paramètres  
 `property-description`  
 Description de la propriété.  
  
## Notes  
 La balise \<value\> permet de décrire la valeur représentée par une propriété.  Remarquez que lorsque vous ajoutez une propriété en utilisant l'Assistant Code dans l'environnement de développement Visual Studio .NET, une balise [\<summary\>](../../../csharp/programming-guide/xmldoc/summary.md) est ajoutée pour la nouvelle propriété.  Vous devez ensuite ajouter manuellement une balise \<value\> pour décrire la valeur représentée par la propriété.  
  
 Compilez avec [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour traiter les commentaires de documentation et les placer dans un fichier.  
  
## Exemple  
 [!code-cs[csProgGuideDocComments#14](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/value_1.cs)]  
  
## Voir aussi  
 [Guide de programmation C\#](../../../csharp/programming-guide/index.md)   
 [Balises recommandées pour les commentaires de documentation](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)