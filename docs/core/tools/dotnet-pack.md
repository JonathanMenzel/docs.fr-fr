---
title: Commande dotnet-pack - CLI .NET Core | Microsoft Docs
description: "La commande dotnet-pack crée des packages NuGet pour votre projet .NET Core."
keywords: "dotnet-pack, CLI, commande CLI, .NET Core"
author: blackdwarf
ms.author: mairaw
ms.date: 03/15/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: 8dbbb3f7-b817-4161-a6c8-a3489d05e051
translationtype: Human Translation
ms.sourcegitcommit: dff752a9d31ec92b113dae9eed20cd72faf57c84
ms.openlocfilehash: 6bb8d618cc092131bd6a904fb66f02c4f3a9ecca
ms.lasthandoff: 03/22/2017

---

# <a name="dotnet-pack"></a>dotnet-pack

## <a name="name"></a>Nom

`dotnet-pack` : Place le code dans un package NuGet.

## <a name="synopsis"></a>Résumé

`dotnet pack [<PROJECT>] [-o|--output] [--no-build] [--include-symbols] [--include-source] [-c|--configuration] [--version-suffix <VERSION_SUFFIX>] [-s|--serviceable] [-v|--verbosity] [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet pack` génère le projet et crée les packages NuGet. Le résultat de cette commande est un package NuGet. Si l’option `--include-symbols` est présente, un autre package contenant les symboles de débogage est créé. 

Les dépendances NuGet du projet empaqueté sont ajoutées dans le fichier *.nuspec*, pour pouvoir être correctement résolues lors de l’installation du package. Les références entre projets ne sont pas empaquetées à l’intérieur du projet. Actuellement, vous devez disposer d’un package par projet si vous avez des dépendances entre projets.

Par défaut, `dotnet pack` génère d’abord le projet. Pour éviter ce comportement, passez l’option `--no-build`. Elle est souvent utile dans les scénarios de build d’intégration continue, pour lesquels vous savez que le code a déjà été créé. 

## <a name="arguments"></a>Arguments

`PROJECT` 
    
Projet à empaqueter. Il s’agit du chemin d’accès d’un [fichier csproj](csproj.md) ou d’un répertoire. Si aucune valeur n’est spécifiée, le répertoire actif est utilisé par défaut. 

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.  

`-o|--output <OUTPUT_DIRECTORY>`

Place les packages générés dans le répertoire spécifié. 

`--no-build`

Ne génère pas le projet avant de créer le package. 

`--include-symbols`

Génère les symboles `nupkg`. 

`--include-source`

Inclut les fichiers sources dans le package NuGet. Les fichiers sources sont inclus dans le dossier `src` de `nupkg`. 

`-c|--configuration <CONFIGURATION>`

Configuration à utiliser lors de la génération du projet. Si elle n’est pas spécifiée, la configuration par défaut est `Debug`.

`--version-suffix <VERSION_SUFFIX>`

Définit la valeur de la propriété MSBuild `$(VersionSuffix)` dans le projet.

`-s|--serviceable`

Définit l’indicateur d’un état pouvant faire l’objet d’une maintenance dans le package. Pour plus d’informations, consultez [Blog .NET : .NET 4.5.1 prend en charge les mises à jour de sécurité de Microsoft pour les bibliothèques NuGet .NET](https://aka.ms/nupkgservicing).

`--verbosity <LEVEL>`

Définit le niveau de détail de la commande. Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.

## <a name="examples"></a>Exemples

Empaquetez le projet dans le répertoire actif :

`dotnet pack`

Empaqueter le projet `app1` :

`dotnet pack ~/projects/app1/project.csproj`
    
Empaqueter le projet dans le répertoire actif et placer les packages résultants dans le dossier `nupkgs` :

`dotnet pack --output nupkgs`

Empaqueter le projet dans le répertoire actif du dossier `nupkgs` et ignorer l’étape de génération :

`dotnet pack --no-build --output nupkgs`

Avec le suffixe de version du projet configuré comme `<VersionSuffix>$(VersionSuffix)</VersionSuffix>` dans le fichier *.csproj*, empaqueter le projet actif et mettre à jour la version du package obtenue avec le suffixe donné :

`dotnet pack --version-suffix "ci-1234"`
