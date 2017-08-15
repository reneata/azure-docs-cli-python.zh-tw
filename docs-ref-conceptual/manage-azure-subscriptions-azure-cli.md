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
ms.openlocfilehash: 383fb6ebd90ac79f60869187b402d53d4f1791fd
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2017
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="bb63a-104">管理多個 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="bb63a-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="bb63a-105">如果您是 Azure 的新手，可能只會擁有單一訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="bb63a-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="bb63a-106">但是，如果您已使用 Azure 一段時間，就可能已建立了多個 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="bb63a-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="bb63a-107">如果是如此，您可以將 Azure CLI 2.0 設定為針對特定的訂用帳戶執行命令。</span><span class="sxs-lookup"><span data-stu-id="bb63a-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. <span data-ttu-id="bb63a-108">取得您帳戶中所有訂用帳戶的清單。</span><span class="sxs-lookup"><span data-stu-id="bb63a-108">Get a list of all subscriptions in your account.</span></span>

   ```azurecli-interactive
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. <span data-ttu-id="bb63a-109">預設設定。</span><span class="sxs-lookup"><span data-stu-id="bb63a-109">Set the default.</span></span>
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > <span data-ttu-id="bb63a-110">`--subscription` 參數會使用訂用帳戶名稱或訂用帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb63a-110">The `--subscription` parameter takes either the subscription name or the subscription ID.</span></span>

<span data-ttu-id="bb63a-111">您可以再次執行 `az account list --output table` 命令來驗證變更。</span><span class="sxs-lookup"><span data-stu-id="bb63a-111">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="bb63a-112">一旦您設定預設訂用帳戶後，所有後續的 Azure CLI 命令會對此訂用帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="bb63a-112">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>