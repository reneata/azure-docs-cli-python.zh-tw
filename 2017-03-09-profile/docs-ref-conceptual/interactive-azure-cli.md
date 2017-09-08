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
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="interactive-azure-cli-20"></a>互動式 Azure CLI 2.0

您可以透過執行 `az interactive` 命令，在互動模式下使用 Azure CLI 2.0。
這會讓您處於互動式殼層中，其中會自動完成命令，而且您可以存取命令及其參數的描述和命令範例。

![互動模式](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> 在這裡，我們並未使用預設樣式，因為在黑色背景上閱讀效果不佳。

如果您尚未登入帳戶，請使用 `login` 命令來登入。

## <a name="configure"></a>設定

互動模式會依選擇顯示命令描述、參數描述及命令範例。
您可以使用 `F1` 來開啟或關閉描述和範例。

![描述和範例](./media/interactive-azure-cli/descriptions-and-examples.png)

您可以使用 `F2` 來開啟或關閉參數預設值的顯示。

![預設值](./media/interactive-azure-cli/defaults.png)

`F3` 可開關一些按鍵的摘要說明。

![摘要說明](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a>Scope

您可以將互動模式的範圍限定在特定的命令群組，例如 `vm` 或 `vm image`。
當您這麼做時，就會在該範圍中解譯所有命令。
如果您要在該命令群組中執行所有工作，這是省略命令的絕佳方式。

您可以不輸入下列命令：

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

而是將範圍限定為 vm 命令群組，然後輸入下列命令：

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

您也可以將範圍設定為較低層級的命令群組。
您可以使用 `%%vm image` 將範圍限定為 `vm image`。
在此案例中，由於我們已經將範圍限定為 `vm`，因此我們會使用 `%%image`。

```azurecli
az vm>> %%image
az vm image>>
```

屆時，我們可以使用 `%%..` 將範圍提升回 `vm`，或是就使用 `%%` 將範圍限定為根目錄。

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a>查詢

您可以對所執行之上一個命令的結果執行 JMESPath 查詢。
例如，在建立 VM 之後，您可以確認它是否已完整佈建。

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

若要深入了解如何查詢命令的結果，請參閱[使用 Azure 2.0 來查詢命令結果](query-azure-cli.md)。

## <a name="bash-commands"></a>Bash 命令

您可以透過使用 `#[cmd]`，在不離開互動模式的情況下執行殼層命令。

```azurecli
az>> #dir
```

## <a name="examples"></a>範例

有些命令有許多範例。
使用 `CTRL-N` 即可捲動到下一個範例頁面，使用 `CTRL-Y` 即可捲動到上一頁。

![範例](./media/interactive-azure-cli/examples.png)

您也可以使用 `::#` 來查看特定的範例。

```azurecli
az>> vm create ::8
```
