---
title: "Comment : Count, Sum ou moyenne de données à l’aide de LINQ (Visual Basic) | Documents Microsoft"
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
- average operator [LINQ in Visual Basic]
- aggregate operator [LINQ in Visual Basic]
- aggregate queries
- queries [LINQ in Visual Basic], sum results
- Aggregate clause
- sum operator [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], aggregate queries
- queries [LINQ in Visual Basic], counting results
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
- count operator [LINQ in Visual Basic]
ms.assetid: 51ca1f59-7770-4884-8b76-113002e54fc0
caps.latest.revision: 9
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
ms.openlocfilehash: c5789d9e4bee1388d5ad0368f88fad5c1b6e95cc
ms.contentlocale: fr-fr
ms.lasthandoff: 03/13/2017

---
# <a name="how-to-count-sum-or-average-data-by-using-linq-visual-basic"></a>Comment : compter, additionner ou faire la moyenne de données à l'aide de LINQ (Visual Basic)
Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.  
  
 L’exemple suivant montre comment créer une nouvelle application qui effectue des requêtes sur une base de données SQL Server. L’exemple compte, additionne et calcule la moyenne de résultats à l’aide de la `Aggregate` et `Group By` clauses. Pour plus d’informations, consultez [Clause Aggregate](../../../../visual-basic/language-reference/queries/aggregate-clause.md) et [Group By Clause](../../../../visual-basic/language-reference/queries/group-by-clause.md).  
  
 Les exemples de cette rubrique utilisent la base de données Northwind. Si vous n’avez pas la base de données Northwind sur votre ordinateur de développement, vous pouvez le télécharger à partir de la [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkID=98088) site Web. Pour obtenir des instructions, consultez la page [téléchargement d’exemples de bases de données](https://msdn.microsoft.com/library/bb399411).  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a>Pour créer une connexion à une base de données  
  
1.  Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**Explorateur de base de données** sur la **affichage** menu.  
  
2.  Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** , puis **ajouter une connexion**.  
  
3.  Spécifiez une connexion valide à la base de données Northwind.  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a>Pour ajouter un projet contenant un fichier LINQ to SQL  
  
1.  Dans Visual Studio, sur le **fichier** menu, pointez sur **nouveau** , puis **projet**. Sélectionnez Visual Basic **Application Windows Forms** comme type de projet.  
  
2.  Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**. Sélectionnez le **Classes LINQ to SQL** modèle d’élément.  
  
3.  Nommez le fichier `northwind.dbml`. Cliquez sur **Ajouter**. Le Concepteur Objet/Relationnel (Concepteur O/R) est ouverte pour le fichier northwind.dbml.  
  
### <a name="to-add-tables-to-query-to-the-or-designer"></a>Pour ajouter des tables à interroger au Concepteur O/R  
  
1.  Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind. Développez le **Tables** dossier.  
  
     Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.  
  
2.  Cliquez sur la table Customers et faites-la glisser vers le volet gauche du concepteur. Cliquez sur la table Orders et faites-le glisser vers le volet gauche du concepteur.  
  
     Le concepteur crée de nouveaux `Customer` et `Order` objets de votre projet. Notez que le concepteur détecte les relations entre les tables automatiquement et crée des propriétés pour les objets enfants. Par exemple, IntelliSense indiquera que la `Customer` objet a un `Orders` propriété pour toutes les commandes associées à ce client.  
  
3.  Enregistrez vos modifications et fermez le concepteur.  
  
4.  Enregistrez votre projet.  
  
### <a name="to-add-code-to-query-the-database-and-display-the-results"></a>Pour ajouter du code pour interroger la base de données et afficher les résultats  
  
1.  À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView>contrôle sur le formulaire Windows par défaut pour votre projet, Form1.</xref:System.Windows.Forms.DataGridView>  
  
2.  Double-cliquez sur Form1 pour ajouter du code pour le `Load` événement du formulaire.  
  
3.  Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext>objet pour votre projet.</xref:System.Data.Linq.DataContext> Cet objet contient le code que vous devez disposer pour accéder à ces tables et pour accéder aux collections et objets individuels de chaque table. Le <xref:System.Data.Linq.DataContext>objet pour votre projet est nommé d’après le nom de votre fichier .dbml.</xref:System.Data.Linq.DataContext> Pour ce projet, le <xref:System.Data.Linq.DataContext>est nommé `northwindDataContext`.</xref:System.Data.Linq.DataContext>  
  
     Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext>dans votre code et interroger les tables spécifiées par le Concepteur O/R.</xref:System.Data.Linq.DataContext>  
  
     Ajoutez le code suivant à la `Load` événement pour interroger les tables qui sont exposées comme propriétés de votre <xref:System.Data.Linq.DataContext>et compter, additionner et la moyenne des résultats.</xref:System.Data.Linq.DataContext> L’exemple utilise le `Aggregate` clause pour interroger un résultat unique et la `Group By` clause pour afficher une moyenne pour les résultats groupés.  
  
     [!code-vb[VbLINQToSQLHowTos&#13;](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-count-sum-or-average-data-by-using-linq_1.vb)]  
  
4.  Appuyez sur F5 pour exécuter votre projet et afficher les résultats.  
  
## <a name="see-also"></a>Voir aussi  
 [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)   
 [Requêtes](../../../../visual-basic/language-reference/queries/queries.md)   
 [LINQ to SQL](https://msdn.microsoft.com/library/bb386976)   
 [Méthodes DataContext (Concepteur O/R)](https://docs.microsoft.com/visualstudio/data-tools/datacontext-methods-o-r-designer)  
 [Aggregate (Clause)](../../../../visual-basic/language-reference/queries/aggregate-clause.md)   
 [Group By (clause)](../../../../visual-basic/language-reference/queries/group-by-clause.md)

