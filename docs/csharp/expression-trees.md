---
title: Expression Trees
description: Expression Trees
keywords: .NET, .NET Core
author: BillWagner
ms.author: wiwagn
ms.date: 06/20/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: aceb4719-0d5a-4b19-b01f-b51063bcc54f
ms.translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: e6ec60b6cdbe29def719f7970dad15fad65902e7
ms.contentlocale: fr-fr
ms.lasthandoff: 05/22/2017

---

# <a name="expression-trees"></a>Expression Trees

Si vous avez déjà utilisé LINQ, vous connaissez une bibliothèque enrichie où les types `Func` font partie de l’ensemble d’API. (Si vous ne connaissez pas LINQ, nous vous conseillons de lire le [didacticiel LINQ](linq/index.md) et le didacticiel sur les [expressions lambda](lambda-expressions.md) avant celui-ci.) Les *arborescences d’expressions* fournissent une interaction plus complète avec les arguments qui sont des fonctions.

Vous écrivez des arguments de fonction, généralement à l’aide d’expressions lambda, quand vous créez des requêtes LINQ. Dans une requête LINQ classique, ces arguments de fonction sont transformés en un délégué créé par le compilateur. 

Quand vous souhaitez avoir une interaction plus complète, vous devez utiliser des *arborescences d’expressions*.
Les arborescences d’expressions représentent le code sous forme de structure que vous pouvez examiner, modifier ou exécuter. Ces outils vous permettent de manipuler le code au moment de l’exécution. Vous pouvez écrire du code qui examine les algorithmes en cours d’exécution ou injecte de nouvelles fonctionnalités. Dans des scénarios avancés, vous pouvez modifier les algorithmes en cours d’exécution, et même traduire les expressions C# dans une autre forme en vue d’une exécution dans un autre environnement.

Vous avez probablement déjà écrit du code qui utilise des arborescences d’expressions. Les API LINQ d’Entity Framework acceptent des arborescences d’expressions comme arguments pour le modèle d’expression de requête LINQ.
Cela permet à [Entity Framework](http://docs.efproject.net/en/latest/) de traduire la requête que vous avez écrite en C# en code SQL qui s’exécute dans le moteur de base de données. [Moq](https://github.com/Moq/moq), framework de simulation populaire pour .NET, constitue un autre exemple.

Les sections suivantes de ce didacticiel expliquent en détail ce que sont les arborescences d’expressions, examinent les classes de framework qui prennent en charge les arborescences d’expressions et montrent comment utiliser des arborescences d’expressions. Vous découvrirez comment lire des arborescences d’expressions, créer des arborescences d’expressions, créer des arborescences d’expressions modifiées et exécuter le code représenté par des arborescences d’expressions. Une fois ce didacticiel terminé, vous serez prêt à utiliser ces structures pour créer des algorithmes adaptatifs enrichis.
<style type="text/css"> ol { list-style-type: upper-roman; } </style>
1. [Explication des arborescences d’expressions](expression-trees-explained.md)

    Understand the structure and concepts behind *Expression Trees*.
    
2. [Types de frameworks prenant en charge les arborescences d’expressions](expression-classes.md)
    
    Découvrez les structures et les classes qui définissent et manipulent des arborescences d’expressions.
    
3. [Exécution d’expressions](expression-trees-execution.md)

    Découvrez comment convertir une arborescence d’expressions représentée sous forme d’expression lambda en un délégué, et comment exécuter le délégué résultant.

4. [Interprétation d’expressions](expression-trees-interpreting.md)

    Découvrez comment parcourir et examiner des *arborescences d’expressions* pour comprendre quel est le code représenté par l’arborescence d’expressions.

5. [Création d’expressions](expression-trees-building.md)

    Découvrez comment construire les nœuds d’une arborescence d’expressions et comment générer des arborescences d’expressions.

6. [Traduction d’expressions](expression-trees-translating.md)

    Découvrez comment générer une copie modifiée d’une arborescence d’expressions ou comment traduire une arborescence d’expressions dans un format différent.

7. [Conclusion](expression-trees-summary.md)

    Passez en revue les informations sur les arborescences d’expressions.
    

