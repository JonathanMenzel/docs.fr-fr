---
title: "Transformation fonctionnelle de données XML (C#) | Microsoft Docs"
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
ms.assetid: 0ccb9251-38d7-44e3-9b84-1b5fe25e4b59
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: f465d274bcaab257a2eee3e8fc2adb17767204c1
ms.lasthandoff: 03/13/2017


---
# <a name="functional-transformation-of-xml-c"></a>Transformation fonctionnelle de données XML (C#)
Cette rubrique traite de l'approche de transformation fonctionnelle pure permettant de modifier des documents XML et l'oppose à une approche procédurale.  
  
## <a name="modifying-an-xml-document"></a>Modification d'un document XML  
 L'une des tâches les plus courantes pour un programmeur XML consiste à transformer du code XML d'une forme en une autre. La forme d'un document XML est la structure du document, qui inclut les éléments suivants :  
  
-   la hiérarchie exprimée par le document ;  
  
-   les noms des éléments et des attributs ;  
  
-   les types de données des éléments et attributs.  
  
 En général, l'approche la plus efficace pour transformer du code XML d'une forme en une autre consiste à utiliser la transformation fonctionnelle pure. Avec cette approche, la principale tâche du programmeur est de créer une transformation qui est appliquée à l'ensemble du document XML (ou à un ou plusieurs nœuds strictement définis). La transformation fonctionnelle offre sans aucun doute la plus grande facilité de codage (une fois que le programmeur s'est familiarisé avec cette approche) et la plus grande facilité de maintenance du code, et elle est souvent plus compacte que les autres approches.  
  
### <a name="xml-functional-transformational-technologies"></a>Technologies de transformation fonctionnelle XML  
 Microsoft propose deux technologies de transformation fonctionnelle pour une utilisation sur des documents XML : XSLT et LINQ to XML. XSLT est pris en charge dans l’espace de noms managé <xref:System.Xml.Xsl> et dans l’implémentation COM native de MSXML. Bien que XSLT soit une technologie robuste pour la manipulation de documents XML, elle requiert un savoir-faire dans un domaine spécialisé, à savoir le langage XSLT et ses API de prise en charge.  
  
 LINQ to XML procure les outils nécessaires pour coder des transformations fonctionnelles pures de manière expressive et puissante, dans du code C# ou Visual Basic. Par exemple, bon nombre des exemples dans la documentation LINQ to XML utilisent une approche fonctionnelle pure. En outre, dans le [Didacticiel : manipulation de contenu dans un document WordprocessingML (C#)](../../../../csharp/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md), nous utilisons LINQ to XML dans une approche fonctionnelle afin de manipuler des informations dans un document Microsoft Word.  
  
 Pour une comparaison plus approfondie de LINQ to XML et des autres technologies XML Microsoft, consultez [LINQ to XML, différences par rapport à d’autres technologies XML](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-vs-other-xml-technologies.md).  
  
 XSLT est l'outil recommandé pour les transformations centrées sur les documents lorsque le document source a une structure irrégulière. Toutefois, LINQ to XML peut également effectuer des transformations centrées sur les documents. Pour plus d’informations, consultez [Guide pratique pour utiliser des annotations pour transformer des arborescences LINQ to XML en un style XSLT (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-use-annotations-to-transform-linq-to-xml-trees-in-an-xslt-style.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction aux transformations fonctionnelles pures (C#)](../../../../csharp/programming-guide/concepts/linq/introduction-to-pure-functional-transformations.md)   
 [Didacticiel : manipulation de contenu dans un document WordprocessingML (C#)](../../../../csharp/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md)   
 [LINQ to XML, différences par rapport à d’autres technologies XML](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-vs-other-xml-technologies.md)
