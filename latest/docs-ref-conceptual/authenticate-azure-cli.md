---
title: "登入 Azure CLI 2.0"
description: "登入 Linux、Mac 或 Windows 上的 Azure 2.0 CLI。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: 4ab4f0de38614eff00f55bad96ea886bb007f3c0
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="log-in-with-azure-cli-20"></a>登入 Azure CLI 2.0

有數種方式可登入及使用 Azure CLI 進行驗證。 最簡單的開始使用方法是透過瀏覽器以互動方式登入，或在命令列登入。 我們建議的方法是使用服務主體，這種方式所建立的非互動式帳戶可讓您用來處理資源。 僅授與服務主體所需的適當權限，可確保您的自動化指令碼更加安全。

您使用 CLI 所執行的命令，會針對您的預設訂用帳戶來執行。  如果您有一個以上的訂用帳戶，建議您[確認預設訂用帳戶](manage-azure-subscriptions-azure-cli.md)，並適當地加以變更。

## <a name="interactive-log-in"></a>互動式登入

以互動方式從網頁瀏覽器登入。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>命令列

在命令列上，提供您的認證。

> [!Note]
> 這個方法不適用於 Microsoft 帳戶或啟用雙重要素驗證的帳戶。

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>使用服務主體登入

服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。
從處理資源的指令碼或應用程式保護您使用 Azure 資源的最佳方式，就是使用服務主體進行驗證。
透過 `az role` 命令集來定義您想讓使用者具備的角色。
您可以在 [az 角色參考文章](https://docs.microsoft.com/cli/azure/role.md)中，進一步了解並查看服務主體角色的範例。

1. 如果您還沒有服務主體，請[建立一個](create-an-azure-service-principal-azure-cli.md)。

1. 使用服務主體登入。

   ```azurecli-interactive
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   若要取得您的租用戶，請以互動方式登入，然後從您的訂用帳戶中取得 tenantId。

   ```azurecli
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```