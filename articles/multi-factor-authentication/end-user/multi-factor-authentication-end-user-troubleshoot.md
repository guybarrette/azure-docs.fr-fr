---
title: "Vérification en deux étapes pour résoudre les problèmes | Microsoft Docs"
description: "Ce document fournit aux utilisateurs des informations sur la procédure à suivre en cas de problème avec l'Azure Multi-Factor Authentication."
services: multi-factor-authentication
keywords: "client de l'authentification multifacteur, problème d'authentification, ID de corrélation"
documentationcenter: 
author: barlanmsft
manager: femila
ms.assetid: 8f3aef42-7f66-4656-a7cd-d25a971cb9eb
ms.service: multi-factor-authentication
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 07/06/2017
ms.author: barlan
ms.reviewer: richagi
ms.custom: end-user
ms.openlocfilehash: 0ffa3070cef8631c4b38b2aa00ac3dca0d88590b
ms.sourcegitcommit: 9a61faf3463003375a53279e3adce241b5700879
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2017
---
# <a name="get-help-with-two-step-verification"></a>Obtenir de l’aide pour la vérification en deux étapes
Cet article répond aux questions les plus courantes sur la vérification en deux étapes.

## <a name="why-do-i-have-to-perform-two-step-verification-can-i-turn-it-off"></a>Pourquoi dois-je effectuer une vérification en deux étapes ? Puis-je la désactiver ?

La vérification en deux étapes est une fonctionnalité de sécurité que votre organisation a choisie pour protéger vos comptes. Elle est plus sécurisée qu’un simple mot de passe, car elle s’appuie sur deux formes d’authentification : quelque chose que vous connaissez et quelque chose que vous avez sur vous. L’élément que vous connaissez est votre mot de passe. L’élément que vous avez sur vous est un téléphone ou un appareil que vous avez généralement avec vous. Avec la vérification en deux étapes, un pirate ne peut pas se connecter en votre nom, car même s’il récupère votre mot de passe d’une manière ou d’une autre, il n’a pas accès à votre téléphone.

Microsoft propose la vérification en deux étapes, mais votre organisation a le choix d’utiliser cette fonctionnalité ou non. Vous ne pouvez pas désactiver cette fonctionnalité si le support de votre entreprise l’exige, comme vous ne pouvez pas refuser l’utilisation d’un mot de passe pour protéger votre compte.

Si la vérification en deux étapes est activée pour votre compte Microsoft personnel et si vous souhaitez modifier vos paramètres, consultez la page [À propos de la vérification en deux étapes](https://support.microsoft.com/help/12408/microsoft-account-about-two-step-verification).

## <a name="i-dont-have-my-phone-with-me-today"></a>Je n’ai pas mon téléphone sur moi aujourd’hui

Vous laissez parfois votre téléphone à votre domicile, mais vous avez tout de même besoin de vous connecter au bureau. Essayez tout d’abord de vous connecter avec une autre méthode de vérification. Lorsque vous vous êtes inscrit pour la vérification en deux étapes, avez-vous défini plusieurs numéros de téléphone ? Pour essayer de vous connecter avec une autre méthode, procédez comme suit :

1. Ouvrez une session comme à l’ordinaire.
2. Lorsque la page de vérification en deux étapes s’ouvre, choisissez **Utiliser une autre option de vérification**.

   ![Vérification différente](./media/multi-factor-authentication-end-user-troubleshoot/diff_option.png)

3. Sélectionnez l’option de vérification que vous souhaitez utiliser.
4. Poursuivez avec la vérification en deux étapes.

Si le lien **Utiliser une autre option de vérification** n’apparaît pas, cela signifie que vous n’avez pas configuré d’autres méthodes lorsque vous vous êtes inscrit. Contactez le support de votre entreprise pour obtenir de l’aide afin de vous connecter à votre compte. Une fois que vous êtes connecté, veillez à [gérer vos paramètres](multi-factor-authentication-end-user-manage-settings.md) de manière à ajouter d’autres méthodes de vérification pour la prochaine fois.

Si le lien **Utiliser une autre option de vérification** n’apparaît pas et si vous n’avez pas accès à d’autres méthodes de vérification, contactez le support de votre entreprise pour obtenir de l’aide afin de vous connecter à votre compte.

## <a name="i-lost-my-phone-or-got-a-new-number"></a>J’ai perdu mon téléphone ou j’ai un nouveau numéro de téléphone
Il existe deux moyens d’accéder de nouveau à votre compte. Le premier consiste à se connecter avec votre autre numéro de téléphone d’authentification, si vous l’avez défini. Le second consiste à demander au support de votre entreprise d’effacer vos paramètres.

En cas de perte ou de vol de votre téléphone, nous vous recommandons également de demander au support de votre entreprise de réinitialiser vos mots de passe d’application et de désactiver les appareils mémorisés.

### <a name="use-an-alternate-phone-number"></a>Utiliser un autre numéro de téléphone
Si vous avez défini plusieurs options de vérification, notamment un numéro de téléphone secondaire ou une application d’authentification sur un autre appareil, vous pouvez utiliser l’une d’entre elles pour vous connecter.

Pour vous connecter à l’aide d’un autre numéro de téléphone, procédez comme suit :

1. Ouvrez une session comme à l’ordinaire.
2. Lorsque vous êtes invité à vérifier votre compte, choisissez **Utiliser une autre option de vérification**.

   ![Vérification différente](./media/multi-factor-authentication-end-user-troubleshoot/diff_option.png)

3. Sélectionnez le numéro de téléphone ou l’appareil auquel vous avez accès.
4. Une fois de retour dans votre compte, [gérez vos paramètres](multi-factor-authentication-end-user-manage-settings.md) pour modifier votre numéro de téléphone d’authentification.

### <a name="clear-your-settings"></a>Effacer vos paramètres
Si vous n’avez pas configuré de numéro de téléphone secondaire pour l’authentification, vous devez contacter le support de votre entreprise. Demandez-lui d’effacer vos paramètres : de cette façon, la prochaine fois que vous vous connecterez, vous serez invité à vous [réinscrire pour la vérification en deux étapes](multi-factor-authentication-end-user-first-time.md).

## <a name="i-am-not-receiving-a-text-or-call-on-my-phone"></a>Je ne reçois pas le SMS ou l’appel sur mon téléphone
Plusieurs raisons peuvent expliquer que vous ne receviez pas le SMS ou l’appel téléphonique malgré vos tentatives de connexion. S’il vous est déjà arrivé par le passé de recevoir des SMS ou des appels téléphoniques sur votre téléphone sans difficulté, il s’agit probablement d’un problème avec le fournisseur de téléphonie, et non avec votre compte. Assurez-vous de recevoir un signal de bonne qualité. Dans le cas d’un SMS, vérifiez que vous pouvez recevoir les SMS. Demandez à un ami de vous appeler ou de vous envoyer un SMS pour tester cette fonctionnalité.

Si vous avez attendu un SMS ou un appel pendant plusieurs minutes, le moyen le plus rapide d’accéder à votre compte est d’essayer une autre option.

1. Sélectionnez **Utiliser une autre option de vérification** sur la page en attente de vérification.

    ![Vérification différente](./media/multi-factor-authentication-end-user-troubleshoot/diff_option.png)
2. Sélectionnez la méthode à utiliser (numéro de téléphone ou envoi).

    Si vous avez reçu plusieurs codes de vérification, utilisez le plus récent.

Si vous n’avez pas configuré d’autres méthodes, contactez le support de votre entreprise et demandez-lui d’effacer vos paramètres. La prochaine fois que vous vous connecterez, vous devrez [reconfigurer l’authentification multifacteur](multi-factor-authentication-end-user-first-time.md).

Si vous subissez souvent des retards en raison d’un mauvais signal téléphonique, nous vous recommandons d’utiliser [l’application Microsoft Authenticator](microsoft-authenticator-app-how-to.md) sur votre smartphone. L’application peut générer des codes de sécurité aléatoires qui vous permettent de vous connecter et qui ne nécessitent pas de signal téléphonique ou de connexion Internet.

## <a name="app-passwords-are-not-working"></a>Les mots de passe d’application ne fonctionnent pas
Tout d’abord, assurez-vous que vous avez saisi correctement votre mot de passe. Le mot de passe d’application généré remplace votre mot de passe normal, mais uniquement pour les applications de bureau plus anciennes qui ne prennent pas en charge la vérification en deux étapes. Si cela ne fonctionne toujours pas, essayez de vous connecter et de [créer un mot de passe d’application](multi-factor-authentication-end-user-app-passwords.md).  Si le problème persiste, contactez le support de votre entreprise et demandez-lui de [supprimer vos mots de passe d’application existants](../multi-factor-authentication-manage-users-and-devices.md). Vous pourrez alors créer un autre mot de passe.

## <a name="i-didnt-find-an-answer-to-my-problem"></a>Je n’ai pas trouvé de réponse à mon problème.
Si malgré ces étapes de dépannage, vous rencontrez encore des problèmes, contactez le support de votre entreprise. Ils doivent être en mesure de vous aider.

## <a name="related-topics"></a>Rubriques connexes
* [Gérer les paramètres de la vérification en deux étapes](multi-factor-authentication-end-user-manage-settings.md)  
* [FAQ sur l’application Microsoft Authenticator](microsoft-authenticator-app-faq.md)
