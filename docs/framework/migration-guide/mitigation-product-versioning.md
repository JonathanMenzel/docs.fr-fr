---
title: "Atténuation : Gestion de versions de produit | Microsoft Docs"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1c4de9d7-9aba-427a-8f38-0ab9bfb8f85e
caps.latest.revision: 15
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Human Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: a6bf9656dee0e6074a8341997abb0e73dc3666f5
ms.contentlocale: fr-fr
ms.lasthandoff: 04/18/2017

---
# <a name="mitigation-product-versioning"></a>Atténuation : Gestion de versions de produit
Dans le [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] et ultérieur, la gestion de versions de produit a changé par rapport aux versions précédentes du .NET Framework (.NET Framework 4, 4.5, 4.5.1 et 4.5.2).  
  
## <a name="product-versioning-changes"></a>Modifications de la gestion de versions de produit  
 Voici le détail des modifications :  
  
-   La valeur de l’entrée `Version` dans la clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` a été remplacée par `4.6.`*xxxxx* pour le .NET Framework 4.6 et ses versions intermédiaires, et par `4.7.`*xxxxx* pour le .NET Framework 4.7. Dans le .NET Framework 4.5, 4.5.1 et 4.5.2, elle était au format `4.5.`*xxxxx*.  
  
-   La gestion des versions des fichiers et des produits pour les fichiers du .NET Framework est passé de l’ancien schéma `4.0.30319.x` au schéma `4.6.X.0` pour le .NET Framework 4.6 et ses versions intermédiaires, et au schéma `4.7.X.0` pour le .NET Framework 4.7 et ses versions intermédiaires. Pour voir ces nouvelles valeurs, cliquez avec le bouton droit sur un fichier, puis affichez ses **Propriétés**.  
  
-   Les attributs <xref:System.Reflection.AssemblyFileVersionAttribute> et <xref:System.Reflection.AssemblyInformationalVersionAttribute> des assemblys managés ont des valeurs <xref:System.Version> au format `4.6.X.0` pour le .NET Framework 4.6 et ses versions intermédiaires, et au format `4.7.X.0` pour le .NET Framework 4.7 et ses versions intermédiaires.  
  
-   Dans le [!INCLUDE[net_v46](../../../includes/net-v46-md.md)], 4.6.1, 4.6.2 et 4.7, la propriété <xref:System.Environment.Version%2A?displayProperty=fullName> retourne la chaîne de version fixe `4.0.30319.42000`. Dans le .NET Framework 4, 4.5, 4.5.1 et 4.5.2, elle retourne les chaînes de version au format `4.0.30319.xxxxx` (par exemple, « 4.0.30319.18010 »). Notez qu’il n’est pas recommandé pour le code d’application d’ajouter de nouvelles dépendances à la propriété <xref:System.Environment.Version%2A?displayProperty=fullName>.  
  
### <a name="handling-the-product-versioning-changes"></a>Gestion des modifications de la gestion de versions de produit  
 En général, les applications doivent s'appuyer sur les techniques recommandées pour la détection d'éléments tels que la version de runtime du .NET Framework et le répertoire d'installation :  
  
-   Pour détecter la version de runtime du .NET Framework, consultez [Guide pratique pour déterminer les versions .NET Framework installées](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md).  
  
-   Pour déterminer le chemin d'installation du .NET Framework, utilisez la valeur de l'entrée `InstallPath` dans la clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`.  
  
    > [!IMPORTANT]
    >  Le nom de la sous-clé est `NET Framework Setup`, et non `.NET Framework Setup`.  
  
-   Pour déterminer le chemin du répertoire du common language runtime .NET Framework, appelez la méthode <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetRuntimeDirectory%2A?displayProperty=fullName>.  
  
-   Pour obtenir la version du CLR, appelez la méthode <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetSystemVersion%2A?displayProperty=fullName>.   Pour le .NET Framework 4 et ses versions intermédiaires (.NET Framework 4.5, 4.5.1, 4.5.2, ainsi que le [!INCLUDE[net_v46](../../../includes/net-v46-md.md)], 4.6.1, 4.6.2 et 4.7), elle retourne la chaîne `v4.0.30319`.  
  
## <a name="see-also"></a>Voir aussi  
 [Modifications du runtime](../../../docs/framework/migration-guide/runtime-changes-in-the-net-framework-4-6.md)
 
