---
title: "/errorreport (Options du compilateur C#) | Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /errorreport
dev_langs:
- CSharp
helpviewer_keywords:
- -errorreport compiler option [C#]
- errorreport compiler option [C#]
- /errorreport compiler option [C#]
ms.assetid: bd0e7493-b79d-4369-9c3f-ba26ebdfbedf
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
ms.translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 34e7e3b8c6a9f645ec1b359095c2d289afd1370a
ms.contentlocale: fr-fr
ms.lasthandoff: 05/22/2017

---
# <a name="errorreport-c-compiler-options"></a>/errorreport (Options du compilateur C#)
Cette option fournit un moyen pratique de signaler une erreur interne du compilateur C# à Microsoft.  
  
> [!NOTE]
>  Sur Windows Vista et Windows Server 2008, les paramètres de rapport d’erreurs que vous spécifiez pour Visual Studio ne remplacent pas les paramètres définis par l’intermédiaire de Rapport d’erreurs Windows. Les paramètres de Rapport d’erreurs Windows ont toujours priorité sur les paramètres de signalement d’erreurs de Visual Studio.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
/errorreport:{ none | prompt | queue | send }  
```  
  
## <a name="arguments"></a>Arguments  
 **none**  
 Les rapports sur les erreurs internes du compilateur ne seront pas collectés ni envoyés à Microsoft.  
  
 **prompt**  
 Vous invite à envoyer un rapport dès qu'une erreur interne du compilateur se produit. **prompt** est la valeur par défaut quand vous compilez une application dans l’environnement de développement.  
  
 **queue**  
 Met le rapport d’erreurs en file d’attente. Quand vous ouvrez une session avec des informations d’identification administratives, vous pouvez signaler toute défaillance qui s’est produite depuis votre dernière connexion. Vous ne serez pas invité à envoyer des rapports d’échecs plus d’une fois tous les trois jours. **queue** est la valeur par défaut quand vous compilez une application à partir de la ligne de commande.  
  
 **send**  
 Envoie automatiquement des rapports d’erreurs internes du compilateur à Microsoft. Pour activer cette option, vous devez tout d’abord accepter la politique de collecte de données de Microsoft. La première fois que vous spécifiez **/errorreport:send** sur un ordinateur, un message du compilateur vous dirige vers un site web qui affiche la politique de collecte de données de Microsoft.  
  
 Cette option dépend des paramètres du Registre. Pour plus d’informations sur la façon de définir les valeurs appropriées dans le Registre, consultez [Guide pratique pour activer le rapport d’erreurs automatique dans les outils en ligne de commande de Visual Studio 2008](http://go.microsoft.com/fwlink/?LinkID=184695) sur le site web MSDN.  
  
## <a name="remarks"></a>Remarques  
 Une erreur interne du compilateur se produit quand le compilateur ne peut pas traiter un fichier de code source. Quand une telle erreur se produit, le compilateur ne génère pas de fichier de sortie ni de diagnostic utile que vous pouvez utiliser pour corriger votre code.  
  
 Dans les versions précédentes, quand vous receviez une erreur interne du compilateur, vous étiez invité à contacter le Support technique Microsoft pour signaler le problème. En utilisant **/errorreport**, vous pouvez fournir des informations sur l’erreur interne du compilateur à l’équipe Visual C#. Vos rapports d’erreurs peuvent aider à améliorer les versions ultérieures du compilateur.  
  
 La capacité d’un utilisateur à envoyer des rapports dépend des autorisations de stratégie ordinateur et utilisateur.  
  
 Pour plus d’informations sur le débogueur d’erreur, consultez [Description de l’outil Dr Watson pour Windows (Drwtsn32.exe)](http://go.microsoft.com/fwlink/?LinkId=147286).  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1.  Ouvrez la page **Propriétés** du projet. Pour plus d’informations, consultez [Générer, page du Concepteur de projets (C#)](https://docs.microsoft.com/visualstudio/ide/reference/build-page-project-designer-csharp).  
  
2.  Cliquez sur la page de propriétés **Générer**.  
  
3.  Cliquez sur le bouton **Avancées** .  
  
4.  Modifiez la propriété **Rapport d’erreurs du compilateur interne**.  
  
 Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.ErrorReport%2A>.  
  
## <a name="see-also"></a>Voir aussi  
 [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
