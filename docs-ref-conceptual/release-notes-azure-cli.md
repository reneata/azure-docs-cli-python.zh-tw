---
title: "Azure CLI 2.0 版本資訊"
description: "深入了解 Azure CLI 2.0 的最新更新"
keywords: "Azure CLI 2.0, 版本資訊"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 56190b653ab9765017fffd1699056de7eae2db77
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: zh-TW
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 版本資訊

## <a name="april-3-2017"></a>2017 年 4 月 3 日

版本 2.0.2

在這一版中，我們發行了 ACR、Batch、KeyVault 和 SQL 元件。

```
azure-cli (2.0.2)
 
acr (2.0.0)
acs (2.0.2)
appservice (0.1.2)
batch (2.0.0)
cloud (2.0.0)
component (2.0.0)
configure (2.0.2)
container (0.1.2)
core (2.0.2)
documentdb (0.1.2)
feedback (2.0.0)
find (0.0.1b1)
iot (0.1.2)
keyvault (2.0.0)
lab (0.0.1)
monitor (0.0.1)
network (2.0.2)
nspkg (2.0.0)
profile (2.0.2)
redis (0.1.1b3)
resource (2.0.2)
role (2.0.1)
sql (2.0.0)
storage (2.0.2)
vm (2.0.2)
```

### <a name="core"></a>核心

* 將 ACR、實驗室、監視及尋找模組新增至預設清單。
* Login︰略過錯誤的租用戶 ([#2634](https://github.com/Azure/azure-cli/pull/2634))
* Login︰將預設訂用帳戶設定為具有「已啟用」狀態的訂用帳戶 ([#2575](https://github.com/Azure/azure-cli/pull/2575))
* 將 wait 命令和 --no-wait 支援新增至多個命令 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* Core︰支援使用憑證的服務主體登入 ([#2457](https://github.com/Azure/azure-cli/pull/2457))
* 新增遺漏範本參數的提示。 ([#2364](https://github.com/Azure/azure-cli/pull/2364))
* 支援設定諸如預設資源群組、預設 web、預設 VM 等常見引數的預設值
* 支援登入特定的租用戶
 
### <a name="acs"></a>ACS

* [ACS] 新增設定預設 ACS 叢集的支援 ([#2554](https://github.com/Azure/azure-cli/pull/2554))
* 新增 SSH 金鑰密碼提示的支援。 ([#2044](https://github.com/Azure/azure-cli/pull/2044))
* 新增 Windows 叢集的支援。 ([#2211](https://github.com/Azure/azure-cli/pull/2211))
* 將角色從擁有者切換為參與者。 ([#2321](https://github.com/Azure/azure-cli/pull/2321))
 
### <a name="appservice"></a>AppService

* appservice︰取得用於 DNS A 記錄之外部 IP 位址的支援 ([#2627](https://github.com/Azure/azure-cli/pull/2627))
* appservice︰支援繫結萬用字元憑證 ([#2625](https://github.com/Azure/azure-cli/pull/2625))
* appservice︰支援列出發行設定檔 ([#2504](https://github.com/Azure/azure-cli/pull/2504))
* AppService - 設定之後觸發原始檔控制同步處理 ([#2326](https://github.com/Azure/azure-cli/pull/2326))
 
### <a name="datalake"></a>DataLake

* Data Lake Analytics 模組的初始版本。
* Data Lake Store 模組的初始版本。
 
### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB︰新增列出連接字串的支援 ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>VM

* [Compute] 將 AppGateway 支援新增至虛擬機器擴展集建立 ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] 改良的磁碟快取支援 ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS︰併入入口網站所使用的認證驗證邏輯 ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* 新增 wait 命令和 --no-wait 支援 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* 虛擬機器擴展集︰支援 * 列出跨 VM 的執行個體檢視 ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* 新增 VM 和虛擬機器擴展集的 --祕密 ([#2212}(https://github.com/Azure/azure-cli/pull/2212))
* 可使用特殊的 VHD 來建立 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>2017 年 2 月 27 日

版本 2.0.0

此版本的 Azure CLI 2.0 是第一個「正式運作」版本。
正式運作適用於下列的命令模組︰
- Container Service (ACS)
- 計算 (包含 Resource Manager、VM、虛擬機器擴展集、受控磁碟)
- 網路功能
- 儲存體

這些命令模組可用在生產環境中，且受標準 Microsoft SLA 支援。
您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues)開啟問題。
您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。
您可以從包含 `az feedback` 命令的命令列提供意見反應。

這些模組中的命令很穩定，且不應該變更此版 Azure CLI 之未來版本的語法。

若要確認的 CLI 的版本，請使用 `az --version`。
輸出會列出 CLI 本身的版本 (此版本中為 2.0.0)、個別的命令模組，以及您所使用的 Python 和 GCC 版本。

```
azure-cli (2.0.0)

acs (2.0.0)
appservice (0.1.1b5)
batch (0.1.1b4)
cloud (2.0.0)
component (2.0.0)
configure (2.0.0)
container (0.1.1b4)
core (2.0.0)
documentdb (0.1.1b2)
feedback (2.0.0)
iot (0.1.1b3)
keyvault (0.1.1b5)
network (2.0.0)
nspkg (2.0.0)
profile (2.0.0)
redis (0.1.1b3)
resource (2.0.0)
role (2.0.0)
sql (0.1.1b5)
storage (2.0.0)
vm (2.0.0)
 
Python (Darwin) 2.7.10 (default, Jul 30 2016, 19:40:32) 
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]
```

> [!Note]
> 有些命令模組會有 "bn" 或 "rcn" 後置。
> 這些命令模組仍處於預覽狀態，且未來會正式運作。

我們也有 CLI 的夜間預覽組建。
如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。

您可以透過下列方式來報告夜間預覽組建的問題︰
- 在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues)中報告問題
- 連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。
- 從包含 `az feedback` 命令的命令列提供意見反應。

