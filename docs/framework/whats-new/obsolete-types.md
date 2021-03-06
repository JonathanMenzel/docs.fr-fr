---
title: "Types obsolètes dans le .NET Framework | Microsoft Docs"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- .NET Framework 4.5, obsolete types
- types, obsolete in .NET Framework 4.5
- obsolete types [.NET Framework]
ms.assetid: e636d024-0fac-45eb-b721-25a8c0ceca8f
caps.latest.revision: 41
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Human Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 175e46e3729190423b85296d7c7c47b136339305
ms.contentlocale: fr-fr
ms.lasthandoff: 04/18/2017

---
# <a name="obsolete-types-in-the-net-framework"></a>Types obsolètes dans le .NET Framework
<a name="introduction"></a> Les tableaux de cet article, organisés par assembly, répertorient les types qui sont obsolètes dans le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] et le [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]. Utilisez les liens suivants pour consulter la liste des types obsolètes et des alternatives recommandées dans chaque assembly. Ces types étant obsolètes, tous leurs membres le sont également. Pour obtenir la liste des membres obsolètes supplémentaires dans la bibliothèque de classes .NET Framework, consultez [Membres obsolètes](../../../docs/framework/whats-new/obsolete-members.md).  
  
-   [Types obsolètes dans les assemblys système](#obsolete_types_in_system_assemblies)  
  
    -   [mscorlib.dll](#mscorlib)  
  
    -   [System.Core.dll](#Core)  
  
    -   [System.Data.dll](#data)  
  
    -   [System.Data.OracleClient.dll](#oracleclient)  
  
    -   [System.Design.dll](#design)  
  
    -   [System.dll](#system)  
  
    -   [System.EnterpriseServices.dll](#enterpriseservices)  
  
    -   [System.Net.dll](#net)  
  
    -   [System.ServiceModel.dll](#servicemodel)  
  
    -   [System.Web.dll](#web)  
  
    -   [System.Web.Mobile.dll](#mobile)  
  
    -   [System.Workflow.Activities.dll](#workflow_activities)  
  
    -   [System.Workflow.ComponentModel.dll](#workflow_componentmodel)  
  
    -   [System.Workflow.Runtime.dll](#workflow_runtime)  
  
    -   [System.WorkflowServices.dll](#workflowservices)  
  
    -   [System.Xaml.dll](#xaml)  
  
    -   [System.Xml.dll](#xml)  
  
    -   [WindowsBase.dll](#WindowsBase)  
  
-   [Types obsolètes dans les assemblys Microsoft](#obsolete_types_in_microsoft_assemblies)  
  
    -   [IEHost.dll et IEExec.exe](#IEHost)  
  
    -   [Microsoft.Build.Engine.dll](#Engine)  
  
    -   [Microsoft.JScript.dll](#jscript)  
  
    -   [Microsoft.VisualBasic.Compatibility.dll](#VBCompat)  
  
    -   [Microsoft.VisualBasic.Compatibility.Data.dll](#VBCompatData)  
  
    -   [Microsoft.VisualC.dll](#visualc)  
  
<a name="obsolete_types_in_system_assemblies"></a>   
## <a name="obsolete-types-in-system-assemblies"></a>Types obsolètes dans les assemblys système  
 Les tableaux suivants répertorient les types qui ont été déclarés obsolètes dans les assemblys système. Ces assemblys sont utilisés pour le développement d’applications à usage général qui ciblent le .NET Framework.  
  
<a name="mscorlib"></a>   
### <a name="assembly-mscorlibdll"></a>Assembly : mscorlib.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.ExecutionEngineException?displayProperty=fullName>|Ce type indiquait une erreur irrécupérable non spécifiée dans l'exécution. Étant donné que l'exécution ne déclenche plus cette exception, ce type est devenu obsolète.|  
|<xref:System.Collections.CaseInsensitiveHashCodeProvider?displayProperty=fullName>|Utilisez <xref:System.StringComparer?displayProperty=fullName> à la place.|  
|<xref:System.Collections.IHashCodeProvider?displayProperty=fullName>|Utilisez <xref:System.Collections.IEqualityComparer?displayProperty=fullName> à la place.|  
|<xref:System.Configuration.Assemblies.AssemblyHash?displayProperty=fullName>|La classe <xref:System.Configuration.Assemblies.AssemblyHash> est dépréciée.|  
|<xref:System.Diagnostics.Contracts.Internal.ContractHelper?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5. Utilisez plutôt la classe <xref:System.Runtime.CompilerServices.ContractHelper?displayProperty=fullName> dans l’espace de noms System.Runtime.CompilerServices.|  
|<xref:System.Reflection.Emit.UnmanagedMarshal?displayProperty=fullName>|Une autre API est disponible : émettez l’attribut personnalisé <xref:System.Runtime.InteropServices.MarshalAsAttribute?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.BIND_OPTS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.BIND_OPTS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.BINDPTR?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.BINDPTR?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.CALLCONV?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.CALLCONV?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.CONNECTDATA?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.CONNECTDATA?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.DESCKIND?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.DESCKIND?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.DISPPARAMS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.DISPPARAMS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.ELEMDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.ELEMDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.EXCEPINFO?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.EXCEPINFO?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.FILETIME?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.FILETIME?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.FUNCDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.FUNCDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.FUNCFLAGS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.FUNCFLAGS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.FUNCKIND?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.FUNCKIND?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.IDispatchImplAttribute?displayProperty=fullName>|Cet attribut est déprécié et sera supprimé dans une version ultérieure.|  
|<xref:System.Runtime.InteropServices.IDispatchImplType?displayProperty=fullName>|<xref:System.Runtime.InteropServices.IDispatchImplAttribute?displayProperty=fullName> est déprécié.|  
|<xref:System.Runtime.InteropServices.IDLDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IDLDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.IDLFLAG?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IDLFLAG?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.IMPLTYPEFLAGS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IMPLTYPEFLAGS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.INVOKEKIND?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.INVOKEKIND?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.LIBFLAGS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.LIBFLAGS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.PARAMDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.PARAMDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.PARAMFLAG?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.PARAMFLAG?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.SetWin32ContextInIDispatchAttribute?displayProperty=fullName>|Cet attribut est déprécié. Les domaines d'application ne respectent plus les limites de contexte d'activation dans les appels IDispatch.|  
|<xref:System.Runtime.InteropServices.STATSTG?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.STATSTG?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.SYSKIND?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.SYSKIND?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.TYPEATTR?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.TYPEATTR?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.TYPEDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.TYPEDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.TYPEFLAGS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.TYPEFLAGS?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.TYPEKIND?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.TYPEKIND?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.TYPELIBATTR?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.TYPELIBATTR?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIBindCtx?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IBindCtx?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIConnectionPoint?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIConnectionPointContainer?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIEnumConnectionPoints?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IEnumConnectionPoints?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIEnumConnections?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IEnumConnections?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIEnumMoniker?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IEnumMoniker?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIEnumString?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IEnumString?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIEnumVARIANT?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IEnumVARIANT?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIMoniker?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IMoniker?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIPersistFile?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IPersistFile?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIRunningObjectTable?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IRunningObjectTable?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMIStream?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.IStream?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMITypeComp?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.ITypeComp?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMITypeInfo?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.ITypeInfo?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.UCOMITypeLib?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.ITypeLib?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.VARDESC?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.VARDESC?displayProperty=fullName> à la place.|  
|<xref:System.Runtime.InteropServices.VARFLAGS?displayProperty=fullName>|Utilisez <xref:System.Runtime.InteropServices.ComTypes.VARFLAGS?displayProperty=fullName> à la place.|  
|<xref:System.Security.SecurityCriticalScope?displayProperty=fullName>|<xref:System.Security.SecurityCriticalScope> est utilisé uniquement pour la compatibilité de transparence du .NET 2.0.|  
|<xref:System.Security.SecurityTreatAsSafeAttribute?displayProperty=fullName>|<xref:System.Security.SecurityTreatAsSafeAttribute> est utilisé uniquement pour la compatibilité de transparence du .NET 2.0. Utilisez <xref:System.Security.SecuritySafeCriticalAttribute?displayProperty=fullName> à la place.|  
|<xref:System.Security.Policy.FirstMatchCodeGroup?displayProperty=fullName>|Ce type est obsolète et sera supprimé dans une prochaine version du .NET Framework.|  
|<xref:System.Security.Policy.PermissionRequestEvidence?displayProperty=fullName>|La sécurité déclarative au niveau de l'assembly est obsolète et n'est plus appliquée par le CLR par défaut.|  
|<xref:System.Security.Policy.UnionCodeGroup?displayProperty=fullName>|Ce type est obsolète et sera supprimé dans une prochaine version du .NET Framework.|  
  
 [Retour au début](#introduction)  
  
<a name="Core"></a>   
### <a name="assembly-systemcoredll"></a>Assembly : System.Core.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Runtime.CompilerServices.ExecutionScope?displayProperty=fullName>|L'utilisation de ce type génère une erreur du compilateur.<br /><br /> N'utilisez pas ce type.|  
  
 [Retour au début](#introduction)  
  
<a name="data"></a>   
### <a name="assembly-systemdatadll"></a>Assembly : System.Data.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Data.DataSysDescriptionAttribute?displayProperty=fullName>|<xref:System.Data.DataSysDescriptionAttribute> est déprécié.|  
|<xref:System.Data.PropertyAttributes?displayProperty=fullName>|<xref:System.Data.PropertyAttributes> est déprécié.|  
|<xref:System.Data.TypedDataSetGenerator?displayProperty=fullName>|La classe <xref:System.Data.TypedDataSetGenerator> sera supprimée dans une version ultérieure. Utilisez <xref:System.Data.Design.TypedDataSetGenerator?displayProperty=fullName> dans System.Design.dll.|  
|<xref:System.Xml.XmlDataDocument?displayProperty=fullName>|La classe <xref:System.Xml.XmlDataDocument> sera supprimée dans une version ultérieure.|  
  
 [Retour au début](#introduction)  
  
<a name="oracleclient"></a>   
### <a name="assembly-systemdataoracleclientdll"></a>Assembly : System.Data.OracleClient.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Data.OracleClient.OracleClientFactory?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleClientFactory> est déprécié.|  
|<xref:System.Data.OracleClient.OracleCommand?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleCommand> est déprécié.|  
|<xref:System.Data.OracleClient.OracleCommandBuilder?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleCommandBuilder> est déprécié.|  
|<xref:System.Data.OracleClient.OracleConnection?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleConnection> est déprécié.|  
|<xref:System.Data.OracleClient.OracleConnectionStringBuilder?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleConnectionStringBuilder> est déprécié.|  
|<xref:System.Data.OracleClient.OracleDataAdapter?displayProperty=fullName>|<xref:System.Data.OracleClient.OracleDataAdapter> est déprécié.|  
|<xref:System.Data.OracleClient.OraclePermission?displayProperty=fullName>|<xref:System.Data.OracleClient.OraclePermission> est déprécié.|  
|<xref:System.Data.OracleClient.OraclePermissionAttribute?displayProperty=fullName>|<xref:System.Data.OracleClient.OraclePermissionAttribute?displayProperty=fullName> est déprécié.|  
  
 [Retour au début](#introduction)  
  
<a name="design"></a>   
### <a name="assembly-systemdesigndll"></a>Assembly : System.Design.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.ComponentModel.Design.LocalizationExtenderProvider?displayProperty=fullName>|Cette classe est dépréciée. Utilisez <xref:System.ComponentModel.Design.Serialization.CodeDomLocalizationProvider?displayProperty=fullName> à la place.|  
|<xref:System.Web.UI.Design.DataBindingCollectionConverter?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification DataBindings est lancée par l’intermédiaire d’un <xref:System.ComponentModel.Design.DesignerActionList?displayProperty=fullName> au lieu de la grille des propriétés.|  
|<xref:System.Web.UI.Design.DataBindingCollectionEditor?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification DataBindings est lancée par l’intermédiaire d’un <xref:System.ComponentModel.Design.DesignerActionList?displayProperty=fullName> au lieu de la grille des propriétés.|  
|<xref:System.Web.UI.Design.IControlDesignerBehavior?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.IControlDesignerTag?displayProperty=fullName> et <xref:System.Web.UI.Design.IControlDesignerView?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.IHtmlControlDesignerBehavior?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.IControlDesignerTag?displayProperty=fullName> et <xref:System.Web.UI.Design.IControlDesignerView?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.ITemplateEditingFrame?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification de modèle est gérée dans <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>. Pour prendre en charge la modification de modèle, exposez les données de modèle dans la propriété <xref:System.Web.UI.Design.ControlDesigner.TemplateGroups%2A?displayProperty=fullName> et appelez <xref:System.Web.UI.Design.ControlDesigner.SetViewFlags%2A?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.IWebFormReferenceManager?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.WebFormsReferenceManager?displayProperty=fullName>. <xref:System.Web.UI.Design.WebFormsReferenceManager> contient des fonctionnalités supplémentaires et autorise une meilleure extensibilité. Pour obtenir <xref:System.Web.UI.Design.WebFormsReferenceManager>, utilisez la propriété `RootDesigner.ReferenceManager` à partir de votre <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.IWebFormsDocumentService?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.WebFormsRootDesigner?displayProperty=fullName>. <xref:System.Web.UI.Design.WebFormsRootDesigner> contient des fonctionnalités supplémentaires et autorise une meilleure extensibilité. Pour obtenir <xref:System.Web.UI.Design.WebFormsRootDesigner>, utilisez la propriété <xref:System.Web.UI.Design.ControlDesigner.RootDesigner%2A> à partir de votre <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.ITemplateEditingService?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification de modèle est gérée dans <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>. Pour prendre en charge la modification de modèle, exposez les données de modèle dans la propriété <xref:System.Web.UI.Design.ControlDesigner.TemplateGroups%2A?displayProperty=fullName> et appelez <xref:System.Web.UI.Design.ControlDesigner.SetViewFlags%2A?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.ReadWriteControlDesigner?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.ContainerControlDesigner?displayProperty=fullName>, car elle utilise un <xref:System.Web.UI.Design.EditableDesignerRegion?displayProperty=fullName> pour la modification du contenu. Les zones du concepteur permettent de mieux contrôler le contenu qui est modifié.|  
|<xref:System.Web.UI.Design.TemplateEditingService?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification de modèle est gérée dans <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>. Pour prendre en charge la modification de modèle, exposez les données de modèle dans la propriété <xref:System.Web.UI.Design.ControlDesigner.TemplateGroups%2A?displayProperty=fullName> et appelez <xref:System.Web.UI.Design.ControlDesigner.SetViewFlags%2A?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.TemplateEditingVerb?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car la modification de modèle est gérée dans <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName>. Pour prendre en charge la modification de modèle, exposez les données de modèle dans la propriété <xref:System.Web.UI.Design.ControlDesigner.TemplateGroups%2A?displayProperty=fullName> et appelez <xref:System.Web.UI.Design.ControlDesigner.SetViewFlags%2A?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.WebControls.CalendarAutoFormatDialog?displayProperty=fullName>|L'utilisation de ce type n'est pas recommandée étant donné que la boîte de dialogue Mise en forme automatique est lancée par l'hôte concepteur. La liste des mises en forme automatiques disponibles est exposée sur <xref:System.Web.UI.Design.ControlDesigner?displayProperty=fullName> dans la propriété <xref:System.Web.UI.Design.ControlDesigner.AutoFormats%2A?displayProperty=fullName>.|  
|<xref:System.Web.UI.Design.WebControls.PanelDesigner?displayProperty=fullName>|L’alternative recommandée est <xref:System.Web.UI.Design.WebControls.PanelContainerDesigner?displayProperty=fullName>, car elle utilise un <xref:System.Web.UI.Design.EditableDesignerRegion?displayProperty=fullName> pour la modification du contenu. Les zones du concepteur permettent de mieux contrôler le contenu qui est modifié.|  
  
 [Retour au début](#introduction)  
  
<a name="system"></a>   
### <a name="assembly-systemdll"></a>Assembly : System.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.ComponentModel.IComNativeDescriptorHandler?displayProperty=fullName>|Cette interface est dépréciée. Ajoutez plutôt un <xref:System.ComponentModel.TypeDescriptionProvider?displayProperty=fullName> pour gérer le type <xref:System.ComponentModel.TypeDescriptor.ComObjectType%2A?displayProperty=fullName>.|  
|<xref:System.ComponentModel.RecommendedAsConfigurableAttribute?displayProperty=fullName>|Utilisez plutôt <xref:System.ComponentModel.SettingsBindableAttribute?displayProperty=fullName> pour travailler avec le nouveau modèle de paramètres.|  
|<xref:System.ComponentModel.Design.Serialization.RootDesignerSerializerAttribute?displayProperty=fullName>|Cet attribut est déprécié. Utilisez <xref:System.ComponentModel.Design.Serialization.DesignerSerializerAttribute?displayProperty=fullName> à la place. Par exemple, si vous voulez spécifier un concepteur racine pour CodeDom, utilisez `DesignerSerializerAttribute\(...,typeof\(TypeCodeDomSerializer\)\)`.|  
|<xref:System.Diagnostics.DiagnosticsConfigurationHandler?displayProperty=fullName>|Cette classe est dépréciée.|  
|<xref:System.Diagnostics.PerformanceCounterManager?displayProperty=fullName>|Cette classe est dépréciée. Utilisez plutôt les compteurs de performance par l’intermédiaire de la classe <xref:System.Diagnostics.PerformanceCounter?displayProperty=fullName>.|  
|<xref:System.Net.GlobalProxySelection?displayProperty=fullName>|Cette classe est dépréciée. Utilisez plutôt <xref:System.Net.WebRequest.DefaultWebProxy%2A?displayProperty=fullName> pour accéder au proxy global par défaut et le définir. Utilisez « null » au lieu de <xref:System.Net.GlobalProxySelection.GetEmptyWebProxy%2A?displayProperty=fullName>.|  
|<xref:System.Net.Sockets.SocketClientAccessPolicyProtocol?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
  
 [Retour au début](#introduction)  
  
<a name="enterpriseservices"></a>   
### <a name="assembly-systementerpriseservicesdll"></a>Assembly : System.EnterpriseServices.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.EnterpriseServices.RegistrationHelperTx?displayProperty=fullName>|La classe <xref:System.EnterpriseServices.RegistrationHelperTx>classe est dépréciée.|  
  
 [Retour au début](#introduction)  
  
<a name="net"></a>   
### <a name="assembly-systemnetdll"></a>Assembly : System.Net.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Net.INetworkProgress?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.IUnsafeWebRequestCreate?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.NetworkProgressChangedEventArgs?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.UiSynchronizationContext?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.Sockets.HttpPolicyDownloaderProtocol?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.Sockets.SecurityCriticalAction?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.Sockets.SocketPolicy?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.Sockets.UdpAnySourceMulticastClient?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Net.Sockets.UdpSingleSourceMulticastClient?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
  
 [Retour au début](#introduction)  
  
<a name="servicemodel"></a>   
### <a name="assembly-systemservicemodeldll"></a>Assembly : System.ServiceModel.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.ServiceModel.NetPeerTcpBinding?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.Channels.HttpCookieContainerBindingElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Ce type est obsolète. Pour activer HTTP <xref:System.Net.CookieContainer>, utilisez la propriété `AllowCookies` sur la liaison HTTP ou sur <xref:System.ServiceModel.Channels.HttpTransportBindingElement>.|  
|<xref:System.ServiceModel.Channels.PeerCustomResolverBindingElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.Channels.PeerTransportBindingElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.Configuration.NetPeerTcpBindingCollectionElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.Configuration.PeerTransportElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
|<xref:System.ServiceModel.PeerResolvers.CustomPeerResolverService?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> La fonctionnalité de canal pair est obsolète et sera supprimée dans le futur.|  
  
 [Retour au début](#introduction)  
  
<a name="web"></a>   
### <a name="assembly-systemwebdll"></a>Assembly : System.Web.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Web.Configuration.PassportAuthentication?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.Mail.MailAttachment?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mail.Attachment?displayProperty=fullName>.|  
|<xref:System.Web.Mail.MailEncoding?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mime.TransferEncoding?displayProperty=fullName>.|  
|<xref:System.Web.Mail.MailFormat?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mail.MailMessage.IsBodyHtml%2A?displayProperty=fullName>.|  
|<xref:System.Web.Mail.MailMessage?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mail.MailMessage?displayProperty=fullName>.|  
|<xref:System.Web.Mail.MailPriority?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mail.MailPriority?displayProperty=fullName>.|  
|<xref:System.Web.Mail.SmtpMail?displayProperty=fullName>|L’alternative recommandée est <xref:System.Net.Mail.SmtpClient?displayProperty=fullName>.|  
|<xref:System.Web.Security.PassportAuthenticationEventArgs?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.Security.PassportAuthenticationEventHandler?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.Security.PassportAuthenticationModule?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.Security.PassportIdentity?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.Security.PassportPrincipal?displayProperty=fullName>|Ce type est obsolète. Le produit d’authentification Passport n’est plus pris en charge et a été remplacé par [Compte Microsoft](http://go.microsoft.com/fwlink/?LinkId=733413).|  
|<xref:System.Web.UI.ObjectConverter?displayProperty=fullName>|L’alternative recommandée est <xref:System.Convert?displayProperty=fullName> et <xref:System.String.Format%2A?displayProperty=fullName>.|  
  
 [Retour au début](#introduction)  
  
<a name="mobile"></a>   
### <a name="assembly-systemwebmobiledll"></a>Assembly : System.Web.Mobile.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Web.Mobile.CookielessData?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.DeviceFilterElement?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.DeviceFilterElementCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.DeviceFiltersSection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.ErrorHandlerModule?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.MobileCapabilities?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.MobileDeviceCapabilitiesSectionHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.MobileErrorInfo?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.Mobile.MobileFormsAuthentication?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.Design.MobileControls.IMobileDesigner?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.Design.MobileControls.IMobileWebFormServices?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.Design.MobileControls.MobileResource?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.Design.MobileControls.Converters.DataFieldConverter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.Design.MobileControls.Converters.DataMemberConverter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.AdRotator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Alignment?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ArrayListCollectionBase?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.BaseValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.BooleanOption?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Calendar?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Command?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.CommandFormat?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.CompareValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Constants?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ControlElement?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ControlElementCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ControlPager?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.CustomValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DesignerAdapterAttribute?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceElement?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceElementCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceOverridableAttribute?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecific?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificChoice?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificChoiceCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificChoiceControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificChoiceTemplateBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificChoiceTemplateContainer?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.DeviceSpecificControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ErrorFormatterPage?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.FontInfo?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.FontSize?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Form?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.FormControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.FormMethod?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.IControlAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Image?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.IObjectListFieldCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.IPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ItemPager?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ITemplateable?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Label?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Link?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.List?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListCommandEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListCommandEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListDataBindEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListDataBindEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListDecoration?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ListSelectType?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LiteralLink?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LiteralText?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LiteralTextContainerControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LiteralTextControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LoadItemsEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.LoadItemsEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileControl?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileControlsSection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileControlsSectionHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileListItem?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileListItemCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileListItemType?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobilePage?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileTypeNameConverter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.MobileUserControl?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectList?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListCommand?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListCommandCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListCommandEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListCommandEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListDataBindEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListDataBindEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListField?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListFieldCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListItem?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListItemCollection?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListSelectEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListSelectEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListShowCommandsEventArgs?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListShowCommandsEventHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListTitleAttribute?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ObjectListViewMode?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.PagedControl?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.PagerStyle?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Panel?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.PanelControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.PersistNameAttribute?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.PhoneCall?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.RangeValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.RegularExpressionValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.RequiredFieldValidator?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.SelectionList?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Style?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.StyleSheet?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.StyleSheetControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TemplateContainer?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TextBox?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TextBoxControlBuilder?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TextControl?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TextView?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.TextViewElement?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.ValidationSummary?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Wrapping?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlCalendarAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlCommandAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlFormAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlImageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlLinkAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlMobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlPhoneCallAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlSelectionListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ChtmlTextBoxAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.ControlAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlCalendarAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlCommandAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlControlAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlFormAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlImageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlLabelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlLinkAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlLiteralTextAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlMobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlObjectListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlPanelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlPhoneCallAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlSelectionListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlTextBoxAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlTextViewAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlValidationSummaryAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.HtmlValidatorAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.MobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.MultiPartWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.UpWmlMobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.UpWmlPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlCalendarAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlCommandAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlControlAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlFormAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlImageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlLabelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlLinkAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlLiteralTextAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlMobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlObjectListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlPanelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlPhoneCallAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlPostFieldType?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlSelectionListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlTextBoxAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlTextViewAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlValidationSummaryAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.WmlValidatorAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.Doctype?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.StyleSheetLocation?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlCalendarAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlCommandAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlControlAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlCssHandler?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlFormAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlImageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlLabelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlLinkAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlLiteralTextAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlMobileTextWriter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlObjectListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlPageAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlPanelAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlPhoneCallAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlSelectionListAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlTextBoxAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlTextViewAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlValidationSummaryAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
|<xref:System.Web.UI.MobileControls.Adapters.XhtmlAdapters.XhtmlValidatorAdapter?displayProperty=fullName>|L'assembly System.Web.Mobile.dll est déconseillé et ne doit plus être utilisé. Pour plus d’informations sur le développement d’applications mobiles ASP.NET, consultez [ASP.NET pour les mobiles](http://go.microsoft.com/fwlink/?LinkId=157231).|  
  
 [Retour au début](#introduction)  
  
<a name="workflow_activities"></a>   
### <a name="assembly-systemworkflowactivitiesdll"></a>Assembly : System.Workflow.Activities.dll  
  
|Type|Message|  
|----------|-------------|  
|Tous les types dans l’espace de noms <xref:System.Workflow.Activities?displayProperty=fullName>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.Activities.Configuration.ActiveDirectoryRoleFactoryConfiguration?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.Activities.Rules.RuleActionTrackingEvent?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.Activities.Rules.RuleConditionReference?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.Activities.Rules.RuleSetReference?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
  
 [Retour au début](#introduction)  
  
<a name="workflow_componentmodel"></a>   
### <a name="assembly-systemworkflowcomponentmodeldll"></a>Assembly : System.Workflow.ComponentModel.dll  
  
|Type|Message|  
|----------|-------------|  
|Tous les types dans l’espace de noms xref:System.Workflow.ComponentModel> sauf <xref:System.Workflow.ComponentModel.GetValueOverride?displayProperty=fullName> et <xref:System.Workflow.ComponentModel.SetValueOverride?displayProperty=fullName>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.ComponentModel.Compiler> sauf <xref:System.Workflow.ComponentModel.Compiler.ValidationError?displayProperty=fullName> et <xref:System.Workflow.ComponentModel.Compiler.ValidationErrorCollection?displayProperty=fullName>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.ComponentModel.Design> sauf <xref:System.Workflow.ComponentModel.Design.ConnectorEventHandler>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.ActivityCodeDomSerializationManager?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.ActivityCodeDomSerializer?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.ActivityMarkupSerializer?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.ActivitySurrogateSelector?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.ActivityTypeCodeDomSerializer?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.CompositeActivityMarkupSerializer?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.ComponentModel.Serialization.DependencyObjectCodeDomSerializer?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
  
 [Retour au début](#introduction)  
  
<a name="workflow_runtime"></a>   
### <a name="assembly-systemworkflowruntimedll"></a>Assembly : System.Workflow.Runtime.dll  
  
|Type|Message|  
|----------|-------------| 
|System.Activities.Statements.Interop](assetId:///T:System.Activities.Statements.Interop)|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br />Les types Workflow Foundation 3.0 sont dépréciés. Au lieu de cela, utilisez les types Workflow 4.0 de <xref:System.Activities>.\*.|  
|<xref:System.Activities.Tracking.InteropTrackingRecord>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br />Les types Workflow Foundation 3.0 sont dépréciés. Au lieu de cela, utilisez les types Workflow 4.0 de <xref:System.Activities>.\*.|   
|Tous les types dans l’espace de noms <xref:System.Workflow.Runtime>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms .|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.Runtime.DebugEngine> sauf <xref:System.Workflow.Runtime.DebugEngine.DebugEngineCallback>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.Runtime.Hosting> sauf <xref:System.Workflow.Runtime.Hosting.WorkflowCommitWorkBatchService.CommitWorkBatchCallback>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.Runtime.Tracking>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types System.Workflow.\* sont dépréciés. Utilisez plutôt les nouveaux types de <xref:System.Activities>.\*.|  
  
 [Retour au début](#introduction)  
  
<a name="workflowservices"></a>   
### <a name="assembly-systemworkflowservicesdll"></a>Assembly : System.WorkflowServices.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.ServiceModel.WorkflowServiceHost?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Activation.WorkflowServiceHostFactory?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Activities.Description.WorkflowRuntimeEndpoint?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Configuration.ExtendedWorkflowRuntimeServiceElementCollection?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Configuration.PersistenceProviderElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Configuration.WorkflowRuntimeElement?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Description.DurableOperationAttribute?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Description.DurableServiceAttribute?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Description.PersistenceProviderBehavior?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Description.UnknownExceptionAction?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Description.WorkflowRuntimeBehavior?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Dispatcher.DurableOperationContext?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.InstanceLockException?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.InstanceNotFoundException?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.LockingPersistenceProvider?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.PersistenceException?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.PersistenceProvider?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.PersistenceProviderFactory?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.ServiceModel.Persistence.SqlPersistenceProviderFactory?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|Tous les types dans l’espace de noms <xref:System.Workflow.Activities?displayProperty=fullName>.|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
|<xref:System.Workflow.Runtime.Hosting.ChannelManagerService?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> Les types WF 3 sont dépréciés. Utilisez plutôt les nouveaux types WF 4 de <xref:System.Activities>.\*.|  
  
 [Retour au début](#introduction)  
  
<a name="xaml"></a>   
### <a name="assembly-systemxamldll"></a>Assembly : System.Xaml.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Windows.Markup.AcceptedMarkupExtensionExpressionTypeAttribute?displayProperty=fullName>|Cela n'est pas utilisé par l'analyseur XAML. Examinez <xref:System.Windows.Markup.XamlSetMarkupExtensionAttribute?displayProperty=fullName>.|  
  
 [Retour au début](#introduction)  
  
<a name="xml"></a>   
### <a name="assembly-systemxmldll"></a>Assembly : System.Xml.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Xml.IApplicationResourceStreamResolver?displayProperty=fullName>|Déprécié pour la première fois dans .NET Framework 4.5.<br /><br /> L'utilisation de ce type génère une erreur du compilateur.<br /><br /> Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Xml.Schema.XmlSchemaCollection?displayProperty=fullName>|Utilisez <xref:System.Xml.Schema.XmlSchemaSet?displayProperty=fullName> pour la compilation et la validation du schéma.|  
|<xref:System.Xml.XmlValidatingReader?displayProperty=fullName>|Utilisez plutôt un <xref:System.Xml.XmlReader?displayProperty=fullName> créé par la méthode <xref:System.Xml.XmlReader.Create%2A?displayProperty=fullName> à l’aide du <xref:System.Xml.XmlReaderSettings?displayProperty=fullName> approprié.|  
|<xref:System.Xml.XmlXapResolver?displayProperty=fullName>|L'utilisation de ce type génère une erreur du compilateur. Cette API prend en charge l'infrastructure .NET Framework et n'est pas destinée à être directement utilisée à partir de votre code.|  
|<xref:System.Xml.Xsl.XslTransform?displayProperty=fullName>|Cette classe est dépréciée. Utilisez <xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=fullName> à la place.|  
  
 [Retour au début](#introduction)  
  
<a name="WindowsBase"></a>   
### <a name="assembly-windowsbasedll"></a>Assembly : WindowsBase.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:System.Windows.Markup.IReceiveMarkupExtension?displayProperty=fullName>|<xref:System.Windows.Markup.IReceiveMarkupExtension?displayProperty=fullName> est déprécié. Cette interface n'est plus utilisée.|  
  
 [Retour au début](#introduction)  
  
<a name="obsolete_types_in_microsoft_assemblies"></a>   
## <a name="obsolete-types-in-microsoft-assemblies"></a>Types obsolètes dans les assemblys Microsoft  
 Les sections suivantes répertorient les types obsolètes dans les assemblys Microsoft. Il s'agit d'assemblys ayant un usage spécial, comme les assemblys qui ciblent un langage individuel (par exemple, Microsoft.JScript.dll ou Microsoft.VisualC.dll).  
  
<a name="IEHost"></a>   
### <a name="assembly-iehostdll-and-ieexecexe"></a>Assembly : IEHost.dll et IEExec.exe  
 Les assemblys IEHost.dll et IEExec.exe ont été supprimés du .NET Framework. Tous leurs types et leurs membres sont obsolètes et ne sont pas pris en charge à partir de [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)]. Ces assemblys ont été utilisés pour héberger des contrôles Windows Forms et exécuter des exécutables dans Internet Explorer. Les alternatives recommandées incluent ClickOnce, des applications du navigateur XAML (XBAP) et Microsoft Silverlight.  
  
 [Retour au début](#introduction)  
  
<a name="Engine"></a>   
### <a name="assembly-microsoftbuildenginedll"></a>Assembly : Microsoft.Build.Engine.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:Microsoft.Build.BuildEngine.Engine?displayProperty=fullName>|Cette classe est dépréciée. Utilisez plutôt <xref:Microsoft.Build.Evaluation.ProjectCollection?displayProperty=fullName> de l’assembly <!--zz <xref:Microsoft.Build?displayProperty=fullName> -->``Microsoft.Build`.|  
|<xref:Microsoft.Build.BuildEngine.Project?displayProperty=fullName>|Cette classe est dépréciée. Utilisez plutôt <xref:Microsoft.Build.Evaluation.ProjectCollection?displayProperty=fullName> de l’assembly <xref:Microsoft.Build?displayProperty=fullName>.|  
  
 [Retour au début](#introduction)  
  
<a name="jscript"></a>   
### <a name="assembly-microsoftjscriptdll"></a>Assembly : Microsoft.JScript.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:Microsoft.JScript.Vsa.BaseVsaEngine?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.BaseVsaSite?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.BaseVsaStartup?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaCodeItem?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaEngine?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaError?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaGlobalItem?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaItem?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaItems?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaPersistSite?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaReferenceItem?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.IJSVsaSite?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.JSVsaError?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.JSVsaException?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.JSVsaItemFlag?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.JSVsaItemType?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.ResInfo?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
|<xref:Microsoft.JScript.Vsa.VsaEngine?displayProperty=fullName>|L’utilisation de ce type n’est pas recommandée, car il est déconseillé dans Visual Studio 2005 ; cette fonctionnalité ne sera pas remplacée. Pour obtenir une aide supplémentaire, consultez la documentation <xref:System.CodeDom.Compiler.ICodeCompiler?displayProperty=fullName>.|  
  
 [Retour au début](#introduction)  
  
<a name="VBCompat"></a>   
### <a name="assembly-microsoftvisualbasiccompatibilitydll"></a>Assembly : Microsoft.VisualBasic.Compatibility.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.BaseControlArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.BaseOcxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ButtonArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.CheckBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.CheckedListBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ColorDialogArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ComboBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DirListBox?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DirListBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DriveListBox?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DriveListBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.FileListBox?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.FileListBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.FixedLengthString?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.FontDialogArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.FormShowConstants?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.GroupBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.HScrollBarArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ImageListArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.LabelArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ListBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ListBoxItem?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ListViewArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.LoadResConstants?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.MaskedTextBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.MenuItemArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.MouseButtonConstants?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.OpenFileDialogArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.PanelArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.PictureBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.PrintDialogArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ProgressBarArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.RadioButtonArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.RichTextBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.SaveFileDialogArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ScaleMode?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ShiftConstants?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.StatusBarArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.StatusStripArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.Support?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.TabControlArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.TextBoxArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.TimerArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ToolBarArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ToolStripArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ToolStripMenuItemArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.TreeViewArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.VScrollBarArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebBrowserArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClass?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassContainingClassNotOptional?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassCouldNotFindEvent?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassNextItemCannotBeCurrentWebItem?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassNextItemRespondNotFound?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassUserWebClassNameNotOptional?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassWebClassFileNameNotOptional?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebClassWebItemNotValid?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItem?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemAssociatedWebClassNotOptional?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemClosingTagNotFound?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemCouldNotLoadEmbeddedResource?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemCouldNotLoadTemplateFile?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemNameNotOptional?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemNoTemplateSpecified?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemTooManyNestedTags?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.WebItemUnexpectedErrorReadingTemplateFile?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ZOrderConstants?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
  
 [Retour au début](#introduction)  
  
<a name="VBCompatData"></a>   
### <a name="assembly-microsoftvisualbasiccompatibilitydatadll"></a>Assembly : Microsoft.VisualBasic.Compatibility.Data.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.BOFActionEnum?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.EndOfRecordsetDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.EOFActionEnum?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.ErrorDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.FetchCompleteDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.FetchProgressDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.FieldChangeCompleteDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.MoveCompleteDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.OrientationEnum?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.RecordChangeCompleteDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.RecordsetChangeCompleteDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.WillChangeFieldDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.WillChangeRecordDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.WillChangeRecordsetDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODC.WillMoveDelegate?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.ADODCArray?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.BaseDataEnvironment?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.BindingCollectionEnumerator?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.CONNECTDATA?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBBINDING?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBCOLUMNINFO?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBID?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBinding?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBindingCollection?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBKINDENUM?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.DBPROPIDSET?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IAccessor?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IChapteredRowset?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IColumnsInfo?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IConnectionPoint?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IConnectionPointContainer?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IDataFormat?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IDataFormatDisp?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IEnumConnectionPoints?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IEnumConnections?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowPosition?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowPositionChange?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowset?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowsetChange?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowsetIdentity?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowsetInfo?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.IRowsetNotify?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.MBinding?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.MBindingCollection?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.SRDescriptionAttribute?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.UGUID?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.UNAME?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
|<xref:Microsoft.VisualBasic.Compatibility.VB6.UpdateMode?displayProperty=fullName>|Consultez [Microsoft.VisualBasic.Compatibility.VB6.\<membre> est obsolète et pris en charge dans les processus 32 bits uniquement](https://msdn.microsoft.com/library/ee839621.aspx).|  
  
 [Retour au début](#introduction)  
  
<a name="visualc"></a>   
### <a name="assembly-microsoftvisualcdll"></a>Assembly : Microsoft.VisualC.dll  
  
|Type|Message|  
|----------|-------------|  
|<xref:Microsoft.VisualC.DebugInfoInPDBAttribute?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.DecoratedNameAttribute?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.IsConstModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.IsCXXReferenceModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.IsLongModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.IsSignedModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.IsVolatileModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.MiscellaneousBitsAttribute?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.NeedsCopyConstructorModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
|<xref:Microsoft.VisualC.NoSignSpecifiedModifier?displayProperty=fullName>|Microsoft.VisualC.dll est un assembly obsolète et existe uniquement à des fins de compatibilité descendante.|  
  
## <a name="see-also"></a>Voir aussi  
 [Éléments obsolètes dans la bibliothèque de classes](../../../docs/framework/whats-new/whats-obsolete.md)   
 [Membres obsolètes](../../../docs/framework/whats-new/obsolete-members.md)
