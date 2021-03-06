---
title: "Visite guidée de C# - Guide C# | Microsoft Docs"
description: "Vous débutez en C# ? Découvrez les principes de base du langage."
keywords: ".NET, .NET Core, C#, Abécédaire du langage C#, Guide du langage C#"
author: BillWagner
ms.author: wiwagn
ms.date: 08/10/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: ebc727cd-8112-42e7-b59c-3c2873ad661c
ms.translationtype: Human Translation
ms.sourcegitcommit: 4437ce5d344cf06d30e31911def6287999fc6ffc
ms.openlocfilehash: f122f59dd6f194facd98f4c6fa7f84c658c02a90
ms.contentlocale: fr-fr
ms.lasthandoff: 05/23/2017

---

# <a name="a-tour-of-the-c-language"></a>Présentation rapide du langage C#  

C# (prononcé « C Sharp ») est un langage de programmation simple, moderne, orienté objet et de type sécurisé. C# prend sa source dans la famille de langages C et sera immédiatement reconnaissable aux programmeurs en C, C++, Java et JavaScript.

C# est un langage orienté objet, mais C# inclut de plus la prise en charge de la programmation ***orientée composant***. La conception logicielle moderne s’appuie de plus en plus sur les composants logiciels sous la forme de packages de fonctionnalités autonomes et autodescriptifs. Point important, ces composants présentent un modèle de programmation avec propriétés, méthodes et événements ; ils ont des attributs qui fournissent des informations déclaratives sur le composant ; et ils intègrent leur propre documentation. C# fournit des constructions de langage qui prennent directement en charge ces concepts, ce qui fait de C# un langage très naturel pour créer et utiliser des composants logiciels.

Plusieurs fonctionnalités de C# participent à la construction d’applications robustes et fiables : le ***garbage collection*** récupère automatiquement la mémoire occupée par les objets inutilisés et inaccessibles ; la ***gestion des exceptions*** fournit une approche structurée et extensible de la détection d’erreurs et la récupération ; et, grâce à la conception ***de type sécurisé*** du langage, il est impossible de lire des variables non initialisées, d’indexer des tableaux au-delà de leurs limites et d’effectuer des transtypages non contrôlés.

C# a un ***système de type unifié***. Tous les types C#, y compris les types primitifs tels que `int` et `double`, héritent d’un seul type `object` racine. Par conséquent, tous les types partagent un ensemble d’opérations communes, et des valeurs de tous types peuvent être stockées, transmises et exploitées de manière cohérente. En outre, C# prend en charge les types référence et les types valeur définis par l’utilisateur, ce qui permet l’allocation dynamique d’objets, ainsi que le stockage en ligne de structures légères.

Pour que les bibliothèques et les programmes C# puissent évoluer au fil du temps de manière compatible, l’accent a été mis sur la ***gestion des versions*** dans la conception de C#. De nombreux langages de programmation n’accordent que peu d’attention à ce problème ; par conséquent, les programmes écrits dans ces langages s’arrêtent plus souvent que nécessaire lors de l’introduction de versions plus récentes des bibliothèques dépendantes. Certains aspects de la conception de C# ont été directement influencés par les considérations relatives à la gestion des versions, notamment les modificateurs `virtual` et `override` distincts, les règles de résolution des surcharges de méthodes et la prise en charge des déclarations explicites de membres d’interface.

## <a name="hello-world"></a>Hello World

Le programme « Hello, World » est souvent utilisé pour présenter un langage de programmation. Le voici en C# :

[!code-csharp[Hello World](../../../samples/snippets/csharp/tour/hello/Program.cs#L1-L8)]

Les fichiers sources C# ont généralement l’extension de fichier `.cs`. Si l’on suppose que le programme « Hello, World » est stocké dans le fichier `hello.cs`, le programme peut être compilé en ligne de commande :

```console
csc hello.cs
```

ce qui génère un assembly exécutable nommé hello.exe. Voici la sortie produite par cette application lorsqu’elle est exécutée :

```console
Hello, World
```

> [!IMPORTANT]
> La commande `csc` effectue la compilation pour la totalité du framework ; elle n’est pas nécessairement disponible sur toutes les plateformes.


Le programme « Hello, World » commence par une directive `using` qui fait référence à l’espace de noms `System`. Les espaces de noms représentent un moyen hiérarchique d’organiser les bibliothèques et les programmes C#. Les espaces de noms contiennent des types et d’autres espaces de noms ; par exemple, l’espace de noms `System` contient plusieurs types, notamment la classe `Console` référencée dans le programme, et d’autres espaces de noms, tels que `IO` et `Collections`. Une directive `using` qui fait référence à un espace de noms donné permet l’utilisation non qualifiée des types membres de cet espace de noms. En raison de la directive `using`, le programme peut utiliser `Console.WriteLine` comme raccourci pour `System.Console.WriteLine`.

La classe `Hello` déclarée par le programme « Hello, World » a un membre unique, la méthode nommée `Main`. La méthode `Main` est déclarée avec le modificateur statique. Si les méthodes d’instance peuvent faire référence à une instance d’objet englobante particulière avec le mot clé `this`, les méthodes statiques fonctionnent sans référence à un objet particulier. Par convention, une méthode statique nommée `Main` sert de point d’entrée d’un programme.

La sortie du programme est générée par la méthode `WriteLine` de la classe `Console` dans l’espace de noms `System`. Cette classe est fournie par les bibliothèques de classes standard, qui, par défaut, sont référencées automatiquement par le compilateur.

Il y a beaucoup d’autres choses à apprendre sur C#.  Les rubriques suivantes fournissent une vue d’ensemble des éléments du langage C#. Ces vues d’ensemble fournissent des informations de base sur l’ensemble des éléments du langage et vous donnent les informations nécessaires pour explorer plus en détails les éléments du langage C# :

* [Structure du programme](program-structure.md)
    - Découvrez les concepts clés d’organisation du langage C# : ***programmes***, ***espaces de noms***, ***types***, ***membres*** et ***assemblys***.
* [Types et variables](types-and-variables.md)
    - Découvrez les ***types valeur***, les ***types référence*** et les ***variables*** en langage C#.
* [Expressions](expressions.md)
    - Les ***expressions*** sont construites à partir de ***d’opérandes*** et ***d’opérateurs***. Les expressions produisent une valeur.
* [Instructions](statements.md)
    - On utilise des ***instructions*** pour exprimer les actions d’un programme.
* [Classes et objets](classes-and-objects.md)
    - Les ***classes*** représentent le type le plus fondamental de C#. Les ***objets*** sont des instances d’une classe. Les classes sont générées à l’aide de ***membres***, qui sont également traités dans cette rubrique.
* [Structures](structs.md)
    - Les ***structures*** sont des structures de données qui, contrairement aux classes, sont des types valeur.
* [Tableaux](arrays.md)
    - Un ***tableau*** est une structure de données contenant un certain nombre de variables accessibles par le biais d’indices calculés.
* [Interfaces](interfaces.md)
    - Une ***interface*** définit un contrat qui peut être implémenté par des classes et des structs. Une interface peut contenir des méthodes, des propriétés, des événements et des indexeurs. Une interface ne fournit pas d’implémentations des membres qu’elle définit ; elle spécifie simplement les membres qui doivent être fournis par les classes ou les structs qui implémentent l’interface.
* [Énumérations](enums.md)
    - Un ***type enum*** est un type valeur distinct avec un ensemble de constantes nommées.
* [Délégués](delegates.md)
    - Un ***type délégué*** représente des références à des méthodes avec une liste de paramètres et un type de retour particuliers. Les délégués permettent de traiter les méthodes en tant qu’entités qui peuvent être affectées à des variables et passées comme paramètres. Les délégués sont similaires au concept de pointeurs de fonction dans d’autres langages, mais, contrairement aux pointeurs de fonction, les délégués sont orientés objet et de type sécurisé.
* [Attributs](attributes.md)
     * Les ***attributs*** permettent aux programmes de spécifier des informations déclaratives supplémentaires sur les types, les membres et d’autres entités.

>[!div class="step-by-step"]
[Suivant](program-structure.md)

