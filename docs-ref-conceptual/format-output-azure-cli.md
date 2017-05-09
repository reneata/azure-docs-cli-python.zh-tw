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
ms.openlocfilehash: de37b1ad6aa55c9ac73b5b6b89d9507c86cc1245
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: zh-TW
---
# <a name="output-formats-for-azure-cli-20-commands"></a>Azure CLI 2.0 命令的輸出格式

Azure CLI 2.0 會使用 json 作為其預設輸出選項，但會提供各種方式來設定任何命令的輸出格式。  使用 `--output` (或是 `--out` 或 `-o`) 參數，將命令的輸出格式設定為下表中所述的其中一個輸出類型。 

--output | 說明
---------|-------------------------------
`json`   | json 字串。 `json` 為預設值。
`jsonc`  | 以色彩標示的 json 字串。
`table`  | 包含資料行標題的資料表。
`tsv`    | 定位字元分隔值。

## <a name="using-the-json-option"></a>使用 json 選項

下列範例會以預設的 json 格式顯示訂用帳戶中的虛擬機器清單。

```azurecli
az vm list --output json
```

結果會這種格式顯示 (為保持簡潔，僅顯示部分輸出)。

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
 
## <a name="using-the-table-option"></a>使用資料表選項

資料表選項提供簡單的設定輸出集讀取方式，但請注意，不同於上述 json 範例，具有簡單 `--output table` 的輸出中不包含巢狀物件。  使用具有 'table' 輸出格式的相同範例來提供最常見屬性值的策劃清單。

```azurecli
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

您可以使用 `--query` 參數，以自訂您想要在此清單輸出中顯示的屬性和資料行。 下列範例會顯示如何在 `list` 命令中只選取 VM 名稱和資源群組名稱。

```azurecli
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

## <a name="using-the-tsv-option"></a>使用 tsv 選項

'tsv' 輸出格式會傳回以文字為基礎和定位字元分隔的簡單輸出，沒有標題及連字號。 此格式可讓您輕鬆地取用輸出至需要以某種形式處理文字的其他命令和工具。 使用先前具有 `tsv` 選項的範例，會將定位字元分隔的結果輸出。

```azurecli
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

下一個範例顯示如何將 `tsv` 輸出輸送到類似 `grep` 和 `cut` 的命令，以進一步將 `list` 輸出的特定值進行剖析。 `grep` 命令只會選取其中含有 "RGD" 文字的項目，而 `cut` 命令只會選取要在輸出中顯示的第八個欄位 (以定位字元分隔) 值。

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a>設定預設的輸出格式

您可以使用 `az configure` 命令來設定您的環境，或是建立如輸出格式的預設設定等喜好設定。 針對一般用途，最簡單的輸出格式預設值是使用「資料表」格式 - 當系統提示您輸出格式選項時，選取 **3**。 

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]: 
```