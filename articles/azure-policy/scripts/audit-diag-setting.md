---
title: "Exemple JSON Azure Policy - Auditer le paramètre de diagnostic | Microsoft Docs"
description: "Cet exemple de stratégie JSON vérifie si les paramètres de diagnostic ne sont pas activés pour des types de ressources spécifiés."
services: azure-policy
documentationcenter: 
author: bandersmsft
manager: carmonm
editor: 
ms.assetid: 
ms.service: azure-policy
ms.devlang: 
ms.topic: sample
ms.tgt_pltfrm: 
ms.workload: 
ms.date: 10/30/2017
ms.author: banders
ms.custom: mvc
ms.openlocfilehash: 0e97470491f548cafd5023851e2c2f6bd76cbe9f
ms.sourcegitcommit: 732e5df390dea94c363fc99b9d781e64cb75e220
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2017
---
# <a name="audit-diagnostic-setting"></a>Auditer le paramètre de diagnostic

Vérifie si les paramètres de diagnostic ne sont pas activés pour des types de ressources spécifiés. Spécifiez un tableau de types de ressources pour vérifier si les paramètres de diagnostic sont activés.

[!INCLUDE [quickstarts-free-trial-note](../../../includes/quickstarts-free-trial-note.md)]

## <a name="sample-template"></a>Exemple de modèle

[!code-json[main](../../../policy-templates/samples/Monitoring/audit-diagnostic-setting/azurepolicy.json "Audit diagnostic setting")]

Vous pouvez déployer ce modèle en utilisant le [portail Azure](#deploy-with-the-portal), avec [PowerShell](#deploy-with-powershell) ou avec [Azure CLI](#deploy-with-azure-cli).

## <a name="deploy-with-the-portal"></a>Déployer avec le portail

[![Déploiement sur Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/?feature.customportal=false&microsoft_azure_policy=true&microsoft_azure_policy_policyinsights=true&feature.microsoft_azure_security_policy=true&microsoft_azure_marketplace_policy=true#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-policy%2Fmaster%2Fsamples%2FMonitoring%2Faudit-diagnostic-setting%2Fazurepolicy.json)

## <a name="deploy-with-powershell"></a>Déployer avec PowerShell

[!INCLUDE [sample-powershell-install](../../../includes/sample-powershell-install-no-ssh.md)]

```powershell
$definition = New-AzureRmPolicyDefinition -Name "audit-diagnostic-setting" -DisplayName "Audit diagnostic setting" -description "Audit diagnostic setting for selected resource types" -Policy 'https://raw.githubusercontent.com/Azure/azure-policy/master/samples/Monitoring/audit-diagnostic-setting/azurepolicy.rules.json' -Parameter 'https://raw.githubusercontent.com/Azure/azure-policy/master/samples/Monitoring/audit-diagnostic-setting/azurepolicy.parameters.json' -Mode All
$definition
$assignment = New-AzureRMPolicyAssignment -Name <assignmentname> -Scope <scope>  -listOfResourceTypes <Resource Types> -PolicyDefinition $definition
$assignment
```

### <a name="clean-up-powershell-deployment"></a>Nettoyer un déploiement PowerShell

Exécutez la commande suivante pour supprimer le groupe de ressources, la machine virtuelle et toutes les ressources associées.

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

## <a name="deploy-with-azure-cli"></a>Déploiement avec l’interface de ligne de commande Azure

[!INCLUDE [sample-cli-install](../../../includes/sample-cli-install.md)]

```azurecli-interactive
az policy definition create --name 'audit-diagnostic-setting' --display-name 'Audit diagnostic setting' --description 'Audit diagnostic setting for selected resource types' --rules 'https://raw.githubusercontent.com/Azure/azure-policy/master/samples/Monitoring/audit-diagnostic-setting/azurepolicy.rules.json' --params 'https://raw.githubusercontent.com/Azure/azure-policy/master/samples/Monitoring/audit-diagnostic-setting/azurepolicy.parameters.json' --mode All

az policy assignment create --name <assignmentname> --scope <scope> --policy "audit-diagnostic-setting"
```

### <a name="clean-up-azure-cli-deployment"></a>Nettoyer un déploiement Azure CLI

Exécutez la commande suivante pour supprimer le groupe de ressources, la machine virtuelle et toutes les ressources associées.

```azurecli-interactive
az group delete --name myResourceGroup --yes
```

## <a name="next-steps"></a>Étapes suivantes

- Vous pouvez trouver d’autres exemples de modèles Azure Policy dans [Modèles pour Azure Policy](../json-samples.md).
