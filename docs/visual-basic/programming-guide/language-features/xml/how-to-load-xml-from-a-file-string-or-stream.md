---
title: "Comment : charger du code XML à partir d’un fichier, une chaîne ou un flux de données (Visual Basic) | Documents Microsoft"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- XML [Visual Basic], loading
- LINQ to XML [Visual Basic], loading XML from files
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
caps.latest.revision: 13
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 242c8b79cbe1329b6f53e9fd4e5495d4a157e08c
ms.contentlocale: fr-fr
ms.lasthandoff: 03/13/2017

---
# <a name="how-to-load-xml-from-a-file-string-or-stream-visual-basic"></a>Comment : charger du code XML à partir d'un fichier, d'une chaîne ou d'un flux (Visual Basic)
Vous pouvez créer [littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md) et les remplir avec le contenu à partir d’une source externe, comme un fichier, une chaîne ou un flux de données à l’aide de plusieurs méthodes. Ces méthodes sont illustrées dans les exemples suivants.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-load-xml-from-a-file"></a>Charger XML à partir d’un fichier  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement>ou <xref:System.Xml.Linq.XDocument>objet à partir d’un fichier, utilisez la `Load` méthode.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement> Cette méthode peut prendre un chemin d’accès de fichier, un flux de texte ou un flux de données XML comme entrée.  
  
     L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Load%28System.String%29>méthode pour remplir un <xref:System.Xml.Linq.XDocument>objet XML à partir d’un fichier texte.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XDocument.Load%28System.String%29>  
  
     [!code-vb[VbXMLSamples&#43;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_1.vb)]  
  
### <a name="to-load-xml-from-a-string"></a>Charger XML à partir d’une chaîne  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement>ou <xref:System.Xml.Linq.XDocument>de l’objet à partir d’une chaîne, vous pouvez utiliser la `Parse` méthode.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement>  
  
     L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName>méthode pour remplir un <xref:System.Xml.Linq.XDocument>objet XML à partir d’une chaîne.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName>  
  
     [!code-vb[VbXMLSamples&#47;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_2.vb)]  
  
### <a name="to-load-xml-from-a-stream"></a>Charger XML à partir d’un flux de données  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement>ou <xref:System.Xml.Linq.XDocument>de l’objet à partir d’un flux de données, vous pouvez utiliser la `Load` (méthode) ou la <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>méthode.</xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName> </xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement>  
  
 L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XNode.ReadFrom%2A>méthode pour remplir un <xref:System.Xml.Linq.XDocument>objet XML à partir d’un flux XML.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XNode.ReadFrom%2A>  
  
 [!code-vb[VbXMLSamples&#46;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_3.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName></xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName></xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName></xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName></xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName></xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>   
 [Littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)   
 [Manipulation de XML en Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)

