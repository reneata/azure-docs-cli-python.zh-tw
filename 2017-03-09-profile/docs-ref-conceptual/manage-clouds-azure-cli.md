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
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="5c83a-104">使用 Azure CLI 2.0 管理多重雲端</span><span class="sxs-lookup"><span data-stu-id="5c83a-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="5c83a-105">如果您有多個與 Azure 關聯的訂用帳戶，可能可使用多個雲端。</span><span class="sxs-lookup"><span data-stu-id="5c83a-105">If you have multiple subscriptions associated with Azure, you may have more than one cloud available.</span></span> <span data-ttu-id="5c83a-106">每個雲端都有自己的相關聯端點和功能，且通常與具有不同資料保護標準或需求的特定區域相關聯。</span><span class="sxs-lookup"><span data-stu-id="5c83a-106">Each cloud has its own associated endpoints and capabilities, and is often associated with a particular region that has different data protection standards or requirements.</span></span>

<span data-ttu-id="5c83a-107">若要有效地使用多個雲端，您必須能夠在目前狀態為使用中的雲端間進行切換，且可能要建立新的雲端。</span><span class="sxs-lookup"><span data-stu-id="5c83a-107">To effectively work with multiple clouds, you will need to be able to switch between which is currently active, and possibly create new clouds.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="5c83a-108">列出雲端</span><span class="sxs-lookup"><span data-stu-id="5c83a-108">Listing clouds</span></span>

<span data-ttu-id="5c83a-109">您可以使用 [cloud list](/cli/azure/cloud#list) 命令來列出可以使用的雲端。</span><span class="sxs-lookup"><span data-stu-id="5c83a-109">You may list your available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="5c83a-110">這會告訴您哪個是目前使用中的雲端、其目前的設定檔為何，還可提供有關地區尾碼和主機名稱的資訊。</span><span class="sxs-lookup"><span data-stu-id="5c83a-110">This will tell you which cloud is currently active, what its current profile is, and can provide information on regional suffixes and host names.</span></span>

<span data-ttu-id="5c83a-111">若要取得可用雲端的清單和目前使用中的雲端：</span><span class="sxs-lookup"><span data-stu-id="5c83a-111">To get a list of the available clouds and the currently active one:</span></span>

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

## <a name="switching-the-active-cloud"></a><span data-ttu-id="5c83a-112">切換使用中的雲端</span><span class="sxs-lookup"><span data-stu-id="5c83a-112">Switching the active cloud</span></span>

<span data-ttu-id="5c83a-113">若要切換目前使用中的雲端，請執行 [cloud set](/cli/azure/cloud#set) 命令。</span><span class="sxs-lookup"><span data-stu-id="5c83a-113">In order to switch the currently active cloud, you run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="5c83a-114">這個命令會採用一個必要的引數，就是雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c83a-114">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="5c83a-115">如果您從未驗證使用中的雲端，就必須在執行任何其他 CLI 作業之前先進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="5c83a-115">If you have never authenticated for the active cloud, you will need to do so before performing any other CLI operations.</span></span> <span data-ttu-id="5c83a-116">如需驗證的指示，請參閱[使用 Azure CLI 2.0 登入](/cli/azure/authenticate-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="5c83a-116">For instructions on authenticating, see [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="register-or-unregister-a-cloud"></a><span data-ttu-id="5c83a-117">註冊或取消註冊雲端</span><span class="sxs-lookup"><span data-stu-id="5c83a-117">Register or unregister a cloud</span></span>

<span data-ttu-id="5c83a-118">如果您有自己的端點或需要不同的設定檔，請註冊新的雲端。</span><span class="sxs-lookup"><span data-stu-id="5c83a-118">Register a new cloud if you have your own endpoints or require a different profile.</span></span> <span data-ttu-id="5c83a-119">可利用 [cloud register](/cli/azure/cloud#register) 命令建立雲端。</span><span class="sxs-lookup"><span data-stu-id="5c83a-119">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="5c83a-120">此命令需要名稱，也可以依需求選擇一組功能和端點指定。</span><span class="sxs-lookup"><span data-stu-id="5c83a-120">This command requires a name, and optionally a set of capabilities and endpoint designations.</span></span>

<span data-ttu-id="5c83a-121">若要使用資源管理員的特定端點建立雲端，則需要特定的設定檔：</span><span class="sxs-lookup"><span data-stu-id="5c83a-121">To create a cloud with a specialized endpoint for the resource manager, with a specific profile:</span></span>

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

<span data-ttu-id="5c83a-122">這會建立雲端，但_不_會自動加以選取。</span><span class="sxs-lookup"><span data-stu-id="5c83a-122">This creates the cloud, but does _not_ automatically select it.</span></span>

<span data-ttu-id="5c83a-123">如果您不再需要所建立的雲端，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令取消登錄：</span><span class="sxs-lookup"><span data-stu-id="5c83a-123">If you no longer require the created cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```

