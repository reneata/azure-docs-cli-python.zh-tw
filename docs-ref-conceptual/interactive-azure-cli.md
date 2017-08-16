---
title: "Azure CLI 2.0 互動模式"
description: "在互動模式下使用 Azure CLI 2.0。"
keywords: "Azure CLI 2.0, 互動模式"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 
ms.openlocfilehash: de6a366b84efa5475fd6146ff29c32e32dfe4672
ms.sourcegitcommit: 1791991b82e6ce8ad4a050cab1695e0c93734e08
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2017
---
# <a name="interactive-azure-cli-20"></a><span data-ttu-id="5a57c-104">互動式 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="5a57c-104">Interactive Azure CLI 2.0</span></span>

<span data-ttu-id="5a57c-105">您可以透過執行 `az interactive` 命令，在互動模式下使用 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="5a57c-105">You can use Azure CLI 2.0 in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="5a57c-106">這會讓您處於互動式殼層中，其中會自動完成命令，而且您可以存取命令及其參數的描述和命令範例。</span><span class="sxs-lookup"><span data-stu-id="5a57c-106">That places you in an interactive shell where your commands are auto-completed and you have access to descriptions of commands and their parameters and command examples.</span></span>

![互動模式](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="5a57c-108">在這裡，我們並未使用預設樣式，因為在黑色背景上閱讀效果不佳。</span><span class="sxs-lookup"><span data-stu-id="5a57c-108">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="5a57c-109">如果您尚未登入帳戶，請使用 `login` 命令來登入。</span><span class="sxs-lookup"><span data-stu-id="5a57c-109">If you're not already logged in to your account, use the `login` command to do that.</span></span>

## <a name="configure"></a><span data-ttu-id="5a57c-110">設定</span><span class="sxs-lookup"><span data-stu-id="5a57c-110">Configure</span></span>

<span data-ttu-id="5a57c-111">互動模式會依選擇顯示命令描述、參數描述及命令範例。</span><span class="sxs-lookup"><span data-stu-id="5a57c-111">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="5a57c-112">您可以使用 `F1` 來開啟或關閉描述和範例。</span><span class="sxs-lookup"><span data-stu-id="5a57c-112">You can turn descriptions and examples on or off using `F1`.</span></span>

![描述和範例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="5a57c-114">您可以使用 `F2` 來開啟或關閉參數預設值的顯示。</span><span class="sxs-lookup"><span data-stu-id="5a57c-114">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![預設值](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="5a57c-116">`F3` 可開關一些按鍵的摘要說明。</span><span class="sxs-lookup"><span data-stu-id="5a57c-116">`F3` toggles the display of some key gestures.</span></span>

![摘要說明](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="5a57c-118">Scope</span><span class="sxs-lookup"><span data-stu-id="5a57c-118">Scope</span></span>

<span data-ttu-id="5a57c-119">您可以將互動模式的範圍限定在特定的命令群組，例如 `vm` 或 `vm image`。</span><span class="sxs-lookup"><span data-stu-id="5a57c-119">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="5a57c-120">當您這麼做時，就會在該範圍中解譯所有命令。</span><span class="sxs-lookup"><span data-stu-id="5a57c-120">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="5a57c-121">如果您要在該命令群組中執行所有工作，這是省略命令的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="5a57c-121">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="5a57c-122">您可以不輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="5a57c-122">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="5a57c-123">而是將範圍限定為 vm 命令群組，然後輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="5a57c-123">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="5a57c-124">您也可以將範圍設定為較低層級的命令群組。</span><span class="sxs-lookup"><span data-stu-id="5a57c-124">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="5a57c-125">您可以使用 `%%vm image` 將範圍限定為 `vm image`。</span><span class="sxs-lookup"><span data-stu-id="5a57c-125">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="5a57c-126">在此案例中，由於我們已經將範圍限定為 `vm`，因此我們會使用 `%%image`。</span><span class="sxs-lookup"><span data-stu-id="5a57c-126">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="5a57c-127">屆時，我們可以使用 `%%..` 將範圍提升回 `vm`，或是就使用 `%%` 將範圍限定為根目錄。</span><span class="sxs-lookup"><span data-stu-id="5a57c-127">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="5a57c-128">查詢</span><span class="sxs-lookup"><span data-stu-id="5a57c-128">Query</span></span>

<span data-ttu-id="5a57c-129">您可以對所執行之上一個命令的結果執行 JMESPath 查詢。</span><span class="sxs-lookup"><span data-stu-id="5a57c-129">You can execute a JMESPath query on the results of the last command that you executed.</span></span>
<span data-ttu-id="5a57c-130">例如，在建立 VM 之後，您可以確認它是否已完整佈建。</span><span class="sxs-lookup"><span data-stu-id="5a57c-130">For example, after you create a VM, you can make sure it has fully provisioned.</span></span>

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

<span data-ttu-id="5a57c-131">若要深入了解如何查詢命令的結果，請參閱[使用 Azure 2.0 來查詢命令結果](query-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="5a57c-131">To learn more about querying the results of your commands, see [Query command results with Azure 2.0](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="5a57c-132">Bash 命令</span><span class="sxs-lookup"><span data-stu-id="5a57c-132">Bash commands</span></span>

<span data-ttu-id="5a57c-133">您可以透過使用 `#[cmd]`，在不離開互動模式的情況下執行殼層命令。</span><span class="sxs-lookup"><span data-stu-id="5a57c-133">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="5a57c-134">範例</span><span class="sxs-lookup"><span data-stu-id="5a57c-134">Examples</span></span>

<span data-ttu-id="5a57c-135">有些命令有許多範例。</span><span class="sxs-lookup"><span data-stu-id="5a57c-135">Some commands have lots of examples.</span></span>
<span data-ttu-id="5a57c-136">使用 `CTRL-N` 即可捲動到下一個範例頁面，使用 `CTRL-Y` 即可捲動到上一頁。</span><span class="sxs-lookup"><span data-stu-id="5a57c-136">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![範例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="5a57c-138">您也可以使用 `::#` 來查看特定的範例。</span><span class="sxs-lookup"><span data-stu-id="5a57c-138">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
