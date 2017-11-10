---
title: "Azure CLI 2.0 延伸模組"
description: "使用 Azure CLI 2.0 延伸模組"
keywords: "Azure CLI, 延伸模組"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 930073324d68f9719ce5035388120e7b6ac41a98
ms.sourcegitcommit: 93f6bd2c199774fcb3b43c6b14d714196873ed04
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2017
---
# <a name="using-extensions-with-the-azure-cli-20"></a>使用 Azure CLI 2.0 延伸模組

延伸模組是個別的模組，並未隨附在 Azure CLI 中；可讓您以新增命令的方式來新增功能。 這些模組可能是實驗性或發行前提供的版本、Microsoft 專為您的需求設計的特定工具，或甚至是您自己撰寫的延伸模組。 延伸模組可提供搭配 CLI 使用的靈活性，可讓您依需求進行修改，無需使用與核心功能組不相關的其他套件。

本文會協助您了解如何安裝、更新及移除 CLI 延伸模組， 也會包含延伸模組行為的常見問題回答。

## <a name="finding-extensions"></a>尋找延伸模組

若要知道會提供哪些延伸模組，您可以使用 `az extension list-available`。 此命令會列出由 Microsoft 提供，可用且正式的延伸模組。

## <a name="installing-extensions"></a>安裝延伸模組

一旦找到要安裝延伸模組，請使用 `az extension add` 加以取得。 如果延伸模組是在 `az extension list-available` 中所列出的正式 Microsoft 延伸模組，您可以依名稱來安裝延伸模組。

```azurecli
az extension add --name <extension-name>
```

如果延伸模組是來自於外部資源，或者您擁有該延伸模組的直接連結，可以提供來源網址或本機路徑。 延伸模組_必須_是編譯過的 Python Whell 檔案。

```azurecli
az extension add --source <URL-or-path>
```

安裝延伸模組之後，便可以在 `$AZURE_EXTENSION_DIR` shell 變數的值下找到該延伸模組。 如果未設定這個變數，則 Linux 及 macOS 上的預設值為 `$HOME/.azure/cliextensions`，Windows 上的預設值為 `%USERPROFILE%\.azure\cliextensions`。

## <a name="updating-extensions"></a>更新延伸模組

延伸模組只能依名稱更新：

```azurecli
az extension update --name <extension-name>
```

如果 CLI 因為任何原因無法解析延伸模組名稱，請重新安裝延伸模組名稱並更新。 此外，也有可能是延伸模組被移出預覽，成為 CLI 內建命令。 在此情況下，更新 CLI，並解除安裝延伸模組。

## <a name="uninstalling-extensions"></a>解除安裝延伸模組

如果您不再需要延伸模組，可以使用 `az extension remove` 移除，

```azurecli
az extension remove --name <extension-name>
```

您也可以從安裝位置手動移除延伸模組。 這將會是 `$AZURE_EXTENSION_DIR` Shell 變數的值。 如果未設定這個變數，則 Linux 及 macOS 上的預設值為 `$HOME/.azure/cliextensions`，Windows 上的預設值為 `%USERPROFILE%\.azure\cliextensions`。

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

建議您使用 `az extension remove` 解除安裝。

## <a name="faq"></a>常見問題集

以下是一些 CLI 延伸模組的相關常見問題解答。

### <a name="what-file-formats-are-allowed-for-installation"></a>允許使用何種檔案格式安裝？

目前，只有編譯的 Python Whell 可以安裝為延伸模組。

### <a name="can-extensions-replace-existing-commands"></a>延伸模組可以取代現有的命令嗎？

是。 延伸模組可能會取代現有的命令，但在執行已取代 CLI 的命令之前，會發出警告。

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a>如何知道發行前版本中是否包括延伸模組？

如果發行前版本中包括延伸模組，則應該會在延伸模組的文件和版本控制中找到延伸模的記錄。 Microsoft 也可能會將 CLI 預覽命令發行為延伸模組，並規劃在產品通過預覽階段時，將這些延伸模組移至主要 CLI 介面。

### <a name="can-extensions-depend-upon-each-other"></a>延伸模組會彼此相依嗎？

否。 延伸模組必須是個別的套件，並不會彼此相依。 這是因為 CLI 不保證何時會載入延伸模組，因此無法保證會滿足相依性。 安裝延伸模組只會安裝該延伸模組，即使您移除其他延伸模組，該延伸模組應該仍然會繼續工作。

### <a name="are-extensions-updated-along-with-the-cli"></a>延伸模組會與 CLI 一併更新嗎？

否。 延伸模組必須個別進行更新，如[更新延伸模組](#updating-extensions)一節中所述。
