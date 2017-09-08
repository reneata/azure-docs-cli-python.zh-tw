---
title: "使用 Azure CLI 2.0 查詢命令結果"
description: "使用 --query 在 Azure CLI 2.0 命令的輸出上執行 JMESPath 查詢。"
keywords: "Azure CLI 2.0, JMESPath, 查詢, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 5979acc5-21a5-41e2-a4b6-3183bfe6aa22
ms.openlocfilehash: e0eee9eb9e0a9f136ff076d064ce802f76bc8e3d
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="11579-104">搭配使用 JMESPath 查詢與 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="11579-104">Using JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="11579-105">Azure CLI 2.0 會使用 `--query` 參數，在您 `az` 命令的結果執行 [JMESPath 查詢](http://jmespath.org)。</span><span class="sxs-lookup"><span data-stu-id="11579-105">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="11579-106">JMESPath 是 JSON 輸出功能強大的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="11579-106">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="11579-107">如果您不熟悉 JMESPath 查詢，可以在 [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html) 找到教學課程。</span><span class="sxs-lookup"><span data-stu-id="11579-107">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="11579-108">Azure CLI 2.0 內的每種資源類型 (Container Service、Web Apps、VM 等等) 都支援 `Query` 參數，且此參數可用於各種不同的用途。</span><span class="sxs-lookup"><span data-stu-id="11579-108">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="11579-109">我們在下方列出了數個範例。</span><span class="sxs-lookup"><span data-stu-id="11579-109">We have listed several examples below.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="11579-110">選取簡單屬性</span><span class="sxs-lookup"><span data-stu-id="11579-110">Selecting simple properties</span></span>

<span data-ttu-id="11579-111">具有 `table` 輸出格式的簡單 `list` 命令會以易於閱讀的表格格式，將每個資源類型最常見、簡單屬性的策劃集傳回。</span><span class="sxs-lookup"><span data-stu-id="11579-111">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

```azurecli-interactive
az vm list --out table
```

```
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

<span data-ttu-id="11579-112">您可以使用 `--query` 參數，只顯示訂用帳戶中所有虛擬機器的資源群組名稱和 VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="11579-112">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query [*].[name,resourceGroup] --out table
```

```
Column1     Column2
---------   -----------
DemoVM010   DEMORG1
demovm111   DEMORG1
demovm211   DEMORG1
demovm212   DEMORG1
demovm213   DEMORG1
demovm214   DEMORG1
demovm222   DEMORG1
KBDemo001VM RGDEMO001
KBDemo020   RGDEMO001
```

<span data-ttu-id="11579-113">在上述範例中，您會注意到資料行標題為 "Column1" 和 "Column2"。</span><span class="sxs-lookup"><span data-stu-id="11579-113">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="11579-114">您也可以將好記的標籤或名稱新增到您選取的內容。</span><span class="sxs-lookup"><span data-stu-id="11579-114">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="11579-115">在下列範例中，我們已將 "VMName" 和 "RGName" 標籤新增到選取的 "name" 和 "resourceGroup" 屬性。</span><span class="sxs-lookup"><span data-stu-id="11579-115">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


```azurecli-interactive
az vm list \
  --query "[].{RGName:resourceGroup, VMName:name}" --out table
```

```
RGName     VMName
---------  -----------
DEMORG1    DemoVM010
DEMORG1    demovm111
DEMORG1    demovm211
DEMORG1    demovm212
DEMORG1    demovm213
DEMORG1    demovm214
DEMORG1    demovm222
RGDEMO001  KBDemo001VM
RGDEMO001  KBDemo020
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="11579-116">選取複雜的巢狀屬性</span><span class="sxs-lookup"><span data-stu-id="11579-116">Selecting complex nested properties</span></span>

<span data-ttu-id="11579-117">如果您想要選取的屬性在 JSON 輸出中為深入巢狀，您必須將完整路徑提供給該巢狀屬性。</span><span class="sxs-lookup"><span data-stu-id="11579-117">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="11579-118">下列範例顯示如何從 VM list 命令選取 VMName 和 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="11579-118">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

```azurecli-interactive
az vm list \
  --query "[].{VMName:name,OSType:storageProfile.osDisk.osType}" --out table
```

```
VMName       OSType
-----------  --------
DemoVM010    Linux
demovm111    Linux
demovm211    Linux
demovm212    Linux
demovm213    Linux
demovm214    Linux
demovm222    Linux
KBDemo001VM  Linux
KBDemo020    Linux
```

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="11579-119">使用 contains 函式進行篩選</span><span class="sxs-lookup"><span data-stu-id="11579-119">Filter with the contains function</span></span>

<span data-ttu-id="11579-120">您可以使用 JMESPath `contains` 函式來限定查詢中傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="11579-120">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="11579-121">在下列範例中，命令只會選取名稱中具有 "RGD" 文字的 VM。</span><span class="sxs-lookup"><span data-stu-id="11579-121">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>  

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup,'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

<span data-ttu-id="11579-122">下一個範例中，結果會傳回具有 vmSize 'Standard_DS1' 的 VM。</span><span class="sxs-lookup"><span data-stu-id="11579-122">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

```azurecli-interactive
az vm list \
  --query "[?contains(hardwareProfile.vmSize, 'Standard_DS1')]" --out table
```

```
ResourceGroup    VMName     VmId                                  Location    ProvisioningState
---------------  ---------  ------------------------------------  ----------  -------------------
DEMORG1          DemoVM010  cbd56d9b-9340-44bc-a722-25f15b578444  westus      Succeeded
DEMORG1          demovm111  c1c024eb-3837-4075-9117-bfbc212fa7da  westus      Succeeded
DEMORG1          demovm211  95eda642-417f-4036-9475-67246ac0f0d0  westus      Succeeded
DEMORG1          demovm212  4bdac85d-c2f7-410f-9907-ca7921d930b4  westus      Succeeded
DEMORG1          demovm213  2131c664-221a-4b7f-9653-f6d542fbfa34  westus      Succeeded
DEMORG1          demovm214  48f419af-d27a-4df0-87f3-9481007c2e5a  westus      Succeeded
DEMORG1          demovm222  e0f59516-1d69-4d54-b8a2-f6c4a5d031de  westus      Succeeded
```

## <a name="filter-with-grep"></a><span data-ttu-id="11579-123">使用 grep 進行篩選</span><span class="sxs-lookup"><span data-stu-id="11579-123">Filter with grep</span></span>

<span data-ttu-id="11579-124">`tsv` 輸出格式是沒有標頭的定位字元分隔文字。</span><span class="sxs-lookup"><span data-stu-id="11579-124">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="11579-125">它可輸送到類似 `grep` 和 `cut` 的命令，以進一步將 `list` 輸出的特定值進行剖析。</span><span class="sxs-lookup"><span data-stu-id="11579-125">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="11579-126">在下列範例中，`grep` 命令只會選取名稱中具有 "RGD" 文字的 VM。</span><span class="sxs-lookup"><span data-stu-id="11579-126">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="11579-127">`cut` 命令只會選取要在輸出中顯示的第 8 個欄位 (以定位字元分隔) 值。</span><span class="sxs-lookup"><span data-stu-id="11579-127">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="11579-128">使用 jpterm 進行探索</span><span class="sxs-lookup"><span data-stu-id="11579-128">Explore with jpterm</span></span>

<span data-ttu-id="11579-129">您也可以將命令輸出輸送到 [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal)，並在那裡實驗您的 JMESPath 查詢。</span><span class="sxs-lookup"><span data-stu-id="11579-129">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

