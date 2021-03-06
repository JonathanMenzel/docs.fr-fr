---
title: "Guide pratique pour effectuer une conversion entre des chaînes hexadécimales et des types numériques (Guide de programmation C#) | Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- hexadecimal strings [C#], converting to numeric type
- conversions [C#], hexidecimal strings
- strings [C#], converting hexadecimal strings
- hexadecimal strings [C#]
ms.assetid: 7115c49f-7d1d-40c3-8bd9-aae0cc1d46b6
caps.latest.revision: 19
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
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 5852e79f551ce88e0ca54de159abbc222d769234
ms.lasthandoff: 03/13/2017

---
# <a name="how-to-convert-between-hexadecimal-strings-and-numeric-types-c-programming-guide"></a>Guide pratique pour effectuer une conversion entre des chaînes hexadécimales et des types numériques (Guide de programmation C#)
Ces exemples montrent comment effectuer les tâches suivantes :  
  
-   Obtenir la valeur hexadécimale de chaque caractère dans une chaîne ([string](../../../csharp/language-reference/keywords/string.md)).  
  
-   Obtenir la valeur [char](../../../csharp/language-reference/keywords/char.md) qui correspond à chaque valeur d’une chaîne hexadécimale.  
  
-   Convertir une `string` hexadécimale en [int](../../../csharp/language-reference/keywords/int.md).  
  
-   Convertir une `string` hexadécimale en [float](../../../csharp/language-reference/keywords/float.md).  
  
-   Convertir un tableau d’[octets](../../../csharp/language-reference/keywords/byte.md) en `string` hexadécimale.  
  
## <a name="example"></a>Exemple  
 Cet exemple génère la valeur hexadécimale de chaque caractère dans une `string`. Il convertit d’abord la `string` en un tableau de caractères. Ensuite, il appelle <xref:System.Convert.ToInt32%28System.Char%29> sur chaque caractère pour obtenir sa valeur numérique. Pour finir, il représente le nombre sous forme hexadécimale dans une `string`.  
  
 [!code-cs[csProgGuideTypes#30](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_1.cs)]  
  
## <a name="example"></a>Exemple  
 Cet exemple analyse une `string` de valeurs hexadécimales et génère le caractère correspondant à chacune d’elles. Il appelle d’abord la méthode [Split(Char\[\])](xref:System.String.Split(System.Char[])) pour obtenir chaque valeur hexadécimale sous la forme d’une `string` individuelle dans un tableau. Ensuite, il appelle <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29> pour convertir la valeur hexadécimale en valeur décimale représentée par un entier ([int](../../../csharp/language-reference/keywords/int.md)). Il illustre deux manières d’obtenir le caractère correspondant à ce code de caractère. La première technique utilise <xref:System.Char.ConvertFromUtf32%28System.Int32%29>, qui retourne le caractère correspondant à l’argument entier sous forme de `string`. La deuxième technique effectue un cast explicite de l’`int` en [char](../../../csharp/language-reference/keywords/char.md).  
  
 [!code-cs[csProgGuideTypes#31](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_2.cs)]  
  
## <a name="example"></a>Exemple  
 Cet exemple illustre une autre manière de convertir une `string` hexadécimale en entier en appelant la méthode <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29>.  
  
 [!code-cs[csProgGuideTypes#32](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_3.cs)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment convertir une `string` hexadécimale en [float](../../../csharp/language-reference/keywords/float.md) à l’aide de la classe <xref:System.BitConverter?displayProperty=fullName> et de la méthode <xref:System.Int32.Parse%2A?displayProperty=fullName>.  
  
 [!code-cs[csProgGuideTypes#39](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_4.cs)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment convertir un tableau d’[octets](../../../csharp/language-reference/keywords/byte.md) en chaîne hexadécimale à l’aide de la classe <xref:System.BitConverter?displayProperty=fullName>.  
  
 [!code-cs[csProgGuideTypes#38](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_5.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Chaînes de format numériques standard](http://msdn.microsoft.com/library/580e57eb-ac47-4ffd-bccd-3a1637c2f467)   
 [Types](../../../csharp/programming-guide/types/index.md)   
 [Guide pratique pour déterminer si une chaîne représente une valeur numérique](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)

