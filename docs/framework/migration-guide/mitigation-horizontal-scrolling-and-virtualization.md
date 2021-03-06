---
title: "Atténuation : Défilement horizontal et virtualisation | Microsoft Docs"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d5bafd9b-a3b3-4f92-8241-2aad254fb1a9
caps.latest.revision: 6
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Human Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 37c60fd8a3e3e4e44dc00e278f6edafcdd766c03
ms.contentlocale: fr-fr
ms.lasthandoff: 04/18/2017

---
# <a name="mitigation-horizontal-scrolling-and-virtualization"></a>Atténuation : Défilement horizontal et virtualisation
Cette modification s’applique à un <xref:System.Windows.Controls.ItemsControl> qui effectue sa propre virtualisation dans le sens orthogonal vers la direction de défilement principale. (L’exemple principal est un contrôle <xref:System.Windows.Controls.DataGrid> avec <xref:System.Windows.Controls.DataGrid.EnableColumnVirtualization%2A> défini sur `true`.)  Le résultat de certaines opérations de défilement horizontales a été modifié afin de produire des résultats qui sont plus intuitifs et plus analogues par rapport aux résultats des opérations verticales comparables.  Les opérations spécifiques comprennent **Défilement ici** et **Bord droit** pour utiliser les noms à partir du menu obtenu en double-cliquant sur une barre de défilement horizontale.  Les deux calculent un décalage potentiel et appellent <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset%2A?displayProperty=fullName>.  Après défilement vers le nouveau décalage, les définitions de « ici » ou « bord droit » peuvent avoir été modifiées, car le nouveau contenu dévirtualisé a modifié la valeur de <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth%2A?displayProperty=fullName>.  
  
## <a name="description-of-the-change"></a>Description de la modification  
 Avant [!INCLUDE[net_v462](../../../includes/net-v462-md.md)], l’opération de défilement utilisait simplement le décalage final, même si ce n’est plus « ici » ou le « bord droit ».  Cela entraîne des effets tels que le « rebondissement » du curseur de défilement, comme illustré dans l’exemple.  Supposons qu’un contrôle <xref:System.Windows.Controls.DataGrid> a la valeur <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth%2A> définie sur 1000 et <xref:System.Windows.FrameworkElement.Width%2A> sur 200.  Un défilement vers le « Bord droit » utilise un décalage potentiel de 1000-200 = 800.  Pendant le défilement vers ce décalage, les nouvelles colonnes sont dévirtualisées. Supposons qu’elles sont très larges, afin que la <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth%2A> passe à 2000.  Le défilement se termine par <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset%2A>= 800, et le curseur « rebondit » à proximité du centre de la barre de défilement ; précisément à 800/2000 = 40 %.  
  
 À compter de [!INCLUDE[net_v462](../../../includes/net-v462-md.md)], un nouveau décalage potentiel est recalculé lorsque cette situation se produit. (C’est déjà comme cela que le défilement vertical fonctionne.)  
  
## <a name="impact"></a>Impact  
 La modification génère une expérience plus prévisible et intuitive pour l’utilisateur final, mais il peut également affecter n’importe quelle application qui dépend de la valeur exacte de <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset%2A?displayProperty=fullName> après un défilement horizontal, qu’il soit appelé par l’utilisateur final ou par un appel explicite à <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset%2A?displayProperty=fullName>.  
  
## <a name="mitigation"></a>Atténuation  
 Une application qui utilise une valeur prédite pour <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset%2A?displayProperty=fullName> doit être modifiée afin d’extraire la valeur réelle (et la valeur de <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth%2A>) après un défilement horizontal susceptible de modifier <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth%2A> en raison de la dé-virtualisation.  
  
## <a name="see-also"></a>Voir aussi  
 [Modifications du runtime](../../../docs/framework/migration-guide/runtime-changes-in-the-net-framework-4-6-2.md)
