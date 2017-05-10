---
title: "使用 Azure CLI 2.0 來管理 Azure 訂用帳戶"
description: "使用 Linux、Mac 或 Windows 上的 Azure CLI 2.0 來管理 Azure 訂用帳戶。"
keywords: "Azure CLI 2.0, Linux, Mac, Windows, OS X, 訂用帳戶"
author: kamaljit
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: a28b24dd186fc567f36e52f8a0f5a7c2b0af060c
ms.sourcegitcommit: c2d380f4ad8e7606850530db690855bcccfd6e86
ms.translationtype: HT
ms.contentlocale: zh-TW
---
# <a name="manage-multiple-azure-subscriptions"></a>管理多個 Azure 訂用帳戶

如果您是 Azure 的新手，可能只會擁有單一訂用帳戶。
但是，如果您已使用 Azure 一段時間，就可能已建立了多個 Azure 訂用帳戶。
如果是如此，您可以將 Azure CLI 2.0 設定為針對特定的訂用帳戶執行命令。

1. 取得您帳戶中所有訂用帳戶的清單。

   ```azurecli
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. 預設設定。
 
   ```azurecli
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > `--subscription` 參數會使用訂用帳戶名稱或訂用帳戶識別碼。

您可以再次執行 `az account list --output table` 命令來驗證變更。

一旦您設定預設訂用帳戶後，所有後續的 Azure CLI 命令會對此訂用帳戶執行。