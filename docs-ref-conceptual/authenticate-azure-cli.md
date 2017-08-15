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
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2017
---
# <a name="log-in-with-azure-cli-20"></a><span data-ttu-id="55ab7-104">登入 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="55ab7-104">Log in with Azure CLI 2.0</span></span>

<span data-ttu-id="55ab7-105">有數種方式可登入及使用 Azure CLI 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="55ab7-105">There are several ways to log in and authenticate with the Azure CLI.</span></span> <span data-ttu-id="55ab7-106">最簡單的開始使用方法是透過瀏覽器以互動方式登入，或在命令列登入。</span><span class="sxs-lookup"><span data-stu-id="55ab7-106">The simplest way to get started is to log in interactively through your browser, or to log in at the command line.</span></span> <span data-ttu-id="55ab7-107">我們建議的方法是使用服務主體，這種方式所建立的非互動式帳戶可讓您用來處理資源。</span><span class="sxs-lookup"><span data-stu-id="55ab7-107">Our recommended approach is to use service principals, which provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="55ab7-108">僅授與服務主體所需的適當權限，可確保您的自動化指令碼更加安全。</span><span class="sxs-lookup"><span data-stu-id="55ab7-108">By granting just the appropriate permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="55ab7-109">您使用 CLI 所執行的命令，會針對您的預設訂用帳戶來執行。</span><span class="sxs-lookup"><span data-stu-id="55ab7-109">Commands that you run with the CLI are run against your default subscription.</span></span>  <span data-ttu-id="55ab7-110">如果您有一個以上的訂用帳戶，建議您[確認預設訂用帳戶](manage-azure-subscriptions-azure-cli.md)，並適當地加以變更。</span><span class="sxs-lookup"><span data-stu-id="55ab7-110">If you have more than one subscription, you may want to [confirm your default subscription](manage-azure-subscriptions-azure-cli.md) and change it appropriately.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="55ab7-111">互動式登入</span><span class="sxs-lookup"><span data-stu-id="55ab7-111">Interactive log-in</span></span>

<span data-ttu-id="55ab7-112">以互動方式從網頁瀏覽器登入。</span><span class="sxs-lookup"><span data-stu-id="55ab7-112">Log in interactively from your web browser.</span></span>

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a><span data-ttu-id="55ab7-113">命令列</span><span class="sxs-lookup"><span data-stu-id="55ab7-113">Command line</span></span>

<span data-ttu-id="55ab7-114">在命令列上，提供您的認證。</span><span class="sxs-lookup"><span data-stu-id="55ab7-114">Provide your credentials on the command line.</span></span>

> [!Note]
> <span data-ttu-id="55ab7-115">這個方法不適用於 Microsoft 帳戶或啟用雙重要素驗證的帳戶。</span><span class="sxs-lookup"><span data-stu-id="55ab7-115">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a><span data-ttu-id="55ab7-116">使用服務主體登入</span><span class="sxs-lookup"><span data-stu-id="55ab7-116">Logging in with a service principal</span></span>

<span data-ttu-id="55ab7-117">服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。</span><span class="sxs-lookup"><span data-stu-id="55ab7-117">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span>
<span data-ttu-id="55ab7-118">從處理資源的指令碼或應用程式保護您使用 Azure 資源的最佳方式，就是使用服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="55ab7-118">Authenticating with a service principal is the best way to secure the usage of your Azure resources from either your scripts or applications that manipulate resources.</span></span>
<span data-ttu-id="55ab7-119">透過 `az role` 命令集來定義您想讓使用者具備的角色。</span><span class="sxs-lookup"><span data-stu-id="55ab7-119">You define the roles you want your users to have via the `az role` set of commands.</span></span>
<span data-ttu-id="55ab7-120">您可以在 [az 角色參考文章](https://docs.microsoft.com/cli/azure/role.md)中，進一步了解並查看服務主體角色的範例。</span><span class="sxs-lookup"><span data-stu-id="55ab7-120">You can learn more and see examples of service principal roles in our [az role reference articles](https://docs.microsoft.com/cli/azure/role.md).</span></span>

1. <span data-ttu-id="55ab7-121">如果您還沒有服務主體，請[建立一個](create-an-azure-service-principal-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="55ab7-121">If you don't already have a service principal, [create one](create-an-azure-service-principal-azure-cli.md).</span></span>

1. <span data-ttu-id="55ab7-122">使用服務主體登入。</span><span class="sxs-lookup"><span data-stu-id="55ab7-122">Log in with the service principal.</span></span>

   ```azurecli-interactive
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   <span data-ttu-id="55ab7-123">若要取得您的租用戶，請以互動方式登入，然後從您的訂用帳戶中取得 tenantId。</span><span class="sxs-lookup"><span data-stu-id="55ab7-123">To get your tenant, log in interactively and then get the tenantId from your subscription.</span></span>

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