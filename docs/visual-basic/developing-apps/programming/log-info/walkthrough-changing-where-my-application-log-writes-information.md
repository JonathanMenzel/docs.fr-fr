---
title: "Proc&#233;dure pas &#224; pas&#160;: modification de l&#39;emplacement des informations My.Application.Log (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Application.Log (objet), procédures pas à pas"
  - "journaux des événements, modifier l’emplacement de sortie"
ms.assetid: ecc74f95-743c-450d-93f6-09a30db0fe4a
caps.latest.revision: 20
author: "stevehoag"
ms.author: "shoag"
caps.handback.revision: 20
---
# Proc&#233;dure pas &#224; pas&#160;: modification de l&#39;emplacement des informations My.Application.Log (Visual Basic)
[!INCLUDE[vs2017banner](../../../../visual-basic/includes/vs2017banner.md)]

Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur les événements qui se produisent dans votre application. Cette procédure pas à pas montre comment remplacer les paramètres par défaut et faire en sorte que l’objet `Log` écrive dans d’autres écouteurs de journalisation.  
  
## Composants requis  
 L’objet `Log` peut écrire des informations dans plusieurs écouteurs de journalisation. Vous devez déterminer la configuration actuelle des écouteurs de journalisation avant de modifier les configurations. Pour plus d'informations, consultez [Procédure pas à pas : détermination de l'emplacement des informations My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md).  
  
 Vous pouvez consulter [How to: Write Event Information to a Text File](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-event-information-to-a-text-file.md) ou [Comment : écrire dans le journal des événements de l'application](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-to-an-application-event-log.md).  
  
### Pour ajouter des écouteurs  
  
1.  Cliquez avec le bouton droit sur app.config dans l’**Explorateur de solutions** et choisissez **Ouvrir**.  
  
     ou  
  
     S’il n’existe pas de fichier app.config :  
  
    1.  Dans le menu **Projet**, choisissez **Ajouter un nouvel élément**.  
  
    2.  Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Fichier de configuration de l’application**.  
  
    3.  Cliquez sur **Ajouter**.  
  
2.  Recherchez la section `<listeners>`, sous la section `<source>` avec l’attribut `name` « DefaultSource » dans la section `<sources>`. La section `<sources>` se trouve dans la section `<system.diagnostics>`, dans la section `<configuration>` de plus haut niveau.  
  
3.  Ajoutez ces éléments à cette section `<listeners>`.  
  
    ```  
    <!-- Uncomment to connect the application file log. -->  
    <!-- <add name="FileLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="EventLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="Delimited" /> -->  
    <!-- Uncomment to connect the XML log. -->  
    <!-- <add name="XmlWriter" /> -->  
    <!-- Uncomment to connect the console log. -->  
    <!-- <add name="Console" /> -->  
    ```  
  
4.  Supprimez les marques de commentaire pour les écouteurs de journalisation qui doivent recevoir les messages `Log`.  
  
5.  Recherchez la section `<sharedListeners>` dans la section `<system.diagnostics>`, dans la section `<configuration>` de plus haut niveau.  
  
6.  Ajoutez ces éléments à cette section `<sharedListeners>`.  
  
    ```  
    <add name="FileLog"  
         type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
               Microsoft.VisualBasic, Version=8.0.0.0,   
               Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
         initializeData="FileLogWriter" />  
    <add name="EventLog"  
         type="System.Diagnostics.EventLogTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="sample application"/>  
    <add name="Delimited"   
         type="System.Diagnostics.DelimitedListTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleDelimitedFile.txt"  
         traceOutputOptions="DateTime" />  
    <add name="XmlWriter"  
         type="System.Diagnostics.XmlWriterTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleLogFile.xml" />  
    <add name="Console"  
         type="System.Diagnostics.ConsoleTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="true" />  
    ```  
  
7.  Le contenu du fichier app.config doit être similaire au code XML suivant :  
  
    ```  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <system.diagnostics>  
        <sources>  
          <!-- This section configures My.Application.Log -->  
          <source name="DefaultSource" switchName="DefaultSwitch">  
            <listeners>  
              <add name="FileLog"/>  
              <!-- Uncomment to connect the application file log. -->  
              <!-- <add name="FileLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="EventLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="Delimited" /> -->  
              <!-- Uncomment to connect the XML log. -->  
              <!-- <add name="XmlWriter" /> -->  
              <!-- Uncomment to connect the console log. -->  
              <!-- <add name="Console" /> -->  
            </listeners>  
          </source>  
        </sources>  
        <switches>  
          <add name="DefaultSwitch" value="Information" />  
        </switches>  
        <sharedListeners>  
          <add name="FileLog"  
               type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
                     Microsoft.VisualBasic, Version=8.0.0.0,   
                     Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
               initializeData="FileLogWriter" />  
          <add name="EventLog"  
               type="System.Diagnostics.EventLogTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="sample application"/>  
          <add name="Delimited"   
               type="System.Diagnostics.DelimitedListTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleDelimitedFile.txt"  
               traceOutputOptions="DateTime" />  
          <add name="XmlWriter"  
               type="System.Diagnostics.XmlWriterTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleLogFile.xml" />  
          <add name="Console"  
               type="System.Diagnostics.ConsoleTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="true" />  
        </sharedListeners>  
      </system.diagnostics>  
    </configuration>  
    ```  
  
### Pour reconfigurer un écouteur  
  
1.  Recherchez l’élément `<add>` de l’écouteur dans la section `<sharedListeners>`.  
  
2.  L’attribut `type` donne le nom du type d’écouteur. Ce type doit être hérité de la classe <xref:System.Diagnostics.TraceListener>. Utilisez le nom de type avec un nom fort pour être sûr que le type correct est utilisé. Pour plus d’informations, consultez la section « Pour référencer un type avec un nom fort » ci\-dessous.  
  
     Voici quelques\-uns des types que vous pouvez utiliser :  
  
    -   Un écouteur <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?displayProperty=fullName>, qui écrit dans un fichier journal.  
  
    -   Un écouteur <xref:System.Diagnostics.EventLogTraceListener?displayProperty=fullName>, qui écrit les informations dans le journal des événements de l’ordinateur spécifié par le paramètre `initializeData`.  
  
    -   Les écouteurs <xref:System.Diagnostics.DelimitedListTraceListener?displayProperty=fullName> et <xref:System.Diagnostics.XmlWriterTraceListener?displayProperty=fullName>, qui écrivent dans le fichier spécifié par le paramètre `initializeData`.  
  
    -   Un écouteur <xref:System.Diagnostics.ConsoleTraceListener?displayProperty=fullName>, qui écrit dans la console de ligne de commande.  
  
     Pour plus d’informations sur les emplacements où d’autres types d’écouteurs de journalisation écrivent les informations, consultez la documentation de ce type.  
  
3.  Quand l’application crée l’objet d’écouteur de journalisation, il passe l’attribut `initializeData` comme paramètre de constructeur. La signification de l’attribut `initializeData` dépend de l’écouteur de suivi.  
  
4.  Après avoir créé l’écouteur de journalisation, l’application définit les propriétés de l’écouteur. Ces propriétés sont définies par les autres attributs dans l’élément `<add>`. Pour plus d’informations sur les propriétés d’un écouteur particulier, consultez la documentation de ce type d’écouteur.  
  
### Pour référencer un type avec un nom fort  
  
1.  Pour être sûr que type correct est utilisé pour votre écouteur de journalisation, vérifiez que vous utilisez le nom de type qualifié complet et le nom d’assembly avec nom fort. La syntaxe d’un type avec nom fort est la suivante :  
  
     \<*nom de type*\>, \<*nom d’assembly*\>, \<*numéro de version*\>, \<*culture*\>, \<*nom fort*\>  
  
2.  Cet exemple de code montre comment déterminer le nom de type avec nom fort pour un type qualifié complet, dans ce cas « System.Diagnostics.FileLogTraceListener ».  
  
     [!code-vb[VbVbalrMyApplicationLog#15](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/visualbasic/VbVbalrMyApplicationLog/Form1.vb#15)]  
  
     Voici la sortie. Il peut être utilisé pour faire référence de façon univoque à un type avec nom fort, comme dans la procédure « Pour ajouter des écouteurs » ci\-dessus.  
  
     `Microsoft.VisualBasic.Logging.FileLogTraceListener, Microsoft.VisualBasic, Version=8.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a`  
  
## Voir aussi  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:System.Diagnostics.TraceListener>   
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?displayProperty=fullName>   
 <xref:System.Diagnostics.EventLogTraceListener?displayProperty=fullName>   
 [How to: Write Event Information to a Text File](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-event-information-to-a-text-file.md)   
 [Comment : écrire dans le journal des événements de l'application](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-to-an-application-event-log.md)