---
title: "Événements (Visual Basic) | Microsoft Docs"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- events [Visual Basic], about events
- events [Visual Basic]
ms.assetid: 8fb0353a-e41b-4e23-b78f-da65db832f70
caps.latest.revision: 12
author: dotnet-bot
ms.author: dotnetcontent
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
ms.sourcegitcommit: fe32676f0e39ed109a68f39584cf41aec5f5ce90
ms.openlocfilehash: 59851175865939243260702470955fe0dea38495
ms.contentlocale: fr-fr
ms.lasthandoff: 05/10/2017

---
# <a name="events-visual-basic"></a>Événements (Visual Basic)
On peut se représenter un projet [!INCLUDE[vsprvs](../../../../csharp/includes/vsprvs_md.md)] comme une série de procédures qui s’exécutent de façon séquentielle, mais, en réalité, la plupart des programmes sont pilotés par des événements, ce qui signifie que le flux d’exécution est déterminé par des occurrences externes nommées *événements*.  
  
 Un événement est un signal qui informe l’application que quelque chose d’important s’est produit. Par exemple, lorsqu’un utilisateur clique sur un contrôle sur un formulaire, le formulaire peut déclencher un événement `Click` et appeler une procédure qui gère l’événement. Les événements permettent également à des tâches distinctes de communiquer. Supposons, par exemple, que votre application exécute une tâche de tri de façon distincte de l’application principale. Si un utilisateur annule le tri, votre application peut envoyer un événement d’annulation demandant l’arrêt du processus de tri.  
  
## <a name="event-terms-and-concepts"></a>Concepts et termes relatifs aux événements  
 Cette section décrit les termes et les concepts utilisés avec les événements en [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].  
  
### <a name="declaring-events"></a>Déclaration d'événements  
 On déclare des événements dans des classes, des structures, des modules et des interfaces à l’aide du mot clé `Event`, comme dans l’exemple suivant :  
  
 [!code-vb[VbVbalrEvents#24](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_1.vb)]  
  
### <a name="raising-events"></a>Déclencher des événements  
 Un événement est comme un message qui annonce que quelque chose d’important s’est produit. L’acte de diffusion du message est appelé *déclenchement* de l’événement. En [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)], on déclenche des événements avec l’instruction `RaiseEvent`, comme dans l’exemple suivant :  
  
 [!code-vb[VbVbalrEvents#25](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_2.vb)]  
  
 Les événements doivent être déclenchés dans la portée de la classe, du module ou de la structure dans lequel ils sont déclarés. Par exemple, une classe dérivée ne peut pas déclencher des événements hérités d’une classe de base.  
  
### <a name="event-senders"></a>Émetteurs d’événements  
 Tout objet capable de déclencher un événement est un *émetteur d’événements*, également appelé *source de l’événement*. Les formulaires, les contrôles et les objets définis par l’utilisateur sont des exemples d’émetteurs d’événements.  
  
### <a name="event-handlers"></a>Gestionnaires d'événements  
 Les *gestionnaires d’événements* sont des procédures qui sont appelées lorsqu’un événement correspondant se produit. Une sous-routine valide avec une signature correspondante peut être utilisée comme gestionnaire d’événements. Il n’est pas possible d’utiliser une fonction comme gestionnaire d’événements, toutefois, car elle ne peut pas retourner de valeur à la source de l’événement.  
  
 [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] utilise une convention d’affectation de noms standard pour les gestionnaires d’événements, qui associe le nom de l’émetteur de l’événement, un trait de soulignement et le nom de l’événement. Par exemple, l’événement `Click` d’un bouton nommé `button1` serait nommé `Sub button1_Click`.  
  
> [!NOTE]
>  Nous recommandons d’utiliser cette convention d’affectation de noms pour définir des gestionnaires d’événements pour vos propres événements, mais ce n’est pas obligatoire ; il est possible d’utiliser n’importe quel nom de sous-routine valide.  
  
## <a name="associating-events-with-event-handlers"></a>Associer des événements à des gestionnaires d’événements  
 Pour qu’un gestionnaire d’événements soit utilisable, il faut l’associer à un événement avec l’instruction `Handles` ou `AddHandler`.  
  
### <a name="withevents-and-the-handles-clause"></a>WithEvents et la clause Handles  
 L’instruction `WithEvents` et la clause `Handles` représentent un moyen déclaratif de spécifier des gestionnaires d’événements. Un événement déclenché par un objet déclaré avec le mot clé `WithEvents` peut être géré par n’importe quelle procédure avec une instruction `Handles` pour cet événement, comme l’illustre l’exemple suivant :  
  
 [!code-vb[VbVbalrEvents#1](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_3.vb)]  
  
 L’instruction `WithEvents` et la clause `Handles` représentent souvent le meilleur choix pour les gestionnaires d’événements, car la syntaxe déclarative qu’elles utilisent facilite le codage, la lecture et le débogage de la gestion des événements. Toutefois, soyez conscient des limitations suivantes de l’utilisation de variables `WithEvents` :  
  
-   Il n’est pas possible d’utiliser une variable `WithEvents` comme variable objet. Autrement dit, vous ne pouvez pas la déclarer comme `Object` : vous devez spécifier le nom de classe lorsque vous déclarez la variable.  
  
-   Dans le mesure où les événements partagés ne sont pas liés aux instances de classe, vous ne pouvez pas utiliser `WithEvents` pour les gérer de façon déclarative. De même, vous ne pouvez pas utiliser `WithEvents` ni `Handles` pour gérer les événements d’une `Structure`. Dans les deux cas, vous pouvez utiliser l’instruction `AddHandler` pour gérer ces événements.  
  
-   Il n’est pas possible de créer des tableaux de variables `WithEvents`.  
  
 Les variables `WithEvents` permettent à un même gestionnaire d’événements de gérer un ou plusieurs types d’événements, ou à un ou plusieurs gestionnaires d’événements de gérer le même type d’événements.  
  
 Bien que la clause `Handles` représente le moyen standard d’associer un événement à un gestionnaire d’événements, elle est limitée à l’association d’événements avec des gestionnaires d’événements à la compilation.  
  
 Dans certains cas, par exemple des événements associés à des formulaires ou des contrôles, [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] écrase automatiquement un gestionnaire d’événements vide et l’associe à un événement. Par exemple, lorsqu’on double-clique sur un bouton de commande sur un formulaire en mode Création, [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] crée un gestionnaire d’événements vide et une variable `WithEvents` pour le bouton de commande, comme dans le code suivant :  
  
 [!code-vb[VbVbalrEvents#26](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_4.vb)]  
  
### <a name="addhandler-and-removehandler"></a>AddHandler et RemoveHandler  
 L’instruction `AddHandler` est similaire à la clause `Handles` en ce que les deux permettent de spécifier un gestionnaire d’événements. Toutefois, `AddHandler`, utilisé avec `RemoveHandler`, offre une plus grande flexibilité que la clause `Handles`, ce qui permet d’ajouter, de supprimer et de modifier dynamiquement le gestionnaire d’événements associé à l’événement. Si vous souhaitez gérer des événements partagés ou des événements d’une structure, vous devez utiliser `AddHandler`.  
  
 `AddHandler` prend deux arguments : le nom d’un événement à partir d’un émetteur d’événements tel qu’un contrôle et une expression qui a pour valeur un délégué. Il n’est pas nécessaire de spécifier explicitement la classe déléguée lorsqu’on utilise `AddHandler`, étant donné que l’instruction `AddressOf` retourne toujours une référence au délégué. L’exemple suivant associe un gestionnaire d’événements à un événement déclenché par un objet :  
  
 [!code-vb[VbVbalrEvents#28](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_5.vb)]  
  
 `RemoveHandler`, qui déconnecte un événement d’un gestionnaire d’événements, utilise la même syntaxe que `AddHandler`. Exemple :  
  
 [!code-vb[VbVbalrEvents#29](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_6.vb)]  
  
 Dans l’exemple suivant, un gestionnaire d’événements est associé à un événement, et l’événement est déclenché. Le gestionnaire d’événements intercepte l’événement et affiche un message.  
  
 Ensuite, le premier gestionnaire d’événements est supprimé et un autre gestionnaire d’événements est associé à l’événement. Lorsque l’événement est déclenché à nouveau, un autre message s’affiche.  
  
 Enfin, le second gestionnaire d’événements est supprimé et l’événement est déclenché pour la troisième fois. Dans la mesure où il n’y a plus de gestionnaire d’événements associé à l’événement, aucune action n’est effectuée.  
  
 [!code-vb[VbVbalrEvents#38](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_7.vb)]  
  
## <a name="handling-events-inherited-from-a-base-class"></a>Gérer des événements hérités d’une classe de base  
 Les *classes dérivées*, classes qui héritent des caractéristiques d’une classe de base, peuvent gérer des événements déclenchés par leur classe de base avec l’instruction `Handles``MyBase`.  
  
#### <a name="to-handle-events-from-a-base-class"></a>Gérer des événements provenant d’une classe de base  
  
-   Déclarez un gestionnaire d’événements dans la classe dérivée en ajoutant une instruction `Handles MyBase.`*eventname* à la ligne de déclaration de votre procédure de gestionnaire d’événements, où *eventname* est le nom de l’événement dans la classe de base que vous gérez. Exemple :  
  
     [!code-vb[VbVbalrEvents#12](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/events_8.vb)]  
  
## <a name="related-sections"></a>Rubriques connexes  
  
|Titre|Description|  
|-----------|-----------------|  
|[Procédure pas à pas : déclaration et déclenchement des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-declaring-and-raising-events.md)|Fournit une description étape par étape de la déclaration et du déclenchement des événements pour une classe.|  
|[Procédure pas à pas : gestion des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-handling-events.md)|Montre comment écrire une procédure de gestionnaire d’événements.|  
|[Guide pratique : déclarer des événements personnalisés pour éviter les blocages](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)|Montre comment définir un événement personnalisé qui permet d’appeler ses gestionnaires d’événements de façon asynchrone.|  
|[Guide pratique : déclarer des événements personnalisés pour économiser la mémoire](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-conserve-memory.md)|Montre comment définir un événement personnalisé qui utilise la mémoire uniquement lorsque l’événement est géré.|  
|[Dépannage des gestionnaires d’événements hérités en Visual Basic](../../../../visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)|Répertorie les problèmes courants qui surviennent avec les gestionnaires d’événements dans les composants hérités.|  
|[Événements](../../../../standard/events/index.md)|Fournit une vue d’ensemble du modèle d’événement dans [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)].|  
|[Création de gestionnaires d’événements dans Windows Forms](https://msdn.microsoft.com/library/dacysss4.aspx)|Explique comment utiliser des événements associés à des objets Windows Forms.|  
|[Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)|Fournit une vue d’ensemble des délégués en Visual Basic.|
