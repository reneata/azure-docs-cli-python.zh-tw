---
title: "使用 Azure CLI 2.0 管理多重雲端"
description: "使用 Azure CLI 2.0 建立、登入並管理不同的雲端。"
keywords: "Azure CLI 2.0, Azure, 雲端, 資料中心, 政府, 區域, 中國, 德國"
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>使用 Azure CLI 2.0 管理多重雲端

如果您有多個與 Azure 關聯的訂用帳戶，可能可使用多個雲端。 每個雲端都有自己的相關聯端點和功能，且通常與具有不同資料保護標準或需求的特定區域相關聯。

若要有效地使用多個雲端，您必須能夠在目前狀態為使用中的雲端間進行切換，且可能要建立新的雲端。

## <a name="listing-clouds"></a>列出雲端

您可以使用 [cloud list](/cli/azure/cloud#list) 命令來列出可以使用的雲端。 這會告訴您哪個是目前使用中的雲端、其目前的設定檔為何，還可提供有關地區尾碼和主機名稱的資訊。

若要取得可用雲端的清單和目前使用中的雲端：

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

## <a name="switching-the-active-cloud"></a>切換使用中的雲端

若要切換目前使用中的雲端，請執行 [cloud set](/cli/azure/cloud#set) 命令。 這個命令會採用一個必要的引數，就是雲端的名稱。

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> 如果您從未驗證使用中的雲端，就必須在執行任何其他 CLI 作業之前先進行這項作業。 如需驗證的指示，請參閱[使用 Azure CLI 2.0 登入](/cli/azure/authenticate-azure-cli)。

## <a name="register-or-unregister-a-cloud"></a>註冊或取消註冊雲端

如果您有自己的端點或需要不同的設定檔，請註冊新的雲端。 可利用 [cloud register](/cli/azure/cloud#register) 命令建立雲端。 此命令需要名稱，也可以依需求選擇一組功能和端點指定。

若要使用資源管理員的特定端點建立雲端，則需要特定的設定檔：

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

這會建立雲端，但_不_會自動加以選取。

如果您不再需要所建立的雲端，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令取消登錄：

```azurecli
az cloud unregister --name MyCloud
```

