---
title: Azure CLI 2.0
description: "Azure CLI 2.0 的概觀。"
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
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 35e754b4ecd75481bd60d95dd1545b798c2e85b3
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/16/2017
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 是管理 Azure 資源的 Azure 新命令列體驗。  它可以用於 macOS、Linux 和 Windows。 

Azure CLI 2.0 已針對從命令列管理 Azure 資源進行最佳化，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。 使用 Azure CLI 2.0，您只要輕鬆輸入下列命令，就可以在 Azure 中建立 VM：

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

請檢閱[安裝文章](install-azure-cli.md)來讓 Azure CLI 2.0 在您的系統上啟動並執行，或使用 [Cloud Shell](/azure/cloud-shell/overview) 以在瀏覽器中執行 CLI。
閱讀[開始使用](get-started-with-azure-cli.md)文章來開始使用 CLI。
如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。

下列範例可協助您了解如何使用 Azure CLI 2.0 來執行常見案例：
- [Linux 虛擬機器](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows 虛擬機器](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

另提供詳細的[參考](/cli/azure/)，說明如何使用每個個別的 Azure CLI 2.0 命令。

立即[開始使用](get-started-with-azure-cli.md) Azure CLI 2.0。


> [!NOTE]
> 如果您使用舊版的 CLI (Azure CLI)，可以繼續使用。
> 如果您同時使用這兩個 CLI，請記住，`azure` 是舊的 CLI - Azure CLI，而 `az` 是新的 CLI - Azure CLI 2.0。 