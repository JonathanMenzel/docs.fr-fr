---
title: "Constantes (Guide de programmation C#) | Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- C# language, constants
- constants [C#]
ms.assetid: 1fb39621-1738-49b1-a1b3-8587f109123f
caps.latest.revision: 24
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: ad6c8119d74be0f178681b334f940ff5c38c05ed
ms.contentlocale: fr-fr
ms.lasthandoff: 03/13/2017

---
# <a name="constants-c-programming-guide"></a>Constantes (Guide de programmation C#)
Les constantes sont des valeurs immuables qui sont connues au moment de la compilation et qui ne changent pas pendant la durée de vie du programme. Les constantes sont déclarées avec le modificateur [const](../../../csharp/language-reference/keywords/const.md). Seuls les types intégrés C# (à l’exclusion de <xref:System.Object?displayProperty=fullName>) peuvent être déclarés comme `const`. Pour obtenir une liste des types intégrés, consultez [Tableau des types intégrés](../../../csharp/language-reference/keywords/built-in-types-table.md). Les types définis par l’utilisateur, notamment les classes, les structs et les tableaux, ne peuvent pas être `const`. Utilisez le modificateur [readonly](../../../csharp/language-reference/keywords/readonly.md) pour créer une classe, un struct ou un tableau initialisé une fois au moment de l’exécution (par exemple, dans un constructeur) et qui ne peut pas être modifié ultérieurement.  
  
 C# ne prend pas en charge les propriétés, les événements ou les méthodes `const`.  
  
 Le type enum vous permet de définir des constantes nommées pour les types intégrés intégraux (par exemple, `int`, `uint`, `long`, etc.). Pour plus d’informations, consultez [enum](../../../csharp/language-reference/keywords/enum.md).  
  
 Les constantes doivent être initialisées à mesure qu’elles sont déclarées. Exemple :  
  
 [!code-cs[csProgGuideObjects#64](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/constants_1.cs)]  
  
 Dans cet exemple, la constante `months` est toujours 12, et ne peut pas être modifiée, même par la classe elle-même. En fait, quand le compilateur rencontre un identificateur constant dans du code source C# (par exemple, `months`), il substitue la valeur littérale directement dans le code en langage intermédiaire (IL, Intermediate Language) qu’il produit. Étant donné qu’aucune adresse de variable n’est associée à une constante au moment de l’exécution, les champs `const` ne peuvent pas être passés par référence et ne peuvent pas apparaître comme l-value dans une expression.  
  
> [!NOTE]
>  Procédez avec précaution lorsque vous faites référence à des valeurs constantes définies dans un autre code telles que des DLL. Si une nouvelle version de la DLL définit une nouvelle valeur pour la constante, votre programme conserve l’ancienne valeur littérale jusqu’à ce qu’elle soit recompilée sur la nouvelle version.  
  
 Plusieurs constantes du même type peuvent être déclarées en même temps, par exemple :  
  
 [!code-cs[csProgGuideObjects#65](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/constants_2.cs)]  
  
 L’expression utilisée pour initialiser une constante peut référencer une autre constante si elle ne crée pas de référence circulaire. Exemple :  
  
 [!code-cs[csProgGuideObjects#66](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/constants_3.cs)]  
  
 Les constantes peuvent être marquées comme [public](../../../csharp/language-reference/keywords/public.md), [private](../../../csharp/language-reference/keywords/private.md), [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md) ou `protected``internal`. Ces modificateurs d’accès définissent la façon dont les utilisateurs de la classe peuvent accéder à la constante. Pour plus d’informations, consultez [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).  
  
 Les constantes sont accessibles comme si elles étaient des champs [static](../../../csharp/language-reference/keywords/static.md), car la valeur de la constante est identique pour toutes les instances du type. Vous n’utilisez pas le mot clé `static` pour les déclarer. Les expressions ne se trouvant pas dans la classe qui définit la constante doivent utiliser le nom de la classe, un point et le nom de la constante pour accéder à la constante. Exemple :  
  
 [!code-cs[csProgGuideObjects#67](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/constants_4.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)   
 [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Propriétés](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Types](../../../csharp/programming-guide/types/index.md)   
 [readonly](../../../csharp/language-reference/keywords/readonly.md)   
 [Immutability in C# Part One: Kinds of Immutability](http://go.microsoft.com/fwlink/?LinkId=112379)
