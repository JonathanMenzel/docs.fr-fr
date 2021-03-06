---
title: "Méthodes d’extension (Guide de programmation C#) | Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- methods [C#], adding to existing types
- extension methods [C#]
- methods [C#], extension
ms.assetid: 175ce3ff-9bbf-4e64-8421-faeb81a0bb51
caps.latest.revision: 35
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
ms.openlocfilehash: b12c4b20f65f8cd2b68a55c5d2548b289a560c3c
ms.lasthandoff: 03/13/2017

---
# <a name="extension-methods-c-programming-guide"></a>Méthodes d’extension (Guide de programmation C#)
Les méthodes d'extension vous permettent d'« ajouter » des méthodes à des types existants sans créer un type dérivé, ni recompiler ou modifier le type d'origine. Les méthodes d'extension sont un type particulier de méthode statique appelées comme s'il s'agissait de méthodes d'instance sur le type étendu. Pour le code client écrit en C# et Visual Basic, il n’y a aucune différence apparente entre appeler une méthode d’extension et les méthodes qui sont réellement définies dans un type.  
  
 Les méthodes d’extension les plus courantes sont les opérateurs de requête standard [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)] qui ajoutent des fonctionnalités de requête aux types <xref:System.Collections.IEnumerable?displayProperty=fullName> et <xref:System.Collections.Generic.IEnumerable%601?displayProperty=fullName> existants. Pour utiliser les opérateurs de requête standard, introduisez-les d'abord dans la portée avec une directive `using System.Linq`. Ensuite, tout type qui implémente <xref:System.Collections.Generic.IEnumerable%601> semble avoir des méthodes d’instance telles que <xref:System.Linq.Enumerable.GroupBy%2A>, <xref:System.Linq.Enumerable.OrderBy%2A>, <xref:System.Linq.Enumerable.Average%2A>, et ainsi de suite. Vous pouvez voir ces méthodes supplémentaires dans la saisie semi-automatique des instructions IntelliSense quand vous tapez « point » après une instance d’un type <xref:System.Collections.Generic.IEnumerable%601> tel que <xref:System.Collections.Generic.List%601> ou <xref:System.Array>.  
  
 L'exemple suivant indique comment appeler la méthode `OrderBy` d'opérateur de requête standard sur un tableau d'entiers. L'expression entre parenthèses est une expression lambda. De nombreux opérateurs de requête standard prennent des expressions lambda comme paramètres, mais ce n’est pas requis pour les méthodes d’extension. Pour plus d’informations, consultez [Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).  
  
 [!code-cs[csProgGuideExtensionMethods#3](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/extension-methods_1.cs)]  
  
 Les méthodes d’extension sont définies comme méthodes statiques mais sont appelées en utilisant la syntaxe de méthode d’instance. Leur premier paramètre spécifie les types sur lesquels la méthode s’applique et le paramètre est précédé du modificateur [this](../../../csharp/language-reference/keywords/this.md). Les méthodes d'extension sont uniquement dans la portée lorsque vous importez explicitement l'espace de noms dans votre code source avec une directive `using`.  
  
 L’exemple suivant montre une méthode d’extension définie pour la classe <xref:System.String?displayProperty=fullName>. Notez qu'elle est définie à l'intérieur d'une classe statique, non imbriquée et non générique :  
  
 [!code-cs[csProgGuideExtensionMethods#4](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/extension-methods_2.cs)]  
  
 La méthode d'extension `WordCount` peut être mise à portée avec cette directive `using` :  
  
```  
using ExtensionMethods;  
```  
  
 Elle peut être appelée à partir d'une application à l'aide de cette syntaxe :  
  
```  
string s = "Hello Extension Methods";  
int i = s.WordCount();  
```  
  
 Dans votre code, vous appelez la méthode d'extension avec la syntaxe de méthode d'instance. Toutefois, le langage intermédiaire (IL) généré par le compilateur traduit votre code dans un appel sur la méthode statique. Par conséquent, le principe d'encapsulation n'est pas réellement violé. En fait, les méthodes d’extension ne peuvent pas accéder aux variables privées dans le type qu’elles étendent.  
  
 Pour plus d’informations, consultez [Guide pratique pour implémenter et appeler une méthode d’extension personnalisée](../../../csharp/programming-guide/classes-and-structs/how-to-implement-and-call-a-custom-extension-method.md).  
  
 En général, vous appellerez probablement les méthodes d’extension beaucoup plus souvent que vous n’implémenterez vos propres méthodes. Comme les méthodes d'extension sont appelées à l'aide de la syntaxe de méthode d'instance, aucune connaissance particulière n'est requise pour les utiliser depuis le code client. Pour activer des méthodes d'extension pour un type particulier, ajoutez simplement une directive `using` pour l'espace de noms dans lequel les méthodes sont définies. Par exemple, pour utiliser les opérateurs de requête standard, ajoutez la directive `using` à votre code :  
  
```  
using System.Linq;  
```  
  
 (Il peut également être nécessaire d'ajouter une référence à System.Core.dll.) Vous pouvez remarquer que les opérateurs de requête standard apparaissent dorénavant dans IntelliSense comme des méthodes supplémentaires disponibles pour la plupart des types <xref:System.Collections.Generic.IEnumerable%601>.  
  
> [!NOTE]
>  Bien que les opérateurs de requête standard n’apparaissent pas dans IntelliSense pour <xref:System.String>, ils sont encore disponibles.  
  
## <a name="binding-extension-methods-at-compile-time"></a>Liaison de méthodes d’extension à la compilation  
 Vous pouvez utiliser des méthodes d'extension pour étendre une classe ou une interface, mais pas pour les remplacer. Une méthode d'extension avec le même nom et la même signature qu'une méthode d'interface ou de classe ne sera jamais appelée. Au moment de la compilation, les méthodes d'extension ont toujours la priorité la plus faible par rapport aux méthodes d'instance définies dans le type lui-même. En d'autres termes, si un type a une méthode nommée `Process(int i)` et que vous avez une méthode d'extension avec la même signature, le compilateur créera toujours une liaison avec la méthode d'instance. Lorsque le compilateur rencontre un appel de méthode, il recherche d'abord une correspondance dans les méthodes d'instance du type. Si aucune correspondance n'est trouvée, il recherche toutes les méthodes d'extension définies pour le type et crée une liaison avec la première méthode d'extension qu'il trouve. L’exemple suivant montre comment le compilateur détermine quelle méthode d’extension ou méthode d’instance est choisie pour créer une liaison.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre les règles que le compilateur C# suit pour déterminer s’il faut lier un appel de méthode à une méthode d’instance sur le type, ou à une méthode d’extension. Le classe statique `Extensions` contient des méthodes d'extension définies pour tout type qui implémente `IMyInterface`. Les classes `A`, `B` et `C` implémentent toutes l'interface.  
  
 La méthode d'extension `MethodB` n'est jamais appelée car son nom et sa signature correspondent exactement aux méthodes déjà implémentées par les classes.  
  
 Lorsque le compilateur ne trouve pas de méthode d’instance avec une signature correspondante, il crée une liaison avec une méthode d’extension correspondante, s’il en existe une.  
  
 [!code-cs[csProgGuideExtensionMethods#5](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/extension-methods_3.cs)]  
  
## <a name="general-guidelines"></a>Indications générales  
 En général, nous vous recommandons d'implémenter des méthodes d'extension modérément et uniquement lorsque cela est nécessaire. Dès que cela est possible, le code client qui doit étendre un type existant doit le faire en créant un type dérivé du type existant. Pour plus d’informations, consultez [Héritage](../../../csharp/programming-guide/classes-and-structs/inheritance.md).  
  
 Lors de l’utilisation d’une méthode d’extension pour étendre un type dont le code source ne peut pas être modifié, vous risquez d’interrompre votre méthode d’extension en cas de modification dans l’implémentation du type.  
  
 Si vous implémentez des méthodes d'extension pour un type donné, prenez en compte les points suivants :  
  
-   Une méthode d'extension ne sera jamais appelée si elle a la même signature qu'une méthode définie dans le type.  
  
-   Les méthodes d'extension sont mises en portée au niveau de l'espace de noms. Par exemple, si vous avez plusieurs classes statiques qui contiennent des méthodes d'extension dans un espace de noms unique nommé `Extensions`, elles seront toutes mises en portée par la directive `using Extensions;`.  
  
 Pour une bibliothèque de classes que vous avez implémentée, vous ne devez pas utiliser de méthodes d'extension pour éviter d'incrémenter le numéro de version d'un assembly. Si vous souhaitez ajouter une fonctionnalité importante à une bibliothèque dont le code source vous appartient, vous devez suivre les directives .NET Framework standard relatives à la gestion de version des assemblys. Pour plus d’informations, consultez [Versioning des assemblys](https://msdn.microsoft.com/library/51ket42z).  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)   
 [Exemples de programmation parallèle (il s’agit de nombreux exemples de méthodes d’extension)](http://code.msdn.microsoft.com/Samples-for-Parallel-b4b76364)   
 [Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)   
 [Vue d’ensemble des opérateurs de requête standard](http://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2)   
 [Conversion rules for Instance parameters and their impact](http://go.microsoft.com/fwlink/?LinkId=112385)   
 [Extension methods Interoperability between languages](http://go.microsoft.com/fwlink/?LinkId=112386)   
 [Extension methods and Curried Delegates](http://go.microsoft.com/fwlink/?LinkId=112387)   
 [Extension method Binding and Error reporting](http://go.microsoft.com/fwlink/?LinkId=112388)
