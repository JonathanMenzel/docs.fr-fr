---
title: "Guide pratique pour lire des données d’objet à partir d’un fichier XML (C#) | Microsoft Docs"
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
ms.assetid: 6ad60d96-a4d9-48e6-a8b0-d7f6f803cafa
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: c5f8c23a86c7a09d6f8d0b8c6f1684a38d0336a3
ms.lasthandoff: 03/13/2017

---
# <a name="how-to-read-object-data-from-an-xml-file-c"></a>Guide pratique pour lire des données d’objet à partir d’un fichier XML (C#)
Cet exemple lit les données d’objet écrites précédemment dans un fichier XML à l’aide de la classe <xref:System.Xml.Serialization.XmlSerializer>.  
  
## <a name="example"></a>Exemple  
  
```csharp  
public class Book  
{  
    public String title;  
}         
  
public void ReadXML()  
{  
    // First write something so that there is something to read ...  
    var b = new Book { title = "Serialization Overview" };  
    var writer = new System.Xml.Serialization.XmlSerializer(typeof(Book));  
    var wfile = new System.IO.StreamWriter(@"c:\temp\SerializationOverview.xml");  
    writer.Serialize(wfile, b);  
    wfile.Close();  
  
    // Now we can read the serialized book ...  
    System.Xml.Serialization.XmlSerializer reader =   
        new System.Xml.Serialization.XmlSerializer(typeof(Book));  
    System.IO.StreamReader file = new System.IO.StreamReader(  
        @"c:\temp\SerializationOverview.xml");  
    Book overview =  (Book)reader.Deserialize(file);  
    file.Close();  
  
    Console.WriteLine(overview.title);  
  
}  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Remplacez le nom du fichier « c:\temp\SerializationOverview.xml » par le nom du fichier qui contient les données sérialisées. Pour plus d’informations sur la sérialisation des données, consultez [Guide pratique pour écrire des données d’objet dans un fichier XML (C#)](../../../../csharp/programming-guide/concepts/serialization/how-to-write-object-data-to-an-xml-file.md).  
  
 La classe doit disposer d’un constructeur public sans paramètres.  
  
 Seuls les propriétés et les champs publics sont désérialisés.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   La classe qui est sérialisée n’a pas de constructeur public sans paramètres.  
  
-   Les données du fichier ne représentent pas les données de la classe à désérialiser.  
  
-   Le fichier n’existe pas (<xref:System.IO.IOException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Vérifiez toujours les entrées et ne désérialisez jamais les données provenant d’une source non fiable. L’objet recréé s’exécute sur un ordinateur local avec les autorisations du code qui l’a désérialisé. Vérifiez toutes les entrées avant d'utiliser les données dans votre application.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IO.StreamWriter>   
 [Guide pratique pour écrire des données d’objet dans un fichier XML (C#)](../../../../csharp/programming-guide/concepts/serialization/how-to-write-object-data-to-an-xml-file.md)   
 [Sérialisation (C#)](../../../../csharp/programming-guide/concepts/serialization/index.md)   
 [Guide de programmation C#](../../../../csharp/programming-guide/index.md)
