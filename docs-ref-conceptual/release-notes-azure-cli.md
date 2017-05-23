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
ms.openlocfilehash: 3bd4b9c059da3b841fc0757a11bc7ce78ec64b08
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 版本資訊

## <a name="may-10-2017"></a>2017 年 5 月 10 日

版本 2.0.6

* documentdb 已重新命名為 cosmosdb
* 新增 rdbms (mysql、postgres)
* 包含 Data Lake Analytics 和 Data Lake Store 模組。
* 包含「辨識服務」模組。
* 包含 Service Fabric 模組。
* 包含「互動式」模組 (az-shell 的重新命名)。
* 新增對 CDN 命令的支援。
* 移除「容器」模組。
* 新增 'az -v' 作為 'az --version' 的捷徑 ([#2926 (英文)](https://github.com/Azure/azure-cli/issues/2926))
* 提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))

```
azure-cli (2.0.6)

acr (2.0.4)
acs (2.0.6)
appservice (0.1.6)
batch (2.0.4)
cdn (0.0.2)
cloud (2.0.2)
cognitiveservices (0.1.2)
command-modules-nspkg (2.0.0)
component (2.0.4)
configure (2.0.6)
core (2.0.6)
cosmosdb (0.1.6)
dla (0.0.6)
dls (0.0.6)
feedback (2.0.2)
find (0.2.2)
interactive (0.3.1)
iot (0.1.5)
keyvault (2.0.4)
lab (0.0.4)
monitor (0.0.4)
network (2.0.6)
nspkg (3.0.0)
profile (2.0.4)
rdbms (0.0.1)
redis (0.2.3)
resource (2.0.6)
role (2.0.4)
sf (1.0.1)
sql (2.0.3)
storage (2.0.6)
vm (2.0.6)
```

### <a name="core"></a>核心

* 核心：捕捉未註冊提供者所造成的例外狀況，並自動註冊該提供者   
* 效能：將 adal 權杖快取保存在記憶體中，直到程序結束為止 ([#2603 (英文)](https://github.com/Azure/azure-cli/issues/2603))
* 修正從十六進位指紋 -o tsv 傳回的位元組 ([#3053 (英文)](https://github.com/Azure/azure-cli/issues/3053))
* 增強 Key Vault 憑證下載和 AAD SP 的整合 ([#3003 (英文)](https://github.com/Azure/azure-cli/issues/3003))
* 在 ‘az —version’ 中新增 Python 位置 ([#2986 (英文)](https://github.com/Azure/azure-cli/issues/2986))
* 登入：支援在沒有訂用帳戶時進行登入 ([#2929 (英文)](https://github.com/Azure/azure-cli/issues/2929))
* 核心：修正使用服務主體登入兩次時所發生的失敗 ([#2800 (英文)](https://github.com/Azure/azure-cli/issues/2800))
* 核心：允許透過環境變數設定 accessTokens.json 的檔案路徑 ([#2605 (英文)](https://github.com/Azure/azure-cli/issues/2605))
* 核心：允許將已設定的預設值套用到選擇性引數 ([#2703 (英文)](https://github.com/Azure/azure-cli/issues/2703))
* 核心：提升效能
* 核心：自訂 CA 憑證 - 支援設定 REQUESTS_CA_BUNDLE 環境變數
* 核心：雲端組態 - 如果未設定「管理」端點，則使用「資源管理員」端點

### <a name="acs"></a>ACS

* 將主要和代理程式計數修正為整數，而不是字串
* 公開 'az acs create --no-wait' 和 'az acs wait' 以進行非同步建立
* 公開 'az acs create --validate' 以進行試執行驗證
* 在進行 scale 命令的 PUT 呼叫之前，先移除 Windows 設定檔 ([#2755 (英文)](https://github.com/Azure/azure-cli/issues/2755))

### <a name="appservice"></a>AppService

* functionapp：新增完整的 functionapp 支援，包括 create、show、list、delete、hostname、ssl 等
* 新增 Team Services (vsts) 作為 "appservice web source-control config" 的持續傳遞選項
* 建立 "az webapp" 以取代 "az appservice web" (用於回溯相容性，"az appservice web" 的存續期將再延續 2 個版本)
* 公開引數以在執行 webapp create 時設定部署和「執行階段堆疊」
* 公開 "webapp list-runtimes"
* 支援設定連接字串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))
* 支援附帶預覽功能的位置交換
* 修飾來自 appservice 命令的錯誤 ([#2948 (英文)](https://github.com/Azure/azure-cli/issues/2948))
* 使用 App Service 方案的資源群組來進行憑證作業 ([#2750 (英文)](https://github.com/Azure/azure-cli/issues/2750))

### <a name="cosmosdb"></a>CosmosDB

* 將 documentdb 模組重新命名為 cosmosdb。
* 新增對 documentdb 資料層 API 的支援：資料庫和集合管理
* 新增對在資料庫帳戶上啟用自動容錯移轉的支援
* 新增對新一致性原則 ConsistentPrefix 的支援

### <a name="data-lake-analytics"></a>Data Lake Analytics

* 修正依工作清單的結果和狀態篩選會導致擲回錯誤的 Bug。
* 新增對下列新類別目錄項目類型的支援：套件。 透過 `az dla catalog package` 進行存取
* 能夠從資料庫內列出下列類別目錄項目 (不需指定結構描述)：

  * 資料表
  * 資料表值函式
  * 檢視
  * 資料表統計資料。 這也可以使用結構描述來列出，但不需要指定資料表名稱。

### <a name="data-lake-store"></a>Data Lake Store

* 更新基礎檔案系統 SDK 的版本，以提供更佳的支援來處理伺服器端節流情況。
* 提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))
* 遺失 access show 的說明。 將新增此說明。 ([#2743 (英文)](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>尋找

* 改善搜尋結果，並允許進行搜尋索引版本控制

### <a name="keyvault"></a>KeyVault

* BC：`az keyvault certificate download`將 -e 從字串或二進位變更為 PEM 或 DER，來以更佳的方式代表選項
* BC：從 `keyvault certificate create` 中移除 --expires 和 --not-before，因為服務不支援這些參數。
* 在 `keyvault certificate create` 中新增 --validity 參數，以選擇性地覆寫 --policy 中的值
* 修正 `keyvault certificate get-default-policy` 中公開 'expires' 和 'not_before' 但未公開 'validity_in_months' 的問題。
* 用於匯入 pem 和 pfx 的 keyvault 修正 ([#2754 (英文)](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>實驗室

* 新增適用於實驗室中環境的 create、show、delete 及 list 命令。
* 新增 show 和 list 命令以檢視實驗室中的 ARM 範本。
* 在 `az lab vm list` 中新增 --environment 旗標，以在實驗室中依環境篩選 VM。
* 新增便利命令 `az lab formula export-artifacts` 以匯出實驗室公式內的構件結構。
* 新增命令以管理實驗室內的密碼。

### <a name="monitor"></a>監視

* Bug 修正：建立 `az alert-rules create` 的 `--actions` 模型以取用 JSON 字串 ([#3009 (英文)](https://github.com/Azure/azure-cli/issues/3009))
* Bug 修正：diagnostic-settings create 不接受來自 show 命令的記錄/計量 ([#2913 (英文)](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>網路

* 新增 `network watcher test-connectivity` 命令。
* 新增對 `network watcher packet-capture create` 之 `--filters` 參數的支援。
* 新增對「應用程式閘道」連線清空的支援。
* 新增對「應用程式閘道」WAF 規則集組態的支援。
* 新增對 ExpressRoute 路由篩選和規則的支援。
* 新增對 TrafficManager 地理路由的支援。
* 新增對 VPN 連線原則型流量選取器的支援。
* 新增對 VPN 連線 IPSec 原則的支援。
* 修正 `vpn-connection create` 搭配使用 `--no-wait` 或 `--validate` 參數時的 Bug。
* 新增對「主動-主動」VNet 閘道的支援
* 從 `network vpn-connection list/show` 命令移除 Null 值。
* BC：修正 `vpn-connection create` 之輸出中的 Bug 
* 修正未正確剖析 'vpn-connection create' 之 '--key-length' 引數的 Bug。
* 修正 `dns zone import` 中未正確匯入記錄的 Bug。
* 修正 `traffic-manager endpoint update` 無法運作的 Bug。
* 新增 'network watcher' 預覽命令。

### <a name="profile"></a>設定檔

* 支援在找不到訂用帳戶時進行登入 ([#2560 (英文)](https://github.com/Azure/azure-cli/issues/2560))
* 在 az account set --subscription 中支援短參數名稱 ([#2980 (英文)](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* 新增 update 命令，這也會為 redis 快取新增調整能力
* 取代 'update-settings' 命令。

### <a name="resource"></a>資源

* 新增 managedapp 和 managedapp definition 命令 ([#2985 (英文)](https://github.com/Azure/azure-cli/issues/2985))
* 支援 'provider operation' 命令 ([#2908 (英文)](https://github.com/Azure/azure-cli/issues/2908))
* 支援一般 resource create ([#2606 (英文)](https://github.com/Azure/azure-cli/issues/2606))
* 修正資源剖析和 api 版本查詢。 ([#2781 (英文)](https://github.com/Azure/azure-cli/issues/2781))
* 新增 az lock update 的文件。 ([#2702 (英文)](https://github.com/Azure/azure-cli/issues/2702))
* 如果您嘗試列出不存在之群組的資源，就會發生錯誤。 ([#2769 (英文)](https://github.com/Azure/azure-cli/issues/2769))
* [計算] 修正 VMSS 和 VM 可用性設定組更新的相關問題。 ([#2773 (英文)](https://github.com/Azure/azure-cli/issues/2773))
* 修正 parent-resource-path 為 None 時的 lock create 和 delete ([#2742 (英文)](https://github.com/Azure/azure-cli/issues/2742))

### <a name="role"></a>角色

* create-for-rbac：確保 SP 的結束日期不會超過憑證的到期日 ([#2989 (英文)](https://github.com/Azure/azure-cli/issues/2989))
* RBAC：新增對 'ad group' 的完整支援 ([#2016 (英文)](https://github.com/Azure/azure-cli/issues/2016))
* 角色：修正 role definition update 上的問題 ([#2745 (英文)](https://github.com/Azure/azure-cli/issues/2745))
* create-for-rbac：確保系統會挑選使用者提供的密碼

### <a name="sql"></a>SQL

* 新增 az sql server list-usages 和 az sql db list-usages 命令。
* SQL - 能夠直接連接到資源提供者 ([#2832 (英文)](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>儲存體

* `storage account create` 之資源群組位置的預設位置。
* 新增對遞增 blob 複製的支援
* 新增對大型區塊 blob 上傳的支援
* 當要上傳的檔案大於 200 GB 時，將區塊大小變更為 100 MB

### <a name="vm"></a>VM

* avail-set：將 UD&FD 網域計數設定為選用

  注意：主權雲端中的 VM 命令。請避免使用受管理磁碟相關的功能，包括下列功能：
  1. az disk/snapshot/image
  2. az vm/vmss disk
  3. 在 "az vm/vmss create" 內，請使用 "—use-unmanaged-disk" 來避免使用受管理的磁碟。其他命令應該可運作
* vm/vmss：改進產生 SSH 金鑰組時的警告文字
* vm/vmss：支援從需要方案資訊的市場映像進行建立 ([#1209 (英文)](https://github.com/Azure/azure-cli/issues/1209))


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
您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)開啟問題。
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
> 些命令模組會有 "b*n*" 或 "rc*n*" 後置詞。
> 這些命令模組仍處於預覽狀態，且未來會正式運作。

我們也有 CLI 的夜間預覽組建。
如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。

您可以透過下列方式來報告夜間預覽組建的問題︰
- 在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)中報告問題
- 連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。
- 從包含 `az feedback` 命令的命令列提供意見反應。

