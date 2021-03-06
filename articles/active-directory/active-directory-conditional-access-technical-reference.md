---
title: "Référence technique de Azure Active Directory Conditional Access | Microsoft Docs"
description: "Découvrez comment utiliser le contrôle de l’accès conditionnel dans Azure Active Directory. Spécifiez les conditions d’authentification des utilisateurs et du contrôle d’accès à votre application. Lorsque les conditions spécifiées sont satisfaites, les utilisateurs sont authentifiés et peuvent accéder à votre application."
services: active-directory.
documentationcenter: 
author: MarkusVi
manager: femila
ms.assetid: 56a5bade-7dcc-4dcf-8092-a7d4bf5df3c1
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 11/19/2017
ms.author: markvi
ms.reviewer: spunukol
ms.openlocfilehash: c9e44a696010541ab153597bb1ab5d556c2e7b65
ms.sourcegitcommit: f67f0bda9a7bb0b67e9706c0eb78c71ed745ed1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2017
---
# <a name="azure-active-directory-conditional-access-technical-reference"></a>Référence technique de Azure Active Directory Conditional Access

Vous pouvez utiliser [l’accès conditionnel Azure Active Directory (Azure AD)](active-directory-conditional-access-azure-portal.md) pour préciser les méthodes d’accès des utilisateurs autorisés aux ressources.  

Cette rubrique fournit des informations de support sur les options de configuration suivantes pour une stratégie d’accès conditionnel : 

- Affectations des applications cloud

- Condition de plateforme d’appareil 

- Condition des applications clientes

- Exigence d’une application cliente approuvée



## <a name="cloud-apps-assignments"></a>Affectations des applications cloud

Lorsque vous configurez une stratégie d’accès conditionnel, vous devez [sélectionner les applications cloud utilisant votre stratégie](active-directory-conditional-access-azure-portal.md#who). 

![Sélectionner les applications cloud pour votre stratégie](./media/active-directory-conditional-access-technical-reference/09.png)


### <a name="microsoft-cloud-applications"></a>Applications cloud Microsoft

Vous pouvez affecter une stratégie d’accès conditionnel aux applications cloud Microsoft  suivantes :

- Azure Information Protection - [En savoir plus](https://docs.microsoft.com/information-protection/get-started/faqs#i-see-azure-information-protection-is-listed-as-an-available-cloud-app-for-conditional-accesshow-does-this-work)
- Azure RemoteApp

- Microsoft Dynamics 365

- Microsoft Office 365 Yammer

- Microsoft Office 365 Exchange Online

- Microsoft Office 365 SharePoint Online (y compris OneDrive Entreprise)

- Microsoft Power BI 

- Microsoft Visual Studio Team Services

- Microsoft Teams


### <a name="other-applications"></a>Autres applications 

Outre les applications cloud Microsoft, vous pouvez affecter une stratégie d’accès conditionnel aux types d’applications cloud suivants :

- applications connectées à Azure AD ;

- application software as a service (SaaS) fédérée préintégrée ;

- applications qui utilisent l’authentification unique (SSO) par mot de passe ;

- applications métier ;

- applications utilisant le proxy d’application Azure AD.


## <a name="device-platform-condition"></a>Condition de plateforme d’appareil

Dans une stratégie d’accès conditionnel, vous pouvez configurer la condition de plateforme d’appareil pour lier la stratégie au système d’exploitation d’un client. L’accès conditionnel Azure AD prend en charge les plateformes suivantes :

- Android

- iOS

- Windows Phone

- Windows

- macOS


![Lier la stratégie d’accès au système d’exploitation client](./media/active-directory-conditional-access-technical-reference/41.png)





## <a name="client-apps-condition"></a>Condition d’applications clientes 

Lorsque vous configurez une stratégie d’accès conditionnel, vous pouvez [sélectionner des applications clientes](active-directory-conditional-access-azure-portal.md#client-apps) pour les conditions d’applications clientes. Configurez la condition d’applications clientes afin d’accorder ou de bloquer l’accès en cas de tentative d’accès à partir des types d’applications clientes suivantes :

- Browser
- Applications mobiles et de bureau

![Contrôler l’accès pour les applications clientes](./media/active-directory-conditional-access-technical-reference/03.png)

### <a name="supported-browsers"></a>Navigateurs pris en charge 

Contrôlez l’accès du navigateur à l’aide de l’option **Navigateur** dans votre stratégie d’accès conditionnel. L’accès est accordé uniquement lorsque la tentative d’accès est effectuée depuis un navigateur pris en charge. Dans le cas contraire, la tentative est bloquée.

![Contrôler l’accès pour les navigateurs pris en charge](./media/active-directory-conditional-access-technical-reference/05.png)

Dans une stratégie d’accès conditionnel, les navigateurs suivants sont pris en charge : 


| SE                     | Navigateurs                            | Support     |
| :--                    | :--                                 | :-:         |
| Windows 10             | Internet Explorer, Edge, Chrome     | ![Vérification][1] |
| Windows 8 / 8.1        | Internet Explorer, Chrome           | ![Vérification][1] |
| Windows 7              | Internet Explorer, Chrome           | ![Vérification][1] |
| iOS                    | Safari, Intune Managed Browser      | ![Vérification][1] |
| Android                | Chrome, Intune Managed Browser      | ![Vérification][1] |
| Windows Phone          | Internet Explorer, Edge             | ![Vérification][1] |
| Windows Server 2016    | Internet Explorer, Edge             | ![Vérification][1] |
| Windows Server 2016    | Chrome                              | Bientôt disponible |
| Windows Server 2012 R2 | Internet Explorer, Chrome           | ![Vérification][1] |
| Windows Server 2008 R2 | Internet Explorer, Chrome           | ![Vérification][1] |
| macOS                  | Chrome, Safari                      | ![Vérification][1] |


> [!NOTE]
> La prise en charge de Chrome nécessite l’installation de Windows 10 Creators Update (version 1703) ou version ultérieure.<br>
> Vous pouvez installer [cette extension](https://chrome.google.com/webstore/detail/windows-10-accounts/ppnbnpeolgkicgegkbkbjmhlideopiji).

### <a name="supported-mobile-applications-and-desktop-clients"></a>Applications mobiles et clients de bureau pris en charge

Contrôlez l’accès client et de l’application à l’aide de l’option **Applications mobiles et clients de bureau** dans votre stratégie d’accès conditionnel. L’accès est accordé uniquement lorsque la tentative d’accès est effectuée depuis une application mobile ou un client de bureau pris en charge. Dans le cas contraire, la tentative est bloquée.

![Contrôler l’accès pour les applications mobiles ou les clients de bureau pris en charge](./media/active-directory-conditional-access-technical-reference/06.png)

Les applications mobiles et clients de bureau suivants prennent en charge l’accès conditionnel à Office 365 et à d’autres applications de service connectées à Azure AD :


| Applications clientes| Service cible| Plateforme |
| --- | --- | --- |
| Application distante Azure| Service Application distante Azure| Windows 10, Windows 8.1, Windows 7, iOS, Android et MAC OS X|
| Application Dynamics CRM| Dynamics CRM| Windows 10, Windows 8.1, Windows 7, iOS, Android|
| Application de messagerie/calendrier/contacts, Outlook 2016, Outlook 2013 (avec l’authentification moderne)| Office 365 Exchange Online| Windows 10|
| Stratégie MFA et d’emplacement pour les applications. Les stratégies basées sur les appareils ne sont pas prises en charge.| Tout service d’application Mes applications| Android et iOS|
| Services Microsoft Teams, soit tous les services qui prennent en charge Microsoft Teams et toutes ses applications clientes : Bureau Windows, iOS, Android, WP et client web| Microsoft Teams| Windows 10, Windows 8.1, Windows 7, iOS, Android et macOS|
| Applications Office 2016, Office 2013 (avec authentification moderne), client de synchronisation OneDrive (voir [notes](https://support.office.com/en-US/article/Azure-Active-Directory-conditional-access-with-the-OneDrive-sync-client-on-Windows-028d73d7-4b86-4ee0-8fb7-9a209434b04e))| Office 365 SharePoint Online| Windows 8.1, Windows 7|
| Applications Office 2016, applications Universal Office, Office 2013 (avec authentification moderne), client de synchronisation OneDrive (voir [notes](https://support.office.com/en-US/article/Azure-Active-Directory-conditional-access-with-the-OneDrive-sync-client-on-Windows-028d73d7-4b86-4ee0-8fb7-9a209434b04e)), prise en charge à venir des groupes Office et de l’application SharePoint| Office 365 SharePoint Online| Windows 10|
| Office 2016 pour Mac OS (Word, Excel, PowerPoint, OneNote uniquement). Prise en charge de OneDrive Entreprise prévue| Office 365 SharePoint Online| Mac OS X|
| Applications mobiles Office| Office 365 SharePoint Online| iOS, Android|
| Application Yammer Office| Office 365 Yammer| Windows 10, iOS, Android|
| Outlook 2016 (Office pour Mac OS)| Office 365 Exchange Online| Mac OS X|
| Outlook 2016, Outlook 2013 (avec authentification moderne), Skype Entreprise (avec authentification moderne)| Office 365 Exchange Online| Windows 8.1, Windows 7|
| Application Outlook Mobile| Office 365 Exchange Online| iOS|
| Application PowerBI. L’application Power BI pour Android ne prend pas en charge actuellement l’accès conditionnel en fonction de l’appareil.| Service PowerBI| Windows 10, Windows 8.1, Windows 7 et iOS|
| Skype Entreprise| Office 365 Exchange Online| Android, IOS|
| Application Visual Studio Team Services| Visual Studio Team Services| Windows 10, Windows 8.1, Windows 7, iOS, Android|




## <a name="approved-client-app-requirement"></a>Spécification d’application cliente approuvée 

Contrôlez les connexions clientes à l’aide de l’option **Nécessite une application cliente approuvée** dans votre stratégie d’accès conditionnel. L’accès est accordé uniquement lorsqu’une tentative de connexion est effectuée depuis une application cliente approuvée.

![Contrôler l’accès pour les applications clientes approuvées](./media/active-directory-conditional-access-technical-reference/21.png)

Les applications client suivantes peuvent être utilisées avec l’exigence d’une application cliente approuvée :


- Microsoft Azure Information Protection
- Microsoft Excel
- Microsoft OneDrive
- Microsoft OneNote
- Microsoft Outlook
- Planificateur Microsoft
- Microsoft PowerPoint
- Microsoft SharePoint
- Microsoft Skype Entreprise
- Microsoft Teams
- Microsoft Visio
- Microsoft Word



**Remarques**

- Les applications clientes approuvées prennent en charge la fonctionnalité de gestion des applications mobiles Intune.

- Exigence **Nécessite une application cliente approuvée** :

    - elle prend uniquement en charge iOS et Android pour la [condition de plate-forme de périphérique](#device-platforms-condition).

    - elle ne prend pas en charge l’option **Navigateur** pour la [condition d’applications clientes](#supported-browsers).
    
    - elle remplace l’option **Applications mobiles et clients de bureau** pour la [condition d’applications clientes](#supported-mobile-apps-and-desktop-clients) lorsque cette option est sélectionnée.


## <a name="next-steps"></a>Étapes suivantes

- Vous trouverez une vue d’ensemble de l’accès conditionnel sur la page [Accès conditionnel Azure Active Directory](active-directory-conditional-access-azure-portal.md).
- Si vous êtes prêt à configurer des stratégies d’accès conditionnel dans votre environnement, consultez les [Pratiques recommandées d’accès conditionnel dans Azure Active Directory](active-directory-conditional-access-best-practices.md).



<!--Image references-->
[1]: ./media/active-directory-conditional-access-technical-reference/01.png


