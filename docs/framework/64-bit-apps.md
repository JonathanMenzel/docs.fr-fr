---
title: Applications 64 bits | Microsoft Docs
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- applications [C++], 64-bit
- 64-bit applications [C++]
- 64-bit programming [C++]
ms.assetid: fd4026bc-2c3d-4b27-86dc-ec5e96018181
caps.latest.revision: 53
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Human Translation
ms.sourcegitcommit: fe32676f0e39ed109a68f39584cf41aec5f5ce90
ms.openlocfilehash: 987c7063c5e6dce10233761b6e37ed102d5878a9
ms.contentlocale: fr-fr
ms.lasthandoff: 05/10/2017

---
# <a name="64-bit-applications"></a>Applications 64 bits
Lorsque vous compilez une application, vous pouvez spécifier si elle doit être exécutée sur un système d'exploitation Windows 64 bits comme une application native ou sous WOW64 (Windows 32 bits sur Windows 64 bits). WOW64 est un environnement de compatibilité qui permet à une application 32 bits de s'exécuter sur un système 64 bits. WOW64 est inclus dans toutes les versions 64 bits du système d'exploitation Windows.  
  
## <a name="running-32-bit-vs-64-bit-applications-on-windows"></a>Comparaison de l'exécution d'applications 32 bits et d'applications 64 bits sur Windows  
 Toutes les applications basées sur les versions 1.0 ou 1.1 de .NET Framework sont traitées comme des applications 32 bits sous un système d'exploitation 64 bits et toujours exécutées sous WOW64 et le Common Language Runtime (CLR) 32 bits. Les applications 32 bits basées sur [!INCLUDE[net_v40_long](../../includes/net-v40-long-md.md)] ou les versions ultérieures s'exécutent également sous WOW64 sur les systèmes 64 bits.  
  
 Visual Studio installe la version 32 bits du CLR sur un ordinateur x86, ainsi que la version 32 bits et la version 64 bits appropriée du CLR sur un ordinateur Windows 64 bits. (Dans la mesure où Visual Studio est une application 32 bits, lorsque celle-ci est installée sur un système 64 bits, elle s'exécute sous WOW64.)  
  
> [!NOTE]
>  En raison de la conception de l'émulation x 86 et du sous-système WOW64 pour la famille de processeurs Itanium, les applications sont limitées à l'exécution sur un seul processeur. Ces facteurs réduisent les performances et l'évolutivité des applications .NET Framework 32 bits qui s'exécutent sur des systèmes Itanium. Dans la mesure du possible, il vaut mieux utiliser [!INCLUDE[net_v40_long](../../includes/net-v40-long-md.md)], qui inclut la prise en charge 64 bits native des systèmes Itanium, pour de meilleures performances et une extensibilité accrue.  
  
 Par défaut, lorsque vous exécutez une application managée 64 bits sur un système d'exploitation Windows 64 bits, vous pouvez créer un objet dont la taille maximale est de 2 gigaoctets (Go). Toutefois, dans le [!INCLUDE[net_v45](../../includes/net-v45-md.md)], vous pouvez augmenter cette limite.  Pour plus d'informations, consultez [\<gcAllowVeryLargeObjects> element](../../docs/framework/configure-apps/file-schema/runtime/gcallowverylargeobjects-element.md).  
  
 De nombreux assemblys s'exécutent de façon identique sur le CLR 32 bits et sur le CLR 64 bits. Toutefois, certains programmes peuvent se comporter différemment, selon le CLR, s'ils contiennent un ou plusieurs des éléments suivants :  
  
-   Des structures contenant des membres qui changent de taille selon la plateforme (par exemple de type pointeur).  
  
-   Opération arithmétique de pointeur qui inclut des tailles constantes.  
  
-   Appel de plateforme incorrect ou déclarations COM qui utilisent `Int32` pour des handles au lieu de `IntPtr`.  
  
-   Code renvoyant `IntPtr` à `Int32`.  
  
 Pour plus d'informations sur le portage d'une application 32 bits destinée à s'exécuter sur le CLR 64 bits, consultez [Migration du code managé 32 bits vers du code managé 64 bits](http://go.microsoft.com/fwlink/?LinkId=150542) dans la Bibliothèque MSDN.  
  
## <a name="general-64-bit-programming-information"></a>Informations générales sur la programmation 64 bits  
 Pour obtenir des informations générales sur la programmation 64 bits, consultez les documents suivants :  
  
-   Pour plus d'informations sur la version 64 bits du CLR sur un ordinateur Windows 64 bits, consultez le [Centre de développement .NET Framework](http://go.microsoft.com/fwlink/?LinkId=37079) sur le site Web MSDN.  
  
-   Dans la documentation [!INCLUDE[winsdkshort](../../includes/winsdkshort-md.md)], consultez le [Guide de programmation pour Windows 64 bits](http://go.microsoft.com/fwlink/p/?LinkId=253512).  
  
-   Pour plus d'informations sur le téléchargement d'une version 64 bits du CLR, consultez la rubrique [Téléchargements du Centre de développement .NET Framework](http://go.microsoft.com/fwlink/?LinkId=50953) sur le site Web MSDN.  
  
-   Pour plus d'informations sur la prise en charge de Visual Studio pour créer des applications 64 bits, consultez [Prise en charge des applications 64 bits par l'IDE Visual Studio](http://msdn.microsoft.com/library/b08ff3ad-c6fd-468f-94d5-01a61aab6833).  
  
## <a name="compiler-support-for-creating-64-bit-applications"></a>Prise en charge de la création d'applications 64 bits par les compilateurs  
 Par défaut, lorsque vous utilisez .NET Framework pour générer une application sur un ordinateur 32 bits ou 64 bits, l'application s'exécute sur un ordinateur 64 bits en tant qu'application native (en d'autres termes, pas sous WOW64). Le tableau suivant répertorie les documents qui permettent d'expliquer comment utiliser les compilateurs Visual Studio pour créer des applications 64 bits qui s'exécutent en tant qu'applications natives ou sous WOW64, ou les deux à la fois.  
  
|Compilateur|Option du compilateur|  
|--------------|---------------------|  
|Visual Basic|[/platform (Visual Basic)](~/docs/visual-basic/reference/command-line-compiler/platform.md)|  
|Visual C#|[/platform (Options du compilateur C#)](~/docs/csharp/language-reference/compiler-options/platform-compiler-option.md)|  
|Visual C++|Vous pouvez créer des applications MSIL (Microsoft Intermediate Language) indépendantes des plateformes en utilisant **/clr:safe**. Pour plus d’informations, consultez l’article [/clr (Compilation pour le Common Language Runtime)](/cpp/build/reference/clr-common-language-runtime-compilation).<br /><br /> Visual C++ inclut un compilateur distinct pour chaque système d'exploitation 64 bits. Pour plus d'informations sur l'utilisation de Visual C++ pour créer des applications natives qui s'exécutent sur un système d'exploitation Windows 64 bits, consultez [Programmation 64 bits](http://msdn.microsoft.com/library/h2k70f3s\(v=vs.80\)).|  
  
## <a name="determining-the-status-of-an-exe-file-or-dll-file"></a>Détermination de l'état d'un fichier .exe ou .dll  
 Pour déterminer si un fichier .exe ou .dll est destiné à être exécuté uniquement sur une plateforme spécifique ou sous WOW64, utilisez [CorFlags.exe (Outil de conversion CorFlags)](../../docs/framework/tools/corflags-exe-corflags-conversion-tool.md) sans options. Vous pouvez également utiliser CorFlags.exe pour modifier l'état de plateforme d'un fichier .exe ou .dll. L'en-tête CLR (ou en-tête COM+ Runtime) d'un assembly Visual Studio possède un numéro de version de runtime majeur ayant 2 pour valeur et un numéro de version de runtime mineur ayant 5 pour valeur. Les applications dont la version de runtime mineure est définie à 0 sont traitées comme des applications héritées et sont toujours exécutées sous WOW64.  
  
 Pour interroger par programme un fichier .exe ou .dll pour voir s'il est destiné à être exécuté uniquement sur une plateforme spécifique ou sous WOW64, utilisez la méthode <xref:System.Reflection.Module.GetPEKind%2A?displayProperty=fullName>.
