---
title: "Comment&#160;: cr&#233;er une liaison WSFederationHttpBinding | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "fédération"
  - "WCF, fédération"
ms.assetid: e54897d7-aa6c-46ec-a278-b2430c8c2e10
caps.latest.revision: 16
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 16
---
# Comment&#160;: cr&#233;er une liaison WSFederationHttpBinding
Dans [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)], la classe <xref:System.ServiceModel.WSFederationHttpBinding> \([\<wsFederationHttpBinding\>](../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) dans la configuration\) fournit un mécanisme pour exposer un service fédéré,  autrement dit, un service qui oblige les clients à s'authentifier à l'aide d'un jeton de sécurité émis par un service de jeton de sécurité.  Cette rubrique montre comment installer <xref:System.ServiceModel.WSFederationHttpBinding> dans le code et la configuration.  Une fois la liaison créée, vous pouvez installer un point de terminaison pour utiliser cette liaison.  
  
 Les étapes de base sont les suivantes :  
  
1.  Sélectionnez un mode de sécurité.  <xref:System.ServiceModel.WSFederationHttpBinding> prend en charge `Message`, qui fournit la sécurité de bout en bout au niveau du message, même avec plusieurs sauts, et `TransportWithMessageCredential`, qui fournit les meilleures performances dans les cas où le client et le service peuvent établir une connexion directe sur HTTPS.  
  
    > [!NOTE]
    >  <xref:System.ServiceModel.WSFederationHttpBinding> prend également en charge `None` comme mode de sécurité.  Ce mode, non sécurisé, est fourni à des fins de débogage uniquement.  Si un point de terminaison de service est déployé avec <xref:System.ServiceModel.WSFederationHttpBinding> alors que son mode de sécurité a la valeur `None`, la liaison cliente obtenue \(générée par l'[Outil Service Model Metadata Tool \(Svcutil.exe\)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)\) est <xref:System.ServiceModel.WsHttpBinding> avec un mode de sécurité ayant la valeur `None`.  
  
     Contrairement à d'autres liaisons fournies par le système, il n'est pas nécessaire de sélectionner un type d'informations d'identification du client lors de l'utilisation de `WSFederationHttpBinding`.  Cela est dû au fait que le type d'informations d'identification du client est toujours un jeton émis.  [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] acquiert un jeton d'un émetteur spécifié et présente ce jeton au service pour authentifier le client.  
  
2.  Sur les clients fédérés, affectez à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerAddress%2A> l'URL du service de jeton de sécurité.  Affectez au <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerBinding%2A> la liaison à utiliser pour communiquer avec le service de jeton de sécurité.  
  
3.  Facultatif.  Affectez à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuedTokenType%2A> l'URI \(Uniform Resource Identifier\) d'un type de jeton.  Sur les services fédérés, spécifiez le type de jeton que le service attend.  Sur les clients fédérés, spécifiez le type de jeton que le client demande au service de jeton de sécurité.  
  
     Si aucun type de jeton n'est spécifié, les clients génèrent des jetons RST \(Request Security Token\) WS\-Trust sans l'URI d'un type de jeton, et les services attendent l'authentification du client à l'aide d'un jeton SAML \(Security Assertions Markup Language\) 1.1 par défaut.  
  
     L'URI d'un jeton SAML 1.1 est "http:\/\/docs.oasis\-open.org\/wss\/oasis\-wss\-saml\-token\-profile\-1.1\#SAMLV1.1".  
  
4.  Facultatif.  Sur les services fédérés, affectez à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A> l'URL de métadonnées d'un service de jeton de sécurité.  Le point de terminaison de métadonnées permet aux clients du service de sélectionner une paire liaison\/point de terminaison appropriée, si le service est configuré pour publier des métadonnées.  [!INCLUDE[crabout](../../../../includes/crabout-md.md)] la publication de métadonnées, consultez [Publication de métadonnées](../../../../docs/framework/wcf/feature-details/publishing-metadata.md).  
  
 Vous pouvez également définir d'autres propriétés, y compris le type de clé utilisé comme clé de vérification dans le jeton émis, la suite algorithmique à utiliser entre le client et le service, l'option de négocier ou de spécifier explicitement les informations d'identification du service, toutes les revendications spécifiques que le service s'attend à trouver dans le jeton émis et tous les éléments XML supplémentaires qui doivent être ajoutés à la demande que le client envoie au service de jeton de sécurité.  
  
> [!NOTE]
>  La propriété `NegotiateServiceCredential` n'est pertinente que si `SecurityMode` a la valeur `Message`.  Si `SecurityMode` a la valeur `TransportWithMessageCredential`, alors la propriété `NegotiateServiceCredential` est ignorée.  
  
### Pour configurer une liaison WSFederationHttpBinding dans le code  
  
1.  Créez une instance de <xref:System.ServiceModel.WSFederationHttpBinding>.  
  
2.  Affectez à la propriété <xref:System.ServiceModel.WSFederationHttpSecurity.Mode%2A> la valeur <xref:System.ServiceModel.WSFederationHttpSecurityMode> ou <xref:System.ServiceModel.WSFederationHttpSecurityMode> selon le cas.  Si une suite algorithmique autre que <xref:System.ServiceModel.Security.SecurityAlgorithmSuite.Basic256%2A> est requise, affectez à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.AlgorithmSuite%2A> une valeur extraite de <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.  
  
3.  Définissez la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.NegotiateServiceCredential%2A> comme il convient.  
  
4.  Affectez à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuedKeyType%2A> la valeur <xref:System.IdentityModel.Tokens.SecurityKeyType> `SymmetricKey` ou .`AsymmetricKey` selon le cas.  
  
5.  Affectez la valeur appropriée à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuedTokenType%2A>.  Si aucune valeur n'est définie, [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] a la valeur par défaut "http:\/\/docs.oasis\-open.org\/wss\/oasis\-wss\-saml\-token\-profile\-1.1\#SAMLV1.1", qui indique des jetons SAML 1.1.  
  
6.  Requis sur le client si aucun émetteur local n'est spécifié ; facultatif sur le service.  Créez un <xref:System.ServiceModel.EndpointAddress> qui contient les informations d'adresse et d'identité du service de jeton de sécurité et assignez l'instance <xref:System.ServiceModel.EndpointAddress> à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerAddress%2A>.  
  
7.  Requis sur le client si aucun émetteur local n'est spécifié ; non utilisé sur le service.  Créez <xref:System.ServiceModel.Channels.Binding> pour `SecurityTokenService` et assignez l'instance <xref:System.ServiceModel.Channels.Binding> à la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerBinding%2A>.  
  
8.  Non utilisé sur le client ; facultatif sur le service.  Créez une instance <xref:System.ServiceModel.EndpointAddress> pour les métadonnées du service de jeton de sécurité et assignez\-la à la propriété `IssuerMetadataAddress`.  
  
9. Facultatif sur le client et le service.  Créez et ajoutez une ou plusieurs instances <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement> à la collection retournée par la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>.  
  
10. Facultatif sur le client et le service.  Créez et ajoutez une ou plusieurs instances <xref:System.Xml.XmlElement> à la collection retournée par la propriété <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.TokenRequestParameters%2A>.  
  
### Pour créer un point de terminaison fédéré dans la configuration  
  
1.  Créez [\<wsFederationHttpBinding\>](../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) en tant qu'enfant de l'élément [\<liaisons\>](../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md) dans le fichier de configuration de l'application.  
  
2.  Créez un élément [\<liaison\>](../../../../docs/framework/misc/binding.md) en tant qu'enfant de [\<wsFederationHttpBinding\>](../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) et affectez à l'attribut `name` une valeur appropriée.  
  
3.  Créez un élément `<security>` en tant qu'enfant de l'élément [\<liaison\>](../../../../docs/framework/misc/binding.md).  
  
4.  Affectez à l'attribut `mode` sur l'élément `<security>` une valeur de `Message` ou de `TransportWithMessageCredential`, selon le cas.  
  
5.  Créez un élément `<message>` en tant qu'enfant de l'élément `<security>`.  
  
6.  Facultatif.  Affectez une valeur appropriée à l'attribut `algorithmSuite` sur l'élément `<message>`.  La valeur par défaut est `Basic256`.  
  
7.  Facultatif.  Si une clé de vérification asymétrique est requise, affectez à l'attribut `issuedKeyType` de l'élément `<message>` la valeur `AsymmetricKey`.  La valeur par défaut est `SymmetricKey`.  
  
8.  Facultatif.  Définissez l'attribut `issuedTokenType` sur l'élément `<message>`.  
  
9. Requis sur le client si aucun émetteur local n'est spécifié ; facultatif sur le service.  Créez un élément `<issuer>` en tant qu'enfant de l'élément `<message>`.  
  
10. Affectez l'attribut `address` à l'élément `<issuer>` et spécifiez l'adresse à laquelle le service de jeton de sécurité accepte des demandes de jeton.  
  
11. Facultatif.  Ajoutez un élément enfant `<identity>` et spécifiez l'identité du service de jeton de sécurité.  
  
12. [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)] [Identité du service et authentification](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
13. Requis sur le client si aucun émetteur local n'est spécifié ; non utilisé sur le service.  Créez un élément [\<liaison\>](../../../../docs/framework/misc/binding.md) dans la section des liaisons, qui peut servir à communiquer avec le service de jeton de sécurité.  [!INCLUDE[crabout](../../../../includes/crabout-md.md)] la création d'une liaison, consultez [Comment : spécifier une liaison de service dans la configuration](../../../../docs/framework/wcf/how-to-specify-a-service-binding-in-configuration.md).  
  
14. Spécifiez la liaison créée à l'étape précédente en définissant les attributs `binding` et `bindingConfiguration` de l'élément `<issuer>`.  
  
15. Non utilisé sur le client ; facultatif sur le service.  Créez un élément `<issuerMetadata>` en tant qu'enfant de l'élément \<`message`\>.  Puis, dans un attribut `address` sur l'élément `<issuerMetadata>`, spécifiez l'adresse à laquelle le service de jeton de sécurité doit publier ses métadonnées.  Éventuellement, ajoutez un élément enfant `<identity>` et spécifiez l'identité du service de jeton de sécurité.  
  
16. Facultatif sur le client et le service.  Ajoutez un élément `<claimTypeRequirements>` en tant qu'enfant de l'élément `<message>`.  Spécifiez les revendications requises et facultatives sur lesquelles repose le service en ajoutant des éléments [\<ajouter\>](../../../../docs/framework/configure-apps/file-schema/wcf/add-of-claimtyperequirements.md) à l'élément `<claimTypeRequirements>` et en spécifiant le type de revendication avec l'attribut `claimType`.  Spécifiez si une revendication donnée est requise ou facultative en définissant l'attribut `isOptional`.  
  
## Exemple  
 L'exemple de code suivant montre comment installer `WSFederationHttpBinding` de façon impérative.  
  
 [!code-csharp[c_FederationBinding#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_federationbinding/cs/source.cs#2)]
 <!-- TODO: review snippet reference [!code-vb[c_FederationBinding#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_federationbinding/vb/source.vb#2)]  -->  
  
## Voir aussi  
 [Fédération](../../../../docs/framework/wcf/feature-details/federation.md)   
 [Federation, exemple](../../../../docs/framework/wcf/samples/federation-sample.md)   
 [Comment : désactiver des sessions sécurisées sur une classe WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)