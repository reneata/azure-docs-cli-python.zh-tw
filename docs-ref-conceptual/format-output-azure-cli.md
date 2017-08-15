---
title: "Azure CLI 2.0 的輸出格式"
description: "使用 --output 將 Azure CLI 2.0 命令的輸出設定為資料表、清單或 json 格式。"
keywords: "Azure CLI 2.0, 輸出, 格式, 資料表, 清單, json, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 74bdb727-481d-45f7-a44e-15d18dc55483
ms.openlocfilehash: d1440cc1e99ccddb18d23306cc0fcdb4b8babf14
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2017
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="83909-104">Azure CLI 2.0 命令的輸出格式</span><span class="sxs-lookup"><span data-stu-id="83909-104">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="83909-105">Azure CLI 2.0 會使用 json 作為其預設輸出選項，但會提供各種方式來設定任何命令的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="83909-105">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="83909-106">使用 `--output` (或是 `--out` 或 `-o`) 參數，將命令的輸出格式設定為下表中所述的其中一個輸出類型。</span><span class="sxs-lookup"><span data-stu-id="83909-106">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table.</span></span> 

<span data-ttu-id="83909-107">--output</span><span class="sxs-lookup"><span data-stu-id="83909-107">--output</span></span> | <span data-ttu-id="83909-108">說明</span><span class="sxs-lookup"><span data-stu-id="83909-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="83909-109">json 字串。</span><span class="sxs-lookup"><span data-stu-id="83909-109">json string.</span></span> <span data-ttu-id="83909-110">`json` 為預設值。</span><span class="sxs-lookup"><span data-stu-id="83909-110">`json` is the default.</span></span>
`jsonc`  | <span data-ttu-id="83909-111">以色彩標示的 json 字串。</span><span class="sxs-lookup"><span data-stu-id="83909-111">colorized json string.</span></span>
`table`  | <span data-ttu-id="83909-112">包含資料行標題的資料表。</span><span class="sxs-lookup"><span data-stu-id="83909-112">table with column headings.</span></span>
`tsv`    | <span data-ttu-id="83909-113">定位字元分隔值。</span><span class="sxs-lookup"><span data-stu-id="83909-113">tab-separated values.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a><span data-ttu-id="83909-114">使用 json 選項</span><span class="sxs-lookup"><span data-stu-id="83909-114">Using the json option</span></span>

<span data-ttu-id="83909-115">下列範例會以預設的 json 格式顯示訂用帳戶中的虛擬機器清單。</span><span class="sxs-lookup"><span data-stu-id="83909-115">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="83909-116">結果會這種格式顯示 (為保持簡潔，僅顯示部分輸出)。</span><span class="sxs-lookup"><span data-stu-id="83909-116">The results are in this form (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "demorg1"
        }
      ]
    },
          ...
          ...
          ...   
]
```
 
## <a name="using-the-table-option"></a><span data-ttu-id="83909-117">使用資料表選項</span><span class="sxs-lookup"><span data-stu-id="83909-117">Using the table option</span></span>

<span data-ttu-id="83909-118">資料表選項提供簡單的設定輸出集讀取方式，但請注意，不同於上述 json 範例，具有簡單 `--output table` 的輸出中不包含巢狀物件。</span><span class="sxs-lookup"><span data-stu-id="83909-118">The table option provides an easy to read set of output, but note that nested objects are not included in the output with the simple `--output table`, unlike the preceding .json example.</span></span>  <span data-ttu-id="83909-119">使用具有 'table' 輸出格式的相同範例來提供最常見屬性值的策劃清單。</span><span class="sxs-lookup"><span data-stu-id="83909-119">Using the same example with 'table' output format provides a curated list of most common property values.</span></span>

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

<span data-ttu-id="83909-120">您可以使用 `--query` 參數，以自訂您想要在此清單輸出中顯示的屬性和資料行。</span><span class="sxs-lookup"><span data-stu-id="83909-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="83909-121">下列範例會顯示如何在 `list` 命令中只選取 VM 名稱和資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="83909-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli-interactive
az vm list --query "[].{ resource: resourceGroup, name: name }" -o table
```

```
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

## <a name="using-the-tsv-option"></a><span data-ttu-id="83909-122">使用 tsv 選項</span><span class="sxs-lookup"><span data-stu-id="83909-122">Using the tsv option</span></span>

<span data-ttu-id="83909-123">'tsv' 輸出格式會傳回以文字為基礎和定位字元分隔的簡單輸出，沒有標題及連字號。</span><span class="sxs-lookup"><span data-stu-id="83909-123">'tsv' output format returns a simple text-based and tab-separated output with no headings and dashes.</span></span> <span data-ttu-id="83909-124">此格式可讓您輕鬆地取用輸出至需要以某種形式處理文字的其他命令和工具。</span><span class="sxs-lookup"><span data-stu-id="83909-124">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="83909-125">使用先前具有 `tsv` 選項的範例，會將定位字元分隔的結果輸出。</span><span class="sxs-lookup"><span data-stu-id="83909-125">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="83909-126">下一個範例顯示如何將 `tsv` 輸出輸送到類似 `grep` 和 `cut` 的命令，以進一步將 `list` 輸出的特定值進行剖析。</span><span class="sxs-lookup"><span data-stu-id="83909-126">The next example shows how the `tsv` output can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="83909-127">`grep` 命令只會選取其中含有 "RGD" 文字的項目，而 `cut` 命令只會選取要在輸出中顯示的第八個欄位 (以定位字元分隔) 值。</span><span class="sxs-lookup"><span data-stu-id="83909-127">The `grep` command selects only items that have text "RGD" in them and then the `cut` command selects only the eighth field (separated by tabs) value to show in the output.</span></span>

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a><span data-ttu-id="83909-128">設定預設的輸出格式</span><span class="sxs-lookup"><span data-stu-id="83909-128">Setting the default output format</span></span>

<span data-ttu-id="83909-129">您可以使用 `az configure` 命令來設定您的環境，或是建立如輸出格式的預設設定等喜好設定。</span><span class="sxs-lookup"><span data-stu-id="83909-129">You can use the `az configure` command to set up your environment or establish preferences such as default settings for output formats.</span></span> <span data-ttu-id="83909-130">針對一般用途，最簡單的輸出格式預設值是使用「資料表」格式 - 當系統提示您輸出格式選項時，選取 **3**。</span><span class="sxs-lookup"><span data-stu-id="83909-130">For common use, the easiest output format default is the "table" format - select **3** when prompted for output format choices.</span></span> 

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]: 
```