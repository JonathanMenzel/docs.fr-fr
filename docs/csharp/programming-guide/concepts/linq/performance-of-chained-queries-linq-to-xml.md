---
title: "Performance des requêtes chaînées (LINQ to XML) (C#) | Microsoft Docs"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: b2f1d715-8946-4dc0-8d56-fb3d1bba54a6
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 3429da268df07900ebe59ed206b927d209b1cf7f
ms.lasthandoff: 03/13/2017


---
# <a name="performance-of-chained-queries-linq-to-xml-c"></a>Performance des requêtes chaînées (LINQ to XML) (C#)
L'un des principaux avantages de LINQ (et LINQ to XML) est que les requêtes chaînées peuvent offrir la même performance qu'une requête unique plus grande et plus complexe.  
  
 Une requête chaînée est une requête qui utilise une autre requête comme source. Par exemple, dans le code simple suivant, `query2` utilise `query1` comme source :  
  
```csharp  
XElement root = new XElement("Root",  
    new XElement("Child", 1),  
    new XElement("Child", 2),  
    new XElement("Child", 3),  
    new XElement("Child", 4)  
);  
  
var query1 = from x in root.Elements("Child")  
             where (int)x >= 3  
             select x;  
  
var query2 = from e in query1  
             where (int)e % 2 == 0  
             select e;  
  
foreach (var i in query2)  
    Console.WriteLine("{0}", (int)i);  
```  
  
 Cet exemple génère la sortie suivante :  
  
```  
4  
```  
  
 Cette requête chaînée offre le même profil de performance que l'itération sur une liste liée.  
  
-   L’axe <xref:System.Xml.Linq.XContainer.Elements%2A> offre globalement la même performance qu’une itération dans une liste liée. <xref:System.Xml.Linq.XContainer.Elements%2A> est implémenté comme un itérateur avec exécution différée. Cela signifie qu'en plus de l'itération sur la liste liée, il effectue certaines tâches comme l'allocation de l'objet itérateur et le suivi de l'état d'exécution. Ces tâches peuvent être divisées en deux catégories : les tâches effectuées lors de la configuration de l'itérateur et les tâches effectuées à chaque itération. Les tâches de configuration représentent une part réduite et fixe du travail, tandis que les tâches effectuées à chaque itération sont proportionnelles au nombre d'éléments de la collection source.  
  
-   Dans `query1`, la clause `where` spécifie que la requête appelle la méthode <xref:System.Linq.Enumerable.Where%2A>. Cette méthode est également implémentée en tant qu'itérateur. Les tâches de configuration se composent de l'instanciation du délégué qui fera référence à l'expression, en plus de la configuration normale d'un itérateur. A chaque itération, le délégué est appelé pour exécuter le prédicat. Les tâches de configuration et les tâches effectuées à chaque itération sont similaires aux tâches effectuées lors de l'itération sur l'axe.  
  
-   Dans `query1`, la clause select spécifie que la requête appelle la méthode <xref:System.Linq.Enumerable.Select%2A>. Cette méthode a le même profil de performance que la méthode <xref:System.Linq.Enumerable.Where%2A>.  
  
-   Dans `query2`, la clause `where` et la `select` clause ont toutes deux le même profil de performance que dans `query1`.  
  
 L'itération sur `query2` est donc directement proportionnelle au nombre d'éléments de la source de la première requête, en d'autres termes, elle suit un algorithme linéaire. Un exemple Visual Basic correspondant aurait le même profil de performance.  
  
 Pour plus d’informations sur les itérateurs, consultez [yield](../../../../csharp/language-reference/keywords/yield.md).  
  
 Pour obtenir un didacticiel plus détaillé sur le chaînage de requêtes, consultez [Didacticiel : Chaînage de requêtes](http://msdn.microsoft.com/library/c08d228a-f07a-4c98-810f-1bf0e8f2257c).  
  
## <a name="see-also"></a>Voir aussi  
 [Performance (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/performance-linq-to-xml.md)
