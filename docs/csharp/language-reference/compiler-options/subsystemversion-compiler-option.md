---
title: "-subsystemversion (Options du compilateur C#) | Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: a99fce81-9d92-4813-9874-bee777041445
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
ms.openlocfilehash: 8766904cad739b29c7dfe80b29305ea2b3bd2e6f
ms.lasthandoff: 03/13/2017

---
# <a name="subsystemversion-c-compiler-options"></a>/subsystemversion (Options du compilateur C#)
Spécifie la version minimale du sous-système sur lequel le fichier exécutable généré peut s’exécuter, déterminant ainsi les versions de Windows sur lesquelles le fichier exécutable peut s’exécuter. En règle générale, cette option garantit que le fichier exécutable peut tirer parti de fonctionnalités de sécurité particulières qui ne sont pas disponibles avec des versions antérieures de Windows.  
  
> [!NOTE]
>  Pour spécifier le sous-système lui-même, utilisez l’option du compilateur [/target](../../../csharp/language-reference/compiler-options/target-compiler-option.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
/subsystemversion:major.minor  
```  
  
#### <a name="parameters"></a>Paramètres  
 `major.minor`  
 Version minimale requise du sous-système, telle qu’elle est exprimée dans une notation par points pour les versions majeure et mineure. Par exemple, vous pouvez spécifier qu’une application ne peut pas s’exécuter sur un système d’exploitation antérieur à Windows 7 si vous définissez la valeur de cette option sur 6.01, comme décrit dans le tableau plus loin dans cette rubrique. Vous devez spécifier les valeurs de `major` et `minor` en tant qu’entiers.  
  
 Les zéros à gauche du numéro de version `minor` ne modifient pas la version, contrairement aux zéros de droite. Par exemple, 6.1 et 6.01 font référence à la même version, mais 6.10 fait référence à une version différente. Nous vous recommandons d’exprimer la version mineure avec deux chiffres pour éviter toute confusion.  
  
## <a name="remarks"></a>Remarques  
 Le tableau suivant répertorie les versions courantes de sous-système de Windows.  
  
|Version Windows|Version de sous-système|  
|---------------------|-----------------------|  
|Windows 2000|5.00|  
|Windows XP|5.01|  
|Windows Server 2003|5.02|  
|Windows Vista|6.00|  
|Windows 7|6.01|  
|Windows Server 2008|6.01|  
|[!INCLUDE[win8](../../../csharp/language-reference/compiler-options/includes/win8_md.md)]|6.02|  
  
## <a name="default-values"></a>Valeurs par défaut  
 La valeur par défaut de l’option du compilateur **/subsystemversion** dépend des conditions répertoriées dans la liste suivante :  
  
-   La valeur par défaut est 6.02 si l’une quelconque des options du compilateur de la liste suivante est définie :  
  
    -   [/target:appcontainerexe](../../../csharp/language-reference/compiler-options/target-appcontainerexe-compiler-option.md)  
  
    -   [/target:winmdobj](../../../csharp/language-reference/compiler-options/target-winmdobj-compiler-option.md)  
  
    -   [/platform:arm](../../../csharp/language-reference/compiler-options/platform-compiler-option.md)  
  
-   La valeur par défaut est 6.00 si vous utilisez MSBuild, si vous ciblez [!INCLUDE[net_v45](../../../csharp/language-reference/compiler-options/includes/net_v45_md.md)] et si vous n’avez défini aucune des options du compilateur spécifiées plus haut dans cette liste.  
  
-   La valeur par défaut est 4.00 si aucune des conditions précédentes n’est vraie.  
  
## <a name="setting-this-option"></a>Définition de cette option  
 Pour définir l’option du compilateur **/subsystemversion** dans Visual Studio, vous devez ouvrir le fichier .csproj et spécifier une valeur pour la propriété `SubsystemVersion` dans le code XML MSBuild. Vous ne pouvez pas définir cette option dans l’environnement IDE de Visual Studio. Pour plus d’informations, consultez « Valeurs par défaut » plus haut dans cette rubrique ou [Propriétés communes des projets MSBuild](https://docs.microsoft.com/visualstudio/msbuild/common-msbuild-project-properties).  
  
## <a name="see-also"></a>Voir aussi  
 [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
