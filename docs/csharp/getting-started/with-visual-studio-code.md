---
title: "Bien démarrer avec Visual Studio Code | Guide C#"
description: "Découvrez comment créer et déboguer votre première application .NET Core en C# à l’aide de Visual Studio Code."
keywords: C#, bien commencer, acquisition, installer, Visual Studio Code, multiplateforme
author: kendrahavens
ms.author: mairaw
ms.date: 03/07/2017
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: 76c23597-4cf9-467e-8a47-0c3703ce37e7
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 4550129f4e6f1eeb3521ad7fe3233f2bda49e5c5
ms.lasthandoff: 03/13/2017

---

# <a name="getting-started-with-visual-studio-code"></a>Bien démarrer avec Visual Studio Code

.NET Core vous offre une plateforme rapide et évolutive pour la création d’applications serveur qui s’exécutent sur Windows, Linux et Mac OS. Utilisez Visual Studio Code avec l’extension de langage C# pour une expérience d’édition puissante avec prise en charge complète de C# IntelliSense (saisie semi-automatique intelligente de code).

## <a name="prerequisites"></a>Conditions préalables

1. Installez [Visual Studio Code](https://code.visualstudio.com/).
2. Installez le [SDK .NET Core](https://www.microsoft.com/net/download/core).
3. Installez [l’extension C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp) à partir de la Place de marché Visual Studio.

## <a name="hello-world"></a>Hello World

Commençons par un programme « Hello World » simple sur .NET Core :

1. Ouvrez un projet :

    * Ouvrez VS Code.
    * Cliquez sur l’icône Explorer dans le menu de gauche, puis sur **Ouvrir le dossier**.
    * Sélectionnez le dossier dans lequel vous souhaitez que votre projet C# se trouve et cliquez sur **Sélectionner le dossier**. Dans notre exemple, nous allons créer un dossier pour notre projet nommé « HelloWorld ». 

  ![VSCodeOpenFolder](media/with-visual-studio-code/vscodeopenfolder.png)

    * Vous pouvez également sélectionner **Fichier** > **Ouvrir le dossier** dans le menu principal pour ouvrir le dossier de votre projet.

2. Initialiser un projet C# :
    * Ouvrez le terminal intégré à partir de Visual Studio Code en tapant sur <kbd>CTRL</kbd>+<kbd>\`</kbd> (accent grave).
    * Dans la fenêtre de Terminal, tapez `dotnet new console`.
    * Cela crée un fichier `Program.cs` dans votre dossier avec un programme simple « Hello World » déjà écrit, ainsi qu’un fichier de projet C# nommé `HelloWorld.csproj`.

  ![La nouvelle commande dotnet](media/with-visual-studio-code/dotnetnew.png)

3. Résolution des ressources de génération :

    * Tapez `dotnet restore`. Exécuter `dotnet restore` vous donne accès aux packages .NET Core qui sont nécessaires pour générer votre projet.

  ![La commande dotnet restore](media/with-visual-studio-code/dotnetrestore.png)

4. Exécutez le programme Hello World :

    * Tapez `dotnet run`. 

  ![La commande dotnet run](media/with-visual-studio-code/dotnetrun.png)

Vous pouvez également regarder un court didacticiel vidéo pour plus d’informations sur la configuration sur [Windows](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core), [macOS](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core-on-MacOS) ou [Linux](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-Csharp-dotnet-Core-Ubuntu).

## <a name="debug"></a>Débogage
1. Ouvrez *Program.cs* en cliquant dessus. La première fois que vous ouvrez un fichier C# dans VS Code, [OmniSharp](http://www.omnisharp.net/) se charge dans l’éditeur.

  ![Ouvrez le fichier Program.cs](media/with-visual-studio-code/opencs.png)

2. VS Code vous invite à ajouter les actifs manquants pour générer et déboguer votre application. Sélectionnez **Oui**. 

  ![Invite pour les fichiers manquants](media/with-visual-studio-code/missing-assets.png)

3. Pour ouvrir la vue de débogage, cliquez sur l’icône de débogage dans le menu de gauche.

  ![Ouvrez l'onglet Déboguer](media/with-visual-studio-code/opendebug.png)

4. Cherchez la flèche verte en haut du volet. Assurez-vous que `.NET Core Launch (console)` est sélectionné dans la liste déroulante à côté du volet.

  ![Sélection de .NET Core](media/with-visual-studio-code/selectcore.png)

5. Ajoutez un point d’arrêt à votre projet en cliquant sur la **Marge de l’éditeur** (l’espace à gauche des numéros de ligne dans l’éditeur) à côté de la ligne 9.

  ![Définition d'un point d'arrêt](media/with-visual-studio-code/setbreakpoint.png)

6. Sélectionnez <kbd>F5</kbd> ou sur la flèche verte pour démarrer le débogage. Le débogueur arrête l’exécution de votre programme lorsqu’il atteint le point d’arrêt que vous avez défini à l’étape précédente.
    * Pendant le débogage, vous pouvez afficher vos variables locales dans le volet supérieur gauche ou utiliser la console de débogage.

  ![Exécuter et déboguer](media/with-visual-studio-code/rundebug.png)

7. Cliquez sur la flèche verte en haut pour continuer le débogage, ou appuyez sur le carré rouge pour arrêter.

> [!TIP] 
> Pour plus d’informations et de conseils sur le débogage de .NET Core avec OmniSharp dans VS Code, consultez les [Instructions de configuration du débogueur .NET Core](https://github.com/OmniSharp/omnisharp-vscode/blob/master/debugger.md).

## <a name="see-also"></a>Voir aussi
- [Configuration de Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview)
- [Débogage dans Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging)

