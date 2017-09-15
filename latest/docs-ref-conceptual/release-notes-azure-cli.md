---
title: "Azure CLI 2.0 版本資訊"
description: "深入了解 Azure CLI 2.0 的最新更新"
keywords: "Azure CLI 2.0, 版本資訊"
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: ad30efeb7efafcc5816160ee130665d37adb62c6
ms.sourcegitcommit: e866977985ba0286fa05f41729dd7e7d9ce86f8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/13/2017
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 版本資訊

## <a name="september-11-2017"></a>2017 年 9 月 11 日

版本 2.0.17

### <a name="core"></a>核心

* 啟用命令模組以在遙測中設定自己的相互關聯識別碼
* 修正當遙測設為診斷模式時的 JSON 傾印問題

### <a name="acs"></a>ACS

* 已新增 `acs list-locations` 命令
* 讓 `ssh-key-file` 隨附預期的預設值

### <a name="appservice"></a>AppService

* 新增在資源群組中建立 Web 應用程式，而非在作用中服務計劃中建立 Web 應用程式的功能

### <a name="cdn"></a>CDN

* 修正 `cdn custom-domain create` 的「CustomDomain 無法互動」錯誤。

### <a name="extension"></a>分機

* 初始版本。

### <a name="keyvault"></a>Keyvault

* 修正對 `keyvault set-policy` 的權限區分大小寫的問題。

### <a name="network"></a>網路

* 已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`
* 己針對 `vnet subnet create/update` 將 `--private-access-services` 引數重新命名為 `--service-endpoints`
* 已將多個 IP 和連接埠範圍的支援新增至 `nsg rule create/update`
* 已將 SKU 的支援新增至 `lb create`
* 已將 SKU 的支援新增至 `public-ip create`

### <a name="resource"></a>資源

* 允許在 `policy definition create` 及 `policy definition update` 中傳送資源原則參數定義
* 允許為 `policy assignment create` 傳送參數值
* 允許為所有參數傳送 JSON 或檔案
* 遞增的 API 版本

### <a name="sql"></a>SQL

* 已新增 `sql server vnet-rule` 命令

### <a name="vm"></a>VM

* 已修正：在提供 `--scope` 之前不指派存取權
* 已修正：使用相同延伸模組命名作為入口網站
* 已從 `[vm|vmss] create` 輸出移除 `subscription`
* 已修正：`[vm|vmss] create` 儲存體 SKU 不會套用至搭配映像的資料磁碟
* 已修正：`vm format-secret --secrets` 不會接受新行分隔識別碼

## <a name="august-31-2017"></a>2017 年 8 月 31 日

版本 2.0.16

### <a name="keyvault"></a>Keyvault

* 修正試著自動使用 `secret download` 解析祕密編碼時發生錯誤的問題

### <a name="sf"></a>Sf

* 取代所有命令，以利於 Service Fabric CLI (sfctl)

### <a name="storage"></a>儲存體

* 修正無法在不支援 NetworkACL 功能的區域中建立儲存體帳戶的問題
* 若指定內容類型和內容編碼，則判斷 Blob 及檔案上傳期間的內容類型及內容編碼

## <a name="august-28-2017"></a>2017 年 8 月 28 日

版本 2.0.15

### <a name="cli"></a>CLI

* 已將法律注意事項新增至 `--version`。

### <a name="acs"></a>ACS

* 已更正預覽區域。
* 已正確格式化預設 `dns_name_prefix`。
* 最佳化的 acs 命令輸出。

### <a name="appservice"></a>AppService

* [新變更] 已修正 `az webapp config appsettings [delete|set]` 輸出中的不一致
* 已針對 `az webapp config container set --docker-custom-image-name` 新增 `-i` 的新別名
* 已公開 `az webapp log show`
* 已公開 `az webapp delete` 中的新引數，可保留應用程式服務計劃、計量或 DNS 註冊
* 已修正：正確偵測到位置設定

### <a name="iot"></a>IoT

* 已修正 #3934：建立原則時無法再清除現有的原則

### <a name="network"></a>網路

* [新變更] 已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`
* [新變更] 已將 `--private-access-services` 選項重新命名為適用於 `vnet subnet [create|update]` 的 `--service-endpoints`
* 已將多個 IP 和連接埠範圍的支援新增至 `nsg rule [create|update]`
* 已將 SKU 的支援新增至 `lb create`
* 已將 SKU 的支援新增至 `public-ip create`

### <a name="profile"></a>設定檔

* 已公開 `--msi` 和 `--msi-port`，可使用虛擬機器的身分識別登入

### <a name="service-fabric"></a>Service Fabric

* 預覽版本
* 簡化的登錄使用者/命令的密碼規則
* 已修正使用者即使在參數中傳遞之後的密碼提示
* 已新增空白 `registry_cred` 的支援

### <a name="storage"></a>儲存體

* 已啟用設定 blob 層
* 已將 `--bypass` 和 `--default-action` 引數新增至 `storage account [create|update]` 以支援服務通道
* 新增的命令可將 VNET 規則和以 IP 作為基礎的規則新增至 `storage account network-rule`  
* 透過客戶管理的金鑰啟用服務加密
* [新變更] 已將 `--encryption` 選項重新命名為適用於 `az storage account create and az storage account update` 命令的 `--encryption-services`
* 已修正 #4220：`az storage account update encryption` - 語法不相符

### <a name="vm"></a>VM

* 已修正使用 `--instance-id *` 時會顯示 `vmss get-instance-view` 的額外錯誤資訊的錯誤
* 已將 `--lb-sku` 的支援新增至 `vmss create`： 
* 從 `[vm|vmss] create` 的系統管理員名稱封鎖清單移除人力名稱 
* 已修正在無法從映像擷取計劃資訊時，`[vm|vmss] create` 會擲回錯誤的問題
* 已修正使用內部 LB 建立 vmms scaleset 時的損毀
* 已修正 `--no-wait` 引數無法與 `vm availability-set create` 搭配使用的問題


## <a name="august-15-2017"></a>2017 年 8 月 15 日

版本 2.0.14

### <a name="acs"></a>ACS

* 已更正 kubernetes 的 sshMaster0 連接埠號碼

### <a name="appservice"></a>AppService

* 已修正建立以新 git 作為基礎的 Linux WebApp 時的例外狀況

### <a name="event-grid"></a>Event Grid

* 已新增 SDK 相依性

## <a name="august-11-2017"></a>2017 年 8 月 11 日

版本 2.0.13

### <a name="acs"></a>ACS

* 新增更多預覽區域

### <a name="batch"></a>批次

* 更新為 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0
* 已新增新的命令顯示作業的工作計數
* 已修正資源檔案 SAS URL 處理中的錯誤
* Batch 帳戶端點現在支援選擇性的 'https://' 前置詞
* 支援將超過 100 個工作的清單新增至作業
* 已新增載入擴充功能命令模組的偵錯記錄

### <a name="component"></a>元件

* 已新增對 'az component' 命令的取代警告

### <a name="container"></a>容器

* `create`：已修正環境變數內不允許等號的問題


### <a name="data-lake-store"></a>資料湖存放區

* 已啟用進度控制項

### <a name="event-grid"></a>Event Grid

* 初始版本

### <a name="network"></a>網路

* `lb`：已修正省略某些子資源名稱時未正確解析的問題
* `application-gateway {subresource} delete`：已修正無法接受 `--no-wait` 的問題
* `application-gateway http-settings update`：已修正無法關閉 `--connection-draining-timeout` 的問題
* 已修正非預期關鍵字引數 `sa_data_size_kilobyes` 與 `az network vpn-connection ipsec-policy add` 的錯誤

### <a name="profile"></a>設定檔

* `account list`：已新增 `--refresh`，可從伺服器同步處理最新的訂用帳戶

### <a name="storage"></a>儲存體

* 使用指派身分識別的系統來啟用更新儲存體帳戶

### <a name="vm"></a>VM

* `availability-set`：已在轉換上公開容錯網域計數
* 已公開 `list-skus` 命令
* 支援無需建立角色指派即可指定身分識別
* 在連結資料磁碟上套用儲存體 SKU
* 已移除使用受控磁碟時的預設作業系統磁碟名稱和儲存體 SKU


## <a name="july-28-2017"></a>2017 年 7 月 28 日

版本 2.0.12

* 已新增容器命令
* 已新增計費和耗用模組

```
azure-cli (2.0.12)  

acr (2.0.9)  
acs (2.0.11)  
appservice (0.1.11)  
batch (3.0.3)  
billing (0.1.3)  
cdn (0.0.6)  
cloud (2.0.7)  
cognitiveservices (0.1.6)  
command-modules-nspkg (2.0.1)  
component (2.0.6)  
configure (2.0.10)  
consumption (0.1.3)  
container (0.1.7)  
core (2.0.12)  
cosmosdb (0.1.11)  
dla (0.0.10)  
dls (0.0.11)  
feedback (2.0.6)  
find (0.2.6)  
interactive (0.3.7)  
iot (0.1.10)  
keyvault (2.0.8)  
lab (0.0.9)  
monitor (0.0.8)  
network (2.0.11)  
nspkg (3.0.1)  
profile (2.0.9)  
rdbms (0.0.5)  
redis (0.2.7)  
resource (2.0.11)  
role (2.0.9)  
sf (1.0.5)  
sql (2.0.8)  
storage (2.0.11)  
vm (2.0.11) 
```

### <a name="core"></a>核心

* 包含憑證之服務主體的輸出 SDK 驗證資訊
* 已修正部署進度例外狀況
* 從目前的雲端使用 arm 端點來建立訂用帳戶用戶端
* clouds.config 檔案的改良並行處理 (#3636)
* 重新整理每個命令執行的用戶端要求識別碼
* 使用正確的 SDK 設定檔建立訂用帳戶用戶端 (#3635)
* 範本部署的進度報告 (#3510)
* 已新增透過 jmespath 查詢挑選資料表輸出欄位的支援 (#3581)
* 已改善剖析引數的靜音和使用手勢的附加記錄 (#3434)
* 使用正確的 SDK 設定檔建立訂用帳戶用戶端
* 將所有現有的記錄檔移到最新的資料夾
* 已修正 VM/VMSS 建立的等冪 (#3586)
* 命令路徑不再區分大小寫
* 特定布林型別參數不再區分大小寫
* 支援在內部部署伺服器上登入 ADFS，例如 Azure Stack
* 已修正並行寫入 clouds.config (#3255)

### <a name="acr"></a>ACR

* 已新增受控登錄的 `show-usage` 命令
* 支援受控登錄的 SKU 更新
* 已新增使用受控 SKU 的受控登錄
* 已新增使用 ACR Webhook 命令模組的受控登錄 Webhook
* 已新增使用 ACR 登入命令進行 AAD 驗證
* 已新增 Docker 存放庫、資訊清單及標籤的 delete 命令

### <a name="acs"></a>ACS

* 支援 2017-07-01 版 API

### <a name="appservice"></a>AppService

* 已修正列出 Linux Webapp 不會傳回任何項目的錯誤
* 支援從 ACR 擷取認證
* 將 `appservice web` 底下的所有命令移除
* 命令輸出中的遮罩 Docker 登錄密碼 (#3656)
* 請確定在 macOS 上使用預設瀏覽器不會發生錯誤 (#3623)
* 改善的 `webapp log tail` 和 `webapp log download` 說明 (#3624)
* 已公開可設定靜態路由的 `traffic-routing` 命令 (#3566)
* 已新增設定原始檔控制中的可靠性修正 (#3245)
* 已從適用於 Windows webapps 的 `webapp config update` 移除不支援的 `--node-version` 引數。 請改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`

### <a name="batch"></a>批次

* 已更新至 Batch SDK 3.0.0 並支援集區中的低優先權 VM
* 已將 `pool create` 選項 `--target-dedicated` 重新命名為 `--target-dedicated-nodes`
* 已新增 `pool create` 選項 `--target-low-priority-nodes` 和 `--application-licenses`

### <a name="cdn"></a>CDN

* 當 `--profile-name` 所指定的設定檔不存在時，已針對 `cdn endpoint list` 提供更好的錯誤訊息。

### <a name="cloud"></a>雲端

* 已將雲端中繼資料端點的 API 版本變更為 YYYY-MM-DD 格式
* 不需要資源庫端點
* 支援只向 ARM 資源管理員端點註冊雲端
* 已提供 `cloud set` 的選項，可在選取目前的雲端時選擇設定檔
* 已公開 `endpoint_vm_image_alias_doc`

### <a name="cosmosdb"></a>CosmosDB

* 已修正允許使用自訂的分割區索引鍵來建立集合
* 已新增集合預設 TTL 的支援。

### <a name="data-lake-analytics"></a>Data Lake Analytics

* 已新增在 `dla account compute-policy` 標題下計算原則管理的命令
* 已新增 `dla job pipeline show`
* 已新增 `dla job recurrence list`

### <a name="data-lake-store"></a>資料湖存放區

* 已新增在 `dls account update` 中使用者受控金鑰保存庫金鑰旋轉的支援
* 已更新基礎 Data Lake Store filesystem SDK 版本，從而解決效能問題
* 已新增命令 `dls enable-key-vault`。 此命令會嘗試啟用使用者所提供用於將 Data Lake Store 帳戶中之資料加密的 Key Vault

### <a name="interactive"></a>互動式

* 已使用快取的命令來改善啟動時間
* 已增加測試涵蓋範圍
* 已增強 '?' 手勢以便同時插入下一個命令中
* 已修正包含設定檔 2017-03-09-profile-preview 的互動式錯誤 (#3587)
* 已允許 `--version` 作為互動式模式的參數 (#3645)
* 停止從驗證完成擲回錯誤的互動模式 (#3570)
* 範本部署的進度報告 (#3510)
* 已新增 `--progress` 旗標
* 已從完成將 `--debug` 和 `--verbose` 移除
* 已從完成將 `interactive` 移除 (#3324)

### <a name="iot"></a>IoT

* 已修正建立原則時無法再清除現有的原則。 (#3934)

### <a name="key-vault"></a>金鑰保存庫

* 已新增金鑰保存庫復原功能的命令：
  * `keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`
  * `keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`
  * `keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`
  * `keyvault key` 子命令 `purge`、`recover`、`list-deleted`
* 已新增服務主體金鑰保存庫整合 (#3133)
* 已將金鑰保存庫資料平面更新為 0.3.2。 (#3307)

### <a name="lab"></a>實驗室

* 已新增透過 `az lab vm claim` 在實驗室中宣告任何 VM 的支援
* 已新增 `az lab vm list` 和 `az lab vm show` 的資料表輸出格式器

### <a name="monitor"></a>監視

* 使用 `monitor autoscale-settings get-parameters-template` 命令修正範本檔案 (#3349)
* 已將 `monitor alert-rule-incidents list` 重新命名為 `monitor alert list-incidents`
* 已將 `monitor alert-rule-incidents show` 重新命名為 `monitor alert show-incident`
* 已將 `monitor metric-defintions list` 重新命名為 `monitor metrics list-definitions`
* 已將 `monitor alert-rules` 重新命名為 `monitor alert`
* 已變更 `monitor alert create`：
  * `condition` 和 `action` 子命令不再接受 JSON
  * 新增多個參數以簡化規則建立程序
  * 已不再需要 `location`
  * 新增目標的名稱和 ID 支援
  * 已移除 `--alert-rule-resource-name`
  * 已不再需要將 `is-enabled` 重新命名為 `enabled`
  * `description` 預設值現在會以所提供的條件作為基礎
  *  新增範例來協助釐清新格式
* 支援 `monitor metric` 命令的名稱或識別碼
* 已將便利性引數和範例新增至 `monitor alert rule update`

### <a name="network"></a>網路

* 已新增 `list-private-access-services` 命令
* 已將 `--private-access-services` 引數新增至 `vnet subnet create` 和 `vnet subnet update`
* 已修正 `application-gateway redirect-config create` 會失敗的問題
* 已修正 `application-gateway redirect-config update` 無法與 `--no-wait` 搭配運作的問題
* 已修正使用 `--servers` 引數搭配 `application-gateway address-pool create` 和 `application-gateway address-pool update` 時的問題
* 已新增 `application-gateway redirect-config` 命令
* 已將命令新增至 `application-gateway ssl-policy`：`list-options`、`predefined list`、`predefined show`
* 已將引數新增至 `application-gateway ssl-policy set`：`--name`、`--cipher-suites`、`--min-protocol-version`
* 已將引數新增至 `application-gateway http-settings create` 和 `application-gateway http-settings update`：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`
* 已將引數新增至 `application-gateway url-path-map create` 和 `application-gateway url-path-map update`：`--default-redirect-config`、`--redirect-config`
* 已將引數 `--redirect-config` 新增至 `application-gateway url-path-map rule create`
* 已將 `--no-wait` 的支援新增至 `application-gateway url-path-map rule delete`
* 已將引數新增至 `application-gateway probe create` 和 `application-gateway probe update`：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`
* 已將引數 `--redirect-config` 新增至 `application-gateway rule create` 和 `application-gateway rule update`
* 已將 `--accelerated-networking` 的支援新增至 `nic create` 和 `nic update`
* 已從 `nic create` 移除 `--internal-dns-name-suffix` 引數
* 已將 `--dns-servers` 的支援新增至 `nic update` 和 `nic create`：已新增 --dns-servers 的支援
* 已修正 `local-gateway create` 忽略 `--local-address-prefixes` 的錯誤
* 已將 `--dns-servers` 的支援新增至 `vnet update`
* 已修正使用 `express-route peering create` 時建立不含路由篩選條件之對等互連的錯誤
* 已修正 `--provider` 和 `--bandwidth` 引數無法使用 `express-route update` 的錯誤
* 已修正 `network watcher show-topology` 預設邏輯的錯誤
* 已改良 `network list-usages` 的輸出格式
* 如果只有一個，請使用 `application-gateway http-listener create` 的預設前端 IP
* 如果只有一個，請使用 `application-gateway rule create` 的預設位址集區、HTTP 設定和 HTTP 接聽程式
* 如果只有一個，請使用 `lb rule create` 的預設前端 IP 和後端集區
* 如果只有一個，請使用 `lb inbound-nat-rule create` 的預設前端 IP

### <a name="profile"></a>設定檔

* 支援使用受管理的身分識別在 VM 內部登入
* 支援 SDK 驗證檔案格式的 `account show` 輸出
* 使用 '--expanded-view' 時，顯示取代警告
* 已新增 `get-access-token` 命令，以提供原始 AAD 權杖
* 支援透過沒有相關聯訂用帳戶的使用者帳戶進行登入

### <a name="rdbms"></a>RDBMS

* 支援列出跨訂用帳戶的伺服器 (#3417)
* 已修正因遺漏 `% server_type` 而未處理 `%s` (#3393)
* 已修正文件來源對應並已新增 CI 工作以進行確認 (#3361)
* 已修正 MySQL 和 PostgreSQL 說明 (#3369)

### <a name="resource"></a>資源

* 已改善遺漏 `group deployment create` 參數的提示
* 已改善 `--parameters KEY=VALUE` 語法的剖析
* 已修正無法再使用 `@<file>` 語法辨識 `group deployment create` 參數檔案的問題
* 支援 `resource` 和 `managedapp` 命令的 `--ids` 引數
* 已修正某些剖析和錯誤訊息 (#3584)
* 已修正 `lock` 命令的 `--resource-type` 剖析，以接受 `<resource-namespace>` 和 `<resource-type>`
* 已新增範本連結範本的參數檢查 (#3629)
* 已新增使用 `KEY=VALUE` 語法指定部署參數的支援

### <a name="role"></a>角色

* 支援 SDK 驗證檔案格式的 `create-for-rbac` 輸出
* 已清除在刪除服務主體時的角色指派和相關 AAD 應用程式 (#3610)
* 包含 `app create` 引數 `--start-date` 和 `--end-date` 描述中的時間格式
* 使用 `--expanded-view` 時，顯示取代警告
* 已新增金鑰保存庫整合至 `create-for-rbac` 和 `reset-credentials` 命令

### <a name="service-fabric"></a>Service Fabric
* 已修正應用程式中的大型檔案在上傳時被截斷的問題 (#3666)
* 已新增適用於 Service Fabric 命令的測試 (#3424)
* 已修正許多 Service Fabric 命令 (#3234)

### <a name="sql"></a>SQL

* 已移除中斷的 `sql server create` `--identity` 參數
* 已從 `sql server create` 和 `sql server update` 命令輸出移除密碼值
* 已新增命令 `sql db list-editions` 和 `sql elastic-pool list-editions`

### <a name="storage"></a>儲存體

* 已從 `storage blob list`、`storage container list` 和 `storage share list` 命令移除 `--marker` 選項 (#3745)
* 已啟用建立 https 專用儲存體帳戶
* 已更新儲存體計量、記錄和 cors 命令 (#3495)
* 已從 CORS 新增改換措辭例外狀況訊息 (#3638) (#3362)  
* 已將產生器轉換為下載批次命令不重複原則執行模式中的清單 (#3592) 
* 已修正 blob 下載批次不重複原則執行問題 (#3640) (#3592)

### <a name="vm"></a>VM

* 支援設定 NSG
* 已修正 DNS 伺服器未正確設定的錯誤
* 支援受管理的服務身分識別
* 已修正 `cmss create` 與現有負載平衡器需要 `--backend-pool-name` 的問題。
* 請使用開頭為 0 的 `vm image create` lun 建立 DataDisk


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
您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。您可以從包含 `az feedback` 命令的命令列提供意見反應。

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

