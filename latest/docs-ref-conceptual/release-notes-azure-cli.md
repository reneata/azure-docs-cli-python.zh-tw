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
ms.openlocfilehash: e893b99349bbf2a5eec8af254158eb07001f1da7
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="3bda3-104">Azure CLI 2.0 版本資訊</span><span class="sxs-lookup"><span data-stu-id="3bda3-104">Azure CLI 2.0 release notes</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="3bda3-105">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-105">August 28, 2017</span></span>

<span data-ttu-id="3bda3-106">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="3bda3-106">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="3bda3-107">CLI</span><span class="sxs-lookup"><span data-stu-id="3bda3-107">CLI</span></span>

* <span data-ttu-id="3bda3-108">已將法律注意事項新增至 `--version`。</span><span class="sxs-lookup"><span data-stu-id="3bda3-108">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="3bda3-109">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-109">ACS</span></span>

* <span data-ttu-id="3bda3-110">已更正預覽區域。</span><span class="sxs-lookup"><span data-stu-id="3bda3-110">Corrected preview regions.</span></span>
* <span data-ttu-id="3bda3-111">已正確格式化預設 `dns_name_prefix`。</span><span class="sxs-lookup"><span data-stu-id="3bda3-111">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="3bda3-112">最佳化的 acs 命令輸出。</span><span class="sxs-lookup"><span data-stu-id="3bda3-112">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="3bda3-113">AppService</span><span class="sxs-lookup"><span data-stu-id="3bda3-113">Appservice</span></span>

* <span data-ttu-id="3bda3-114">[新變更] 已修正 `az webapp config appsettings [delete|set]` 輸出中的不一致</span><span class="sxs-lookup"><span data-stu-id="3bda3-114">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="3bda3-115">已針對 `az webapp config container set --docker-custom-image-name` 新增 `-i` 的新別名</span><span class="sxs-lookup"><span data-stu-id="3bda3-115">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="3bda3-116">已公開 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="3bda3-116">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="3bda3-117">已公開 `az webapp delete` 中的新引數，可保留應用程式服務計劃、計量或 DNS 註冊</span><span class="sxs-lookup"><span data-stu-id="3bda3-117">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="3bda3-118">已修正：正確偵測到位置設定</span><span class="sxs-lookup"><span data-stu-id="3bda3-118">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="3bda3-119">IoT</span><span class="sxs-lookup"><span data-stu-id="3bda3-119">IoT</span></span>

* <span data-ttu-id="3bda3-120">已修正 #3934：建立原則時無法再清除現有的原則</span><span class="sxs-lookup"><span data-stu-id="3bda3-120">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="3bda3-121">網路</span><span class="sxs-lookup"><span data-stu-id="3bda3-121">Network</span></span>

* <span data-ttu-id="3bda3-122">[新變更] 已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="3bda3-122">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="3bda3-123">[新變更] 已將 `--private-access-services` 選項重新命名為適用於 `vnet subnet [create|update]` 的 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="3bda3-123">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="3bda3-124">已將多個 IP 和連接埠範圍的支援新增至 `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="3bda3-124">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="3bda3-125">已將 SKU 的支援新增至 `lb create`</span><span class="sxs-lookup"><span data-stu-id="3bda3-125">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="3bda3-126">已將 SKU 的支援新增至 `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="3bda3-126">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="3bda3-127">設定檔</span><span class="sxs-lookup"><span data-stu-id="3bda3-127">Profile</span></span>

* <span data-ttu-id="3bda3-128">已公開 `--msi` 和 `--msi-port`，可使用虛擬機器的身分識別登入</span><span class="sxs-lookup"><span data-stu-id="3bda3-128">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="3bda3-129">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3bda3-129">Service Fabric</span></span>

* <span data-ttu-id="3bda3-130">預覽版本</span><span class="sxs-lookup"><span data-stu-id="3bda3-130">Preview release</span></span>
* <span data-ttu-id="3bda3-131">簡化的登錄使用者/命令的密碼規則</span><span class="sxs-lookup"><span data-stu-id="3bda3-131">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="3bda3-132">已修正使用者即使在參數中傳遞之後的密碼提示</span><span class="sxs-lookup"><span data-stu-id="3bda3-132">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="3bda3-133">已新增空白 `registry_cred` 的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-133">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="3bda3-134">儲存體</span><span class="sxs-lookup"><span data-stu-id="3bda3-134">Storage</span></span>

* <span data-ttu-id="3bda3-135">已啟用設定 blob 層</span><span class="sxs-lookup"><span data-stu-id="3bda3-135">Enabled setting blob tier</span></span>
* <span data-ttu-id="3bda3-136">已將 `--bypass` 和 `--default-action` 引數新增至 `storage account [create|update]` 以支援服務通道</span><span class="sxs-lookup"><span data-stu-id="3bda3-136">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="3bda3-137">新增的命令可將 VNET 規則和以 IP 作為基礎的規則新增至 `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="3bda3-137">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="3bda3-138">透過客戶管理的金鑰啟用服務加密</span><span class="sxs-lookup"><span data-stu-id="3bda3-138">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="3bda3-139">[新變更] 已將 `--encryption` 選項重新命名為適用於 `az storage account create and az storage account update` 命令的 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="3bda3-139">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="3bda3-140">已修正 #4220：`az storage account update encryption` - 語法不相符</span><span class="sxs-lookup"><span data-stu-id="3bda3-140">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="3bda3-141">VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-141">VM</span></span>

* <span data-ttu-id="3bda3-142">已修正使用 `--instance-id *` 時會顯示 `vmss get-instance-view` 的額外錯誤資訊的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-142">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="3bda3-143">已將 `--lb-sku` 的支援新增至 `vmss create`：</span><span class="sxs-lookup"><span data-stu-id="3bda3-143">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="3bda3-144">從 `[vm|vmss] create` 的系統管理員名稱封鎖清單移除人力名稱</span><span class="sxs-lookup"><span data-stu-id="3bda3-144">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="3bda3-145">已修正在無法從映像擷取計劃資訊時，`[vm|vmss] create` 會擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-145">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="3bda3-146">已修正使用內部 LB 建立 vmms scaleset 時的損毀</span><span class="sxs-lookup"><span data-stu-id="3bda3-146">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="3bda3-147">已修正 `--no-wait` 引數無法與 `vm availability-set create` 搭配使用的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-147">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="3bda3-148">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-148">August 15, 2017</span></span>

<span data-ttu-id="3bda3-149">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="3bda3-149">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="3bda3-150">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-150">ACS</span></span>

* <span data-ttu-id="3bda3-151">已更正 kubernetes 的 sshMaster0 連接埠號碼</span><span class="sxs-lookup"><span data-stu-id="3bda3-151">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="3bda3-152">AppService</span><span class="sxs-lookup"><span data-stu-id="3bda3-152">Appservice</span></span>

* <span data-ttu-id="3bda3-153">已修正建立以新 git 作為基礎的 Linux WebApp 時的例外狀況</span><span class="sxs-lookup"><span data-stu-id="3bda3-153">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="3bda3-154">Event Grid</span><span class="sxs-lookup"><span data-stu-id="3bda3-154">Event Grid</span></span>

* <span data-ttu-id="3bda3-155">已新增 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="3bda3-155">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="3bda3-156">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-156">August 11, 2017</span></span>

<span data-ttu-id="3bda3-157">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="3bda3-157">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="3bda3-158">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-158">ACS</span></span>

* <span data-ttu-id="3bda3-159">新增更多預覽區域</span><span class="sxs-lookup"><span data-stu-id="3bda3-159">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="3bda3-160">批次</span><span class="sxs-lookup"><span data-stu-id="3bda3-160">Batch</span></span>

* <span data-ttu-id="3bda3-161">更新為 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="3bda3-161">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="3bda3-162">已新增新的命令顯示作業的工作計數</span><span class="sxs-lookup"><span data-stu-id="3bda3-162">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="3bda3-163">已修正資源檔案 SAS URL 處理中的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-163">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="3bda3-164">Batch 帳戶端點現在支援選擇性的 'https://' 前置詞</span><span class="sxs-lookup"><span data-stu-id="3bda3-164">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="3bda3-165">支援將超過 100 個工作的清單新增至作業</span><span class="sxs-lookup"><span data-stu-id="3bda3-165">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="3bda3-166">已新增載入擴充功能命令模組的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="3bda3-166">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="3bda3-167">元件</span><span class="sxs-lookup"><span data-stu-id="3bda3-167">Component</span></span>

* <span data-ttu-id="3bda3-168">已新增對 'az component' 命令的取代警告</span><span class="sxs-lookup"><span data-stu-id="3bda3-168">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="3bda3-169">容器</span><span class="sxs-lookup"><span data-stu-id="3bda3-169">Container</span></span>

* <span data-ttu-id="3bda3-170">`create`：已修正環境變數內不允許等號的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-170">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="3bda3-171">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3bda3-171">Data Lake Store</span></span>

* <span data-ttu-id="3bda3-172">已啟用進度控制項</span><span class="sxs-lookup"><span data-stu-id="3bda3-172">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="3bda3-173">Event Grid</span><span class="sxs-lookup"><span data-stu-id="3bda3-173">Event Grid</span></span>

* <span data-ttu-id="3bda3-174">初始版本</span><span class="sxs-lookup"><span data-stu-id="3bda3-174">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="3bda3-175">網路</span><span class="sxs-lookup"><span data-stu-id="3bda3-175">Network</span></span>

* <span data-ttu-id="3bda3-176">`lb`：已修正省略某些子資源名稱時未正確解析的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-176">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="3bda3-177">`application-gateway {subresource} delete`：已修正無法接受 `--no-wait` 的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-177">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="3bda3-178">`application-gateway http-settings update`：已修正無法關閉 `--connection-draining-timeout` 的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-178">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="3bda3-179">已修正非預期關鍵字引數 `sa_data_size_kilobyes` 與 `az network vpn-connection ipsec-policy add` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-179">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="3bda3-180">設定檔</span><span class="sxs-lookup"><span data-stu-id="3bda3-180">Profile</span></span>

* <span data-ttu-id="3bda3-181">`account list`：已新增 `--refresh`，可從伺服器同步處理最新的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="3bda3-181">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="3bda3-182">儲存體</span><span class="sxs-lookup"><span data-stu-id="3bda3-182">Storage</span></span>

* <span data-ttu-id="3bda3-183">使用指派身分識別的系統來啟用更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="3bda3-183">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="3bda3-184">VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-184">VM</span></span>

* <span data-ttu-id="3bda3-185">`availability-set`：已在轉換上公開容錯網域計數</span><span class="sxs-lookup"><span data-stu-id="3bda3-185">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="3bda3-186">已公開 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-186">Exposed `list-skus` command</span></span>
* <span data-ttu-id="3bda3-187">支援無需建立角色指派即可指定身分識別</span><span class="sxs-lookup"><span data-stu-id="3bda3-187">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="3bda3-188">在連結資料磁碟上套用儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="3bda3-188">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="3bda3-189">已移除使用受控磁碟時的預設作業系統磁碟名稱和儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="3bda3-189">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="3bda3-190">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-190">July 28, 2017</span></span>

<span data-ttu-id="3bda3-191">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="3bda3-191">Version 2.0.12</span></span>

* <span data-ttu-id="3bda3-192">已新增容器命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-192">Added container commands</span></span>
* <span data-ttu-id="3bda3-193">已新增計費和耗用模組</span><span class="sxs-lookup"><span data-stu-id="3bda3-193">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="3bda3-194">核心</span><span class="sxs-lookup"><span data-stu-id="3bda3-194">Core</span></span>

* <span data-ttu-id="3bda3-195">包含憑證之服務主體的輸出 SDK 驗證資訊</span><span class="sxs-lookup"><span data-stu-id="3bda3-195">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="3bda3-196">已修正部署進度例外狀況</span><span class="sxs-lookup"><span data-stu-id="3bda3-196">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="3bda3-197">從目前的雲端使用 arm 端點來建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="3bda3-197">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="3bda3-198">clouds.config 檔案的改良並行處理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="3bda3-198">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="3bda3-199">重新整理每個命令執行的用戶端要求識別碼</span><span class="sxs-lookup"><span data-stu-id="3bda3-199">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="3bda3-200">使用正確的 SDK 設定檔建立訂用帳戶用戶端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="3bda3-200">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="3bda3-201">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="3bda3-201">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="3bda3-202">已新增透過 jmespath 查詢挑選資料表輸出欄位的支援 (#3581)</span><span class="sxs-lookup"><span data-stu-id="3bda3-202">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="3bda3-203">已改善剖析引數的靜音和使用手勢的附加記錄 (#3434)</span><span class="sxs-lookup"><span data-stu-id="3bda3-203">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="3bda3-204">使用正確的 SDK 設定檔建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="3bda3-204">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="3bda3-205">將所有現有的記錄檔移到最新的資料夾</span><span class="sxs-lookup"><span data-stu-id="3bda3-205">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="3bda3-206">已修正 VM/VMSS 建立的等冪 (#3586)</span><span class="sxs-lookup"><span data-stu-id="3bda3-206">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="3bda3-207">命令路徑不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="3bda3-207">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="3bda3-208">特定布林型別參數不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="3bda3-208">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="3bda3-209">支援在內部部署伺服器上登入 ADFS，例如 Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3bda3-209">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="3bda3-210">已修正並行寫入 clouds.config (#3255)</span><span class="sxs-lookup"><span data-stu-id="3bda3-210">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="3bda3-211">ACR</span><span class="sxs-lookup"><span data-stu-id="3bda3-211">ACR</span></span>

* <span data-ttu-id="3bda3-212">已新增受控登錄的 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-212">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="3bda3-213">支援受控登錄的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="3bda3-213">Support SKU update for managed registries</span></span>
* <span data-ttu-id="3bda3-214">已新增使用受控 SKU 的受控登錄</span><span class="sxs-lookup"><span data-stu-id="3bda3-214">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="3bda3-215">已新增使用 ACR Webhook 命令模組的受控登錄 Webhook</span><span class="sxs-lookup"><span data-stu-id="3bda3-215">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="3bda3-216">已新增使用 ACR 登入命令進行 AAD 驗證</span><span class="sxs-lookup"><span data-stu-id="3bda3-216">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="3bda3-217">已新增 Docker 存放庫、資訊清單及標籤的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-217">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="3bda3-218">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-218">ACS</span></span>

* <span data-ttu-id="3bda3-219">支援 2017-07-01 版 API</span><span class="sxs-lookup"><span data-stu-id="3bda3-219">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="3bda3-220">AppService</span><span class="sxs-lookup"><span data-stu-id="3bda3-220">Appservice</span></span>

* <span data-ttu-id="3bda3-221">已修正列出 Linux Webapp 不會傳回任何項目的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-221">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="3bda3-222">支援從 ACR 擷取認證</span><span class="sxs-lookup"><span data-stu-id="3bda3-222">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="3bda3-223">將 `appservice web` 底下的所有命令移除</span><span class="sxs-lookup"><span data-stu-id="3bda3-223">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="3bda3-224">命令輸出中的遮罩 Docker 登錄密碼 (#3656)</span><span class="sxs-lookup"><span data-stu-id="3bda3-224">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="3bda3-225">請確定在 macOS 上使用預設瀏覽器不會發生錯誤 (#3623)</span><span class="sxs-lookup"><span data-stu-id="3bda3-225">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="3bda3-226">改善的 `webapp log tail` 和 `webapp log download` 說明 (#3624)</span><span class="sxs-lookup"><span data-stu-id="3bda3-226">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="3bda3-227">已公開可設定靜態路由的 `traffic-routing` 命令 (#3566)</span><span class="sxs-lookup"><span data-stu-id="3bda3-227">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="3bda3-228">已新增設定原始檔控制中的可靠性修正 (#3245)</span><span class="sxs-lookup"><span data-stu-id="3bda3-228">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="3bda3-229">已從適用於 Windows webapps 的 `webapp config update` 移除不支援的 `--node-version` 引數。</span><span class="sxs-lookup"><span data-stu-id="3bda3-229">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="3bda3-230">請改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span><span class="sxs-lookup"><span data-stu-id="3bda3-230">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="3bda3-231">批次</span><span class="sxs-lookup"><span data-stu-id="3bda3-231">Batch</span></span>

* <span data-ttu-id="3bda3-232">已更新至 Batch SDK 3.0.0 並支援集區中的低優先權 VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-232">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="3bda3-233">已將 `pool create` 選項 `--target-dedicated` 重新命名為 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="3bda3-233">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="3bda3-234">已新增 `pool create` 選項 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="3bda3-234">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="3bda3-235">CDN</span><span class="sxs-lookup"><span data-stu-id="3bda3-235">CDN</span></span>

* <span data-ttu-id="3bda3-236">當 `--profile-name` 所指定的設定檔不存在時，已針對 `cdn endpoint list` 提供更好的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3bda3-236">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="3bda3-237">雲端</span><span class="sxs-lookup"><span data-stu-id="3bda3-237">Cloud</span></span>

* <span data-ttu-id="3bda3-238">已將雲端中繼資料端點的 API 版本變更為 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="3bda3-238">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="3bda3-239">不需要資源庫端點</span><span class="sxs-lookup"><span data-stu-id="3bda3-239">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="3bda3-240">支援只向 ARM 資源管理員端點註冊雲端</span><span class="sxs-lookup"><span data-stu-id="3bda3-240">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="3bda3-241">已提供 `cloud set` 的選項，可在選取目前的雲端時選擇設定檔</span><span class="sxs-lookup"><span data-stu-id="3bda3-241">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="3bda3-242">已公開 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="3bda3-242">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="3bda3-243">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3bda3-243">CosmosDB</span></span>

* <span data-ttu-id="3bda3-244">已修正允許使用自訂的分割區索引鍵來建立集合</span><span class="sxs-lookup"><span data-stu-id="3bda3-244">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="3bda3-245">已新增集合預設 TTL 的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-245">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="3bda3-246">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3bda3-246">Data Lake Analytics</span></span>

* <span data-ttu-id="3bda3-247">已新增在 `dla account compute-policy` 標題下計算原則管理的命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-247">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="3bda3-248">已新增 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="3bda3-248">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="3bda3-249">已新增 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="3bda3-249">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="3bda3-250">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3bda3-250">Data Lake Store</span></span>

* <span data-ttu-id="3bda3-251">已新增在 `dls account update` 中使用者受控金鑰保存庫金鑰旋轉的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-251">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="3bda3-252">已更新基礎 Data Lake Store filesystem SDK 版本，從而解決效能問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-252">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="3bda3-253">已新增命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="3bda3-253">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="3bda3-254">此命令會嘗試啟用使用者所提供用於將 Data Lake Store 帳戶中之資料加密的 Key Vault</span><span class="sxs-lookup"><span data-stu-id="3bda3-254">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="3bda3-255">互動式</span><span class="sxs-lookup"><span data-stu-id="3bda3-255">Interactive</span></span>

* <span data-ttu-id="3bda3-256">已使用快取的命令來改善啟動時間</span><span class="sxs-lookup"><span data-stu-id="3bda3-256">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="3bda3-257">已增加測試涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="3bda3-257">Increased test coverage</span></span>
* <span data-ttu-id="3bda3-258">已增強 '?' 手勢以便同時插入下一個命令中</span><span class="sxs-lookup"><span data-stu-id="3bda3-258">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="3bda3-259">已修正包含設定檔 2017-03-09-profile-preview 的互動式錯誤 (#3587)</span><span class="sxs-lookup"><span data-stu-id="3bda3-259">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="3bda3-260">已允許 `--version` 作為互動式模式的參數 (#3645)</span><span class="sxs-lookup"><span data-stu-id="3bda3-260">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="3bda3-261">停止從驗證完成擲回錯誤的互動模式 (#3570)</span><span class="sxs-lookup"><span data-stu-id="3bda3-261">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="3bda3-262">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="3bda3-262">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="3bda3-263">已新增 `--progress` 旗標</span><span class="sxs-lookup"><span data-stu-id="3bda3-263">Added `--progress` flag</span></span>
* <span data-ttu-id="3bda3-264">已從完成將 `--debug` 和 `--verbose` 移除</span><span class="sxs-lookup"><span data-stu-id="3bda3-264">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="3bda3-265">已從完成將 `interactive` 移除 (#3324)</span><span class="sxs-lookup"><span data-stu-id="3bda3-265">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="3bda3-266">IoT</span><span class="sxs-lookup"><span data-stu-id="3bda3-266">IoT</span></span>

* <span data-ttu-id="3bda3-267">已修正建立原則時無法再清除現有的原則。</span><span class="sxs-lookup"><span data-stu-id="3bda3-267">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="3bda3-268">(#3934)</span><span class="sxs-lookup"><span data-stu-id="3bda3-268">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="3bda3-269">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="3bda3-269">Key vault</span></span>

* <span data-ttu-id="3bda3-270">已新增金鑰保存庫復原功能的命令：</span><span class="sxs-lookup"><span data-stu-id="3bda3-270">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="3bda3-271">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="3bda3-271">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="3bda3-272">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="3bda3-272">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="3bda3-273">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="3bda3-273">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="3bda3-274">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="3bda3-274">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="3bda3-275">已新增服務主體金鑰保存庫整合 (#3133)</span><span class="sxs-lookup"><span data-stu-id="3bda3-275">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="3bda3-276">已將金鑰保存庫資料平面更新為 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="3bda3-276">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="3bda3-277">(#3307)</span><span class="sxs-lookup"><span data-stu-id="3bda3-277">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="3bda3-278">實驗室</span><span class="sxs-lookup"><span data-stu-id="3bda3-278">Lab</span></span>

* <span data-ttu-id="3bda3-279">已新增透過 `az lab vm claim` 在實驗室中宣告任何 VM 的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-279">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="3bda3-280">已新增 `az lab vm list` 和 `az lab vm show` 的資料表輸出格式器</span><span class="sxs-lookup"><span data-stu-id="3bda3-280">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="3bda3-281">監視</span><span class="sxs-lookup"><span data-stu-id="3bda3-281">Monitor</span></span>

* <span data-ttu-id="3bda3-282">使用 `monitor autoscale-settings get-parameters-template` 命令修正範本檔案 (#3349)</span><span class="sxs-lookup"><span data-stu-id="3bda3-282">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="3bda3-283">已將 `monitor alert-rule-incidents list` 重新命名為 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="3bda3-283">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="3bda3-284">已將 `monitor alert-rule-incidents show` 重新命名為 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="3bda3-284">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="3bda3-285">已將 `monitor metric-defintions list` 重新命名為 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="3bda3-285">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="3bda3-286">已將 `monitor alert-rules` 重新命名為 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="3bda3-286">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="3bda3-287">已變更 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="3bda3-287">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="3bda3-288">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="3bda3-288">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="3bda3-289">新增多個參數以簡化規則建立程序</span><span class="sxs-lookup"><span data-stu-id="3bda3-289">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="3bda3-290">已不再需要 `location`</span><span class="sxs-lookup"><span data-stu-id="3bda3-290">`location` no longer required</span></span>
  * <span data-ttu-id="3bda3-291">新增目標的名稱和 ID 支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-291">Add name and ID support for target</span></span>
  * <span data-ttu-id="3bda3-292">已移除 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="3bda3-292">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="3bda3-293">已不再需要將 `is-enabled` 重新命名為 `enabled`</span><span class="sxs-lookup"><span data-stu-id="3bda3-293">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="3bda3-294">`description` 預設值現在會以所提供的條件作為基礎</span><span class="sxs-lookup"><span data-stu-id="3bda3-294">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="3bda3-295">新增範例來協助釐清新格式</span><span class="sxs-lookup"><span data-stu-id="3bda3-295">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="3bda3-296">支援 `monitor metric` 命令的名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="3bda3-296">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="3bda3-297">已將便利性引數和範例新增至 `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="3bda3-297">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="3bda3-298">網路</span><span class="sxs-lookup"><span data-stu-id="3bda3-298">Network</span></span>

* <span data-ttu-id="3bda3-299">已新增 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-299">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="3bda3-300">已將 `--private-access-services` 引數新增至 `vnet subnet create` 和 `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="3bda3-300">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="3bda3-301">已修正 `application-gateway redirect-config create` 會失敗的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-301">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="3bda3-302">已修正 `application-gateway redirect-config update` 無法與 `--no-wait` 搭配運作的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-302">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="3bda3-303">已修正使用 `--servers` 引數搭配 `application-gateway address-pool create` 和 `application-gateway address-pool update` 時的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-303">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="3bda3-304">已新增 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-304">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="3bda3-305">已將命令新增至 `application-gateway ssl-policy`：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="3bda3-305">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="3bda3-306">已將引數新增至 `application-gateway ssl-policy set`：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="3bda3-306">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="3bda3-307">已將引數新增至 `application-gateway http-settings create` 和 `application-gateway http-settings update`：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="3bda3-307">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="3bda3-308">已將引數新增至 `application-gateway url-path-map create` 和 `application-gateway url-path-map update`：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="3bda3-308">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="3bda3-309">已將引數 `--redirect-config` 新增至 `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="3bda3-309">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="3bda3-310">已將 `--no-wait` 的支援新增至 `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="3bda3-310">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="3bda3-311">已將引數新增至 `application-gateway probe create` 和 `application-gateway probe update`：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="3bda3-311">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="3bda3-312">已將引數 `--redirect-config` 新增至 `application-gateway rule create` 和 `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="3bda3-312">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="3bda3-313">已將 `--accelerated-networking` 的支援新增至 `nic create` 和 `nic update`</span><span class="sxs-lookup"><span data-stu-id="3bda3-313">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="3bda3-314">已從 `nic create` 移除 `--internal-dns-name-suffix` 引數</span><span class="sxs-lookup"><span data-stu-id="3bda3-314">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="3bda3-315">已將 `--dns-servers` 的支援新增至 `nic update` 和 `nic create`：已新增 --dns-servers 的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-315">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="3bda3-316">已修正 `local-gateway create` 忽略 `--local-address-prefixes` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-316">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="3bda3-317">已將 `--dns-servers` 的支援新增至 `vnet update`</span><span class="sxs-lookup"><span data-stu-id="3bda3-317">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="3bda3-318">已修正使用 `express-route peering create` 時建立不含路由篩選條件之對等互連的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-318">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="3bda3-319">已修正 `--provider` 和 `--bandwidth` 引數無法使用 `express-route update` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-319">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="3bda3-320">已修正 `network watcher show-topology` 預設邏輯的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-320">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="3bda3-321">已改良 `network list-usages` 的輸出格式</span><span class="sxs-lookup"><span data-stu-id="3bda3-321">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="3bda3-322">如果只有一個，請使用 `application-gateway http-listener create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="3bda3-322">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="3bda3-323">如果只有一個，請使用 `application-gateway rule create` 的預設位址集區、HTTP 設定和 HTTP 接聽程式</span><span class="sxs-lookup"><span data-stu-id="3bda3-323">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="3bda3-324">如果只有一個，請使用 `lb rule create` 的預設前端 IP 和後端集區</span><span class="sxs-lookup"><span data-stu-id="3bda3-324">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="3bda3-325">如果只有一個，請使用 `lb inbound-nat-rule create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="3bda3-325">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="3bda3-326">設定檔</span><span class="sxs-lookup"><span data-stu-id="3bda3-326">Profile</span></span>

* <span data-ttu-id="3bda3-327">支援使用受管理的身分識別在 VM 內部登入</span><span class="sxs-lookup"><span data-stu-id="3bda3-327">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="3bda3-328">支援 SDK 驗證檔案格式的 `account show` 輸出</span><span class="sxs-lookup"><span data-stu-id="3bda3-328">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="3bda3-329">使用 '--expanded-view' 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="3bda3-329">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="3bda3-330">已新增 `get-access-token` 命令，以提供原始 AAD 權杖</span><span class="sxs-lookup"><span data-stu-id="3bda3-330">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="3bda3-331">支援透過沒有相關聯訂用帳戶的使用者帳戶進行登入</span><span class="sxs-lookup"><span data-stu-id="3bda3-331">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="3bda3-332">RDBMS</span><span class="sxs-lookup"><span data-stu-id="3bda3-332">RDBMS</span></span>

* <span data-ttu-id="3bda3-333">支援列出跨訂用帳戶的伺服器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="3bda3-333">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="3bda3-334">已修正因遺漏 `% server_type` 而未處理 `%s` (#3393)</span><span class="sxs-lookup"><span data-stu-id="3bda3-334">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="3bda3-335">已修正文件來源對應並已新增 CI 工作以進行確認 (#3361)</span><span class="sxs-lookup"><span data-stu-id="3bda3-335">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="3bda3-336">已修正 MySQL 和 PostgreSQL 說明 (#3369)</span><span class="sxs-lookup"><span data-stu-id="3bda3-336">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="3bda3-337">資源</span><span class="sxs-lookup"><span data-stu-id="3bda3-337">Resource</span></span>

* <span data-ttu-id="3bda3-338">已改善遺漏 `group deployment create` 參數的提示</span><span class="sxs-lookup"><span data-stu-id="3bda3-338">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="3bda3-339">已改善 `--parameters KEY=VALUE` 語法的剖析</span><span class="sxs-lookup"><span data-stu-id="3bda3-339">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="3bda3-340">已修正無法再使用 `@<file>` 語法辨識 `group deployment create` 參數檔案的問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-340">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="3bda3-341">支援 `resource` 和 `managedapp` 命令的 `--ids` 引數</span><span class="sxs-lookup"><span data-stu-id="3bda3-341">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="3bda3-342">已修正某些剖析和錯誤訊息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="3bda3-342">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="3bda3-343">已修正 `lock` 命令的 `--resource-type` 剖析，以接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="3bda3-343">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="3bda3-344">已新增範本連結範本的參數檢查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="3bda3-344">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="3bda3-345">已新增使用 `KEY=VALUE` 語法指定部署參數的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-345">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="3bda3-346">角色</span><span class="sxs-lookup"><span data-stu-id="3bda3-346">Role</span></span>

* <span data-ttu-id="3bda3-347">支援 SDK 驗證檔案格式的 `create-for-rbac` 輸出</span><span class="sxs-lookup"><span data-stu-id="3bda3-347">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="3bda3-348">已清除在刪除服務主體時的角色指派和相關 AAD 應用程式 (#3610)</span><span class="sxs-lookup"><span data-stu-id="3bda3-348">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="3bda3-349">包含 `app create` 引數 `--start-date` 和 `--end-date` 描述中的時間格式</span><span class="sxs-lookup"><span data-stu-id="3bda3-349">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="3bda3-350">使用 `--expanded-view` 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="3bda3-350">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="3bda3-351">已新增金鑰保存庫整合至 `create-for-rbac` 和 `reset-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="3bda3-351">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="3bda3-352">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3bda3-352">Service Fabric</span></span>
* <span data-ttu-id="3bda3-353">已修正應用程式中的大型檔案在上傳時被截斷的問題 (#3666)</span><span class="sxs-lookup"><span data-stu-id="3bda3-353">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="3bda3-354">已新增適用於 Service Fabric 命令的測試 (#3424)</span><span class="sxs-lookup"><span data-stu-id="3bda3-354">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="3bda3-355">已修正許多 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="3bda3-355">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="3bda3-356">SQL</span><span class="sxs-lookup"><span data-stu-id="3bda3-356">SQL</span></span>

* <span data-ttu-id="3bda3-357">已移除中斷的 `sql server create` `--identity` 參數</span><span class="sxs-lookup"><span data-stu-id="3bda3-357">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="3bda3-358">已從 `sql server create` 和 `sql server update` 命令輸出移除密碼值</span><span class="sxs-lookup"><span data-stu-id="3bda3-358">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="3bda3-359">已新增命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="3bda3-359">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="3bda3-360">儲存體</span><span class="sxs-lookup"><span data-stu-id="3bda3-360">Storage</span></span>

* <span data-ttu-id="3bda3-361">已從 `storage blob list`、`storage container list` 和 `storage share list` 命令移除 `--marker` 選項 (#3745)</span><span class="sxs-lookup"><span data-stu-id="3bda3-361">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="3bda3-362">已啟用建立 https 專用儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="3bda3-362">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="3bda3-363">已更新儲存體計量、記錄和 cors 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="3bda3-363">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="3bda3-364">已從 CORS 新增改換措辭例外狀況訊息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="3bda3-364">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="3bda3-365">已將產生器轉換為下載批次命令不重複原則執行模式中的清單 (#3592)</span><span class="sxs-lookup"><span data-stu-id="3bda3-365">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="3bda3-366">已修正 blob 下載批次不重複原則執行問題 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="3bda3-366">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="3bda3-367">VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-367">VM</span></span>

* <span data-ttu-id="3bda3-368">支援設定 NSG</span><span class="sxs-lookup"><span data-stu-id="3bda3-368">Support configuring nsg</span></span>
* <span data-ttu-id="3bda3-369">已修正 DNS 伺服器未正確設定的錯誤</span><span class="sxs-lookup"><span data-stu-id="3bda3-369">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="3bda3-370">支援受管理的服務身分識別</span><span class="sxs-lookup"><span data-stu-id="3bda3-370">Support managed service identities</span></span>
* <span data-ttu-id="3bda3-371">已修正 `cmss create` 與現有負載平衡器需要 `--backend-pool-name` 的問題。</span><span class="sxs-lookup"><span data-stu-id="3bda3-371">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="3bda3-372">請使用開頭為 0 的 `vm image create` lun 建立 DataDisk</span><span class="sxs-lookup"><span data-stu-id="3bda3-372">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="3bda3-373">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-373">May 10, 2017</span></span>

<span data-ttu-id="3bda3-374">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="3bda3-374">Version 2.0.6</span></span>

* <span data-ttu-id="3bda3-375">documentdb 已重新命名為 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="3bda3-375">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="3bda3-376">新增 rdbms (mysql、postgres)</span><span class="sxs-lookup"><span data-stu-id="3bda3-376">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="3bda3-377">包含 Data Lake Analytics 和 Data Lake Store 模組。</span><span class="sxs-lookup"><span data-stu-id="3bda3-377">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="3bda3-378">包含「辨識服務」模組。</span><span class="sxs-lookup"><span data-stu-id="3bda3-378">Include Cognitive Services module.</span></span>
* <span data-ttu-id="3bda3-379">包含 Service Fabric 模組。</span><span class="sxs-lookup"><span data-stu-id="3bda3-379">Include Service Fabric module.</span></span>
* <span data-ttu-id="3bda3-380">包含「互動式」模組 (az-shell 的重新命名)。</span><span class="sxs-lookup"><span data-stu-id="3bda3-380">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="3bda3-381">新增對 CDN 命令的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-381">Add support for CDN commands.</span></span>
* <span data-ttu-id="3bda3-382">移除「容器」模組。</span><span class="sxs-lookup"><span data-stu-id="3bda3-382">Remove Container module.</span></span>
* <span data-ttu-id="3bda3-383">新增 'az -v' 作為 'az --version' 的捷徑 ([#2926 (英文)](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="3bda3-383">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="3bda3-384">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="3bda3-384">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="3bda3-385">核心</span><span class="sxs-lookup"><span data-stu-id="3bda3-385">Core</span></span>

* <span data-ttu-id="3bda3-386">核心：捕捉未註冊提供者所造成的例外狀況，並自動註冊該提供者</span><span class="sxs-lookup"><span data-stu-id="3bda3-386">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="3bda3-387">效能：將 adal 權杖快取保存在記憶體中，直到程序結束為止 ([#2603 (英文)](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="3bda3-387">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="3bda3-388">修正從十六進位指紋 -o tsv 傳回的位元組 ([#3053 (英文)](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="3bda3-388">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="3bda3-389">增強 Key Vault 憑證下載和 AAD SP 的整合 ([#3003 (英文)](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="3bda3-389">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="3bda3-390">在 ‘az —version’ 中新增 Python 位置 ([#2986 (英文)](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="3bda3-390">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="3bda3-391">登入：支援在沒有訂用帳戶時進行登入 ([#2929 (英文)](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="3bda3-391">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="3bda3-392">核心：修正使用服務主體登入兩次時所發生的失敗 ([#2800 (英文)](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="3bda3-392">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="3bda3-393">核心：允許透過環境變數設定 accessTokens.json 的檔案路徑 ([#2605 (英文)](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="3bda3-393">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="3bda3-394">核心：允許將已設定的預設值套用到選擇性引數 ([#2703 (英文)](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="3bda3-394">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="3bda3-395">核心：提升效能</span><span class="sxs-lookup"><span data-stu-id="3bda3-395">core: Improved performance</span></span>
* <span data-ttu-id="3bda3-396">核心：自訂 CA 憑證 - 支援設定 REQUESTS_CA_BUNDLE 環境變數</span><span class="sxs-lookup"><span data-stu-id="3bda3-396">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="3bda3-397">核心：雲端組態 - 如果未設定「管理」端點，則使用「資源管理員」端點</span><span class="sxs-lookup"><span data-stu-id="3bda3-397">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="3bda3-398">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-398">ACS</span></span>

* <span data-ttu-id="3bda3-399">將主要和代理程式計數修正為整數，而不是字串</span><span class="sxs-lookup"><span data-stu-id="3bda3-399">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="3bda3-400">公開 'az acs create --no-wait' 和 'az acs wait' 以進行非同步建立</span><span class="sxs-lookup"><span data-stu-id="3bda3-400">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="3bda3-401">公開 'az acs create --validate' 以進行試執行驗證</span><span class="sxs-lookup"><span data-stu-id="3bda3-401">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="3bda3-402">在進行 scale 命令的 PUT 呼叫之前，先移除 Windows 設定檔 ([#2755 (英文)](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="3bda3-402">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="3bda3-403">AppService</span><span class="sxs-lookup"><span data-stu-id="3bda3-403">AppService</span></span>

* <span data-ttu-id="3bda3-404">functionapp：新增完整的 functionapp 支援，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="3bda3-404">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="3bda3-405">新增 Team Services (vsts) 作為 "appservice web source-control config" 的持續傳遞選項</span><span class="sxs-lookup"><span data-stu-id="3bda3-405">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="3bda3-406">建立 "az webapp" 以取代 "az appservice web" (用於回溯相容性，"az appservice web" 的存續期將再延續 2 個版本)</span><span class="sxs-lookup"><span data-stu-id="3bda3-406">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="3bda3-407">公開引數以在執行 webapp create 時設定部署和「執行階段堆疊」</span><span class="sxs-lookup"><span data-stu-id="3bda3-407">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="3bda3-408">公開 "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="3bda3-408">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="3bda3-409">支援設定連接字串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="3bda3-409">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="3bda3-410">支援附帶預覽功能的位置交換</span><span class="sxs-lookup"><span data-stu-id="3bda3-410">support slot swap with preview</span></span>
* <span data-ttu-id="3bda3-411">修飾來自 appservice 命令的錯誤 ([#2948 (英文)](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="3bda3-411">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="3bda3-412">使用 App Service 方案的資源群組來進行憑證作業 ([#2750 (英文)](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="3bda3-412">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="3bda3-413">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3bda3-413">CosmosDB</span></span>

* <span data-ttu-id="3bda3-414">將 documentdb 模組重新命名為 cosmosdb。</span><span class="sxs-lookup"><span data-stu-id="3bda3-414">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="3bda3-415">新增對 documentdb 資料層 API 的支援：資料庫和集合管理</span><span class="sxs-lookup"><span data-stu-id="3bda3-415">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="3bda3-416">新增對在資料庫帳戶上啟用自動容錯移轉的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-416">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="3bda3-417">新增對新一致性原則 ConsistentPrefix 的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-417">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="3bda3-418">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3bda3-418">Data Lake Analytics</span></span>

* <span data-ttu-id="3bda3-419">修正依工作清單的結果和狀態篩選會導致擲回錯誤的 Bug。</span><span class="sxs-lookup"><span data-stu-id="3bda3-419">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="3bda3-420">新增對下列新類別目錄項目類型的支援：套件。</span><span class="sxs-lookup"><span data-stu-id="3bda3-420">Add support for new catalog item type: package.</span></span> <span data-ttu-id="3bda3-421">透過 `az dla catalog package` 進行存取</span><span class="sxs-lookup"><span data-stu-id="3bda3-421">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="3bda3-422">能夠從資料庫內列出下列類別目錄項目 (不需指定結構描述)：</span><span class="sxs-lookup"><span data-stu-id="3bda3-422">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="3bda3-423">資料表</span><span class="sxs-lookup"><span data-stu-id="3bda3-423">Table</span></span>
  * <span data-ttu-id="3bda3-424">資料表值函式</span><span class="sxs-lookup"><span data-stu-id="3bda3-424">Table valued function</span></span>
  * <span data-ttu-id="3bda3-425">檢視</span><span class="sxs-lookup"><span data-stu-id="3bda3-425">View</span></span>
  * <span data-ttu-id="3bda3-426">資料表統計資料。</span><span class="sxs-lookup"><span data-stu-id="3bda3-426">Table Statistics.</span></span> <span data-ttu-id="3bda3-427">這也可以使用結構描述來列出，但不需要指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="3bda3-427">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="3bda3-428">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3bda3-428">Data Lake Store</span></span>

* <span data-ttu-id="3bda3-429">更新基礎檔案系統 SDK 的版本，以提供更佳的支援來處理伺服器端節流情況。</span><span class="sxs-lookup"><span data-stu-id="3bda3-429">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="3bda3-430">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="3bda3-430">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="3bda3-431">遺失 access show 的說明。</span><span class="sxs-lookup"><span data-stu-id="3bda3-431">missed help for access show.</span></span> <span data-ttu-id="3bda3-432">將新增此說明。</span><span class="sxs-lookup"><span data-stu-id="3bda3-432">adding it.</span></span> <span data-ttu-id="3bda3-433">([#2743 (英文)](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="3bda3-433">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="3bda3-434">尋找</span><span class="sxs-lookup"><span data-stu-id="3bda3-434">Find</span></span>

* <span data-ttu-id="3bda3-435">改善搜尋結果，並允許進行搜尋索引版本控制</span><span class="sxs-lookup"><span data-stu-id="3bda3-435">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="3bda3-436">KeyVault</span><span class="sxs-lookup"><span data-stu-id="3bda3-436">KeyVault</span></span>

* <span data-ttu-id="3bda3-437">BC：`az keyvault certificate download`將 -e 從字串或二進位變更為 PEM 或 DER，來以更佳的方式代表選項</span><span class="sxs-lookup"><span data-stu-id="3bda3-437">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="3bda3-438">BC：從 `keyvault certificate create` 中移除 --expires 和 --not-before，因為服務不支援這些參數。</span><span class="sxs-lookup"><span data-stu-id="3bda3-438">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="3bda3-439">在 `keyvault certificate create` 中新增 --validity 參數，以選擇性地覆寫 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="3bda3-439">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="3bda3-440">修正 `keyvault certificate get-default-policy` 中公開 'expires' 和 'not_before' 但未公開 'validity_in_months' 的問題。</span><span class="sxs-lookup"><span data-stu-id="3bda3-440">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="3bda3-441">用於匯入 pem 和 pfx 的 keyvault 修正 ([#2754 (英文)](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="3bda3-441">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="3bda3-442">實驗室</span><span class="sxs-lookup"><span data-stu-id="3bda3-442">Lab</span></span>

* <span data-ttu-id="3bda3-443">新增適用於實驗室中環境的 create、show、delete 及 list 命令。</span><span class="sxs-lookup"><span data-stu-id="3bda3-443">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="3bda3-444">新增 show 和 list 命令以檢視實驗室中的 ARM 範本。</span><span class="sxs-lookup"><span data-stu-id="3bda3-444">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="3bda3-445">在 `az lab vm list` 中新增 --environment 旗標，以在實驗室中依環境篩選 VM。</span><span class="sxs-lookup"><span data-stu-id="3bda3-445">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="3bda3-446">新增便利命令 `az lab formula export-artifacts` 以匯出實驗室公式內的構件結構。</span><span class="sxs-lookup"><span data-stu-id="3bda3-446">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="3bda3-447">新增命令以管理實驗室內的密碼。</span><span class="sxs-lookup"><span data-stu-id="3bda3-447">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="3bda3-448">監視</span><span class="sxs-lookup"><span data-stu-id="3bda3-448">Monitor</span></span>

* <span data-ttu-id="3bda3-449">Bug 修正：建立 `az alert-rules create` 的 `--actions` 模型以取用 JSON 字串 ([#3009 (英文)](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="3bda3-449">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="3bda3-450">Bug 修正：diagnostic-settings create 不接受來自 show 命令的記錄/計量 ([#2913 (英文)](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="3bda3-450">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="3bda3-451">網路</span><span class="sxs-lookup"><span data-stu-id="3bda3-451">Network</span></span>

* <span data-ttu-id="3bda3-452">新增 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="3bda3-452">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="3bda3-453">新增對 `network watcher packet-capture create` 之 `--filters` 參數的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-453">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="3bda3-454">新增對「應用程式閘道」連線清空的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-454">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="3bda3-455">新增對「應用程式閘道」WAF 規則集組態的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-455">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="3bda3-456">新增對 ExpressRoute 路由篩選和規則的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-456">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="3bda3-457">新增對 TrafficManager 地理路由的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-457">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="3bda3-458">新增對 VPN 連線原則型流量選取器的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-458">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="3bda3-459">新增對 VPN 連線 IPSec 原則的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-459">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="3bda3-460">修正 `vpn-connection create` 搭配使用 `--no-wait` 或 `--validate` 參數時的 Bug。</span><span class="sxs-lookup"><span data-stu-id="3bda3-460">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="3bda3-461">新增對「主動-主動」VNet 閘道的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-461">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="3bda3-462">從 `network vpn-connection list/show` 命令移除 Null 值。</span><span class="sxs-lookup"><span data-stu-id="3bda3-462">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="3bda3-463">BC：修正 `vpn-connection create` 之輸出中的 Bug</span><span class="sxs-lookup"><span data-stu-id="3bda3-463">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="3bda3-464">修正未正確剖析 'vpn-connection create' 之 '--key-length' 引數的 Bug。</span><span class="sxs-lookup"><span data-stu-id="3bda3-464">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="3bda3-465">修正 `dns zone import` 中未正確匯入記錄的 Bug。</span><span class="sxs-lookup"><span data-stu-id="3bda3-465">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="3bda3-466">修正 `traffic-manager endpoint update` 無法運作的 Bug。</span><span class="sxs-lookup"><span data-stu-id="3bda3-466">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="3bda3-467">新增 'network watcher' 預覽命令。</span><span class="sxs-lookup"><span data-stu-id="3bda3-467">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="3bda3-468">設定檔</span><span class="sxs-lookup"><span data-stu-id="3bda3-468">Profile</span></span>

* <span data-ttu-id="3bda3-469">支援在找不到訂用帳戶時進行登入 ([#2560 (英文)](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="3bda3-469">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="3bda3-470">在 az account set --subscription 中支援短參數名稱 ([#2980 (英文)](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="3bda3-470">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="3bda3-471">Redis</span><span class="sxs-lookup"><span data-stu-id="3bda3-471">Redis</span></span>

* <span data-ttu-id="3bda3-472">新增 update 命令，這也會為 redis 快取新增調整能力</span><span class="sxs-lookup"><span data-stu-id="3bda3-472">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="3bda3-473">取代 'update-settings' 命令。</span><span class="sxs-lookup"><span data-stu-id="3bda3-473">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="3bda3-474">資源</span><span class="sxs-lookup"><span data-stu-id="3bda3-474">Resource</span></span>

* <span data-ttu-id="3bda3-475">新增 managedapp 和 managedapp definition 命令 ([#2985 (英文)](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="3bda3-475">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="3bda3-476">支援 'provider operation' 命令 ([#2908 (英文)](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="3bda3-476">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="3bda3-477">支援一般 resource create ([#2606 (英文)](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="3bda3-477">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="3bda3-478">修正資源剖析和 api 版本查詢。</span><span class="sxs-lookup"><span data-stu-id="3bda3-478">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="3bda3-479">([#2781 (英文)](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="3bda3-479">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="3bda3-480">新增 az lock update 的文件。</span><span class="sxs-lookup"><span data-stu-id="3bda3-480">Add docs for az lock update.</span></span> <span data-ttu-id="3bda3-481">([#2702 (英文)](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="3bda3-481">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="3bda3-482">如果您嘗試列出不存在之群組的資源，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bda3-482">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="3bda3-483">([#2769 (英文)](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="3bda3-483">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="3bda3-484">[計算] 修正 VMSS 和 VM 可用性設定組更新的相關問題。</span><span class="sxs-lookup"><span data-stu-id="3bda3-484">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="3bda3-485">([#2773 (英文)](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="3bda3-485">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="3bda3-486">修正 parent-resource-path 為 None 時的 lock create 和 delete ([#2742 (英文)](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="3bda3-486">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="3bda3-487">角色</span><span class="sxs-lookup"><span data-stu-id="3bda3-487">Role</span></span>

* <span data-ttu-id="3bda3-488">create-for-rbac：確保 SP 的結束日期不會超過憑證的到期日 ([#2989 (英文)](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="3bda3-488">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="3bda3-489">RBAC：新增對 'ad group' 的完整支援 ([#2016 (英文)](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="3bda3-489">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="3bda3-490">角色：修正 role definition update 上的問題 ([#2745 (英文)](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="3bda3-490">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="3bda3-491">create-for-rbac：確保系統會挑選使用者提供的密碼</span><span class="sxs-lookup"><span data-stu-id="3bda3-491">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="3bda3-492">SQL</span><span class="sxs-lookup"><span data-stu-id="3bda3-492">SQL</span></span>

* <span data-ttu-id="3bda3-493">新增 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="3bda3-493">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="3bda3-494">SQL - 能夠直接連接到資源提供者 ([#2832 (英文)](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="3bda3-494">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="3bda3-495">儲存體</span><span class="sxs-lookup"><span data-stu-id="3bda3-495">Storage</span></span>

* <span data-ttu-id="3bda3-496">`storage account create` 之資源群組位置的預設位置。</span><span class="sxs-lookup"><span data-stu-id="3bda3-496">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="3bda3-497">新增對遞增 blob 複製的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-497">Add support for incremental blob copy</span></span>
* <span data-ttu-id="3bda3-498">新增對大型區塊 blob 上傳的支援</span><span class="sxs-lookup"><span data-stu-id="3bda3-498">Add support for large block blob upload</span></span>
* <span data-ttu-id="3bda3-499">當要上傳的檔案大於 200 GB 時，將區塊大小變更為 100 MB</span><span class="sxs-lookup"><span data-stu-id="3bda3-499">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="3bda3-500">VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-500">VM</span></span>

* <span data-ttu-id="3bda3-501">avail-set：將 UD&FD 網域計數設定為選用</span><span class="sxs-lookup"><span data-stu-id="3bda3-501">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="3bda3-502">注意：主權雲端中的 VM 命令。請避免使用受管理磁碟相關的功能，包括下列功能：</span><span class="sxs-lookup"><span data-stu-id="3bda3-502">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="3bda3-503">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="3bda3-503">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="3bda3-504">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="3bda3-504">az vm/vmss disk</span></span>
  3. <span data-ttu-id="3bda3-505">在 "az vm/vmss create" 內，請使用 "—use-unmanaged-disk" 來避免使用受管理的磁碟。其他命令應該可運作</span><span class="sxs-lookup"><span data-stu-id="3bda3-505">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="3bda3-506">vm/vmss：改進產生 SSH 金鑰組時的警告文字</span><span class="sxs-lookup"><span data-stu-id="3bda3-506">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="3bda3-507">vm/vmss：支援從需要方案資訊的市場映像進行建立 ([#1209 (英文)](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="3bda3-507">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="3bda3-508">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-508">April 3, 2017</span></span>

<span data-ttu-id="3bda3-509">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="3bda3-509">Version 2.0.2</span></span>

<span data-ttu-id="3bda3-510">在這一版中，我們發行了 ACR、Batch、KeyVault 和 SQL 元件。</span><span class="sxs-lookup"><span data-stu-id="3bda3-510">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="3bda3-511">核心</span><span class="sxs-lookup"><span data-stu-id="3bda3-511">Core</span></span>

* <span data-ttu-id="3bda3-512">將 ACR、實驗室、監視及尋找模組新增至預設清單。</span><span class="sxs-lookup"><span data-stu-id="3bda3-512">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="3bda3-513">Login︰略過錯誤的租用戶 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="3bda3-513">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="3bda3-514">Login︰將預設訂用帳戶設定為具有「已啟用」狀態的訂用帳戶 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="3bda3-514">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="3bda3-515">將 wait 命令和 --no-wait 支援新增至多個命令 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="3bda3-515">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="3bda3-516">Core︰支援使用憑證的服務主體登入 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="3bda3-516">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="3bda3-517">新增遺漏範本參數的提示。</span><span class="sxs-lookup"><span data-stu-id="3bda3-517">Add prompting for missing template parameters.</span></span> <span data-ttu-id="3bda3-518">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="3bda3-518">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="3bda3-519">支援設定諸如預設資源群組、預設 web、預設 VM 等常見引數的預設值</span><span class="sxs-lookup"><span data-stu-id="3bda3-519">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="3bda3-520">支援登入特定的租用戶</span><span class="sxs-lookup"><span data-stu-id="3bda3-520">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="3bda3-521">ACS</span><span class="sxs-lookup"><span data-stu-id="3bda3-521">ACS</span></span>

* <span data-ttu-id="3bda3-522">[ACS] 新增設定預設 ACS 叢集的支援 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="3bda3-522">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="3bda3-523">新增 SSH 金鑰密碼提示的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-523">Add support for ssh key password prompting.</span></span> <span data-ttu-id="3bda3-524">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="3bda3-524">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="3bda3-525">新增 Windows 叢集的支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-525">Add support for windows clusters.</span></span> <span data-ttu-id="3bda3-526">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="3bda3-526">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="3bda3-527">將角色從擁有者切換為參與者。</span><span class="sxs-lookup"><span data-stu-id="3bda3-527">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="3bda3-528">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="3bda3-528">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="3bda3-529">AppService</span><span class="sxs-lookup"><span data-stu-id="3bda3-529">AppService</span></span>

* <span data-ttu-id="3bda3-530">appservice︰取得用於 DNS A 記錄之外部 IP 位址的支援 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="3bda3-530">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="3bda3-531">appservice︰支援繫結萬用字元憑證 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="3bda3-531">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="3bda3-532">appservice︰支援列出發行設定檔 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="3bda3-532">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="3bda3-533">AppService - 設定之後觸發原始檔控制同步處理 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="3bda3-533">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="3bda3-534">DataLake</span><span class="sxs-lookup"><span data-stu-id="3bda3-534">DataLake</span></span>

* <span data-ttu-id="3bda3-535">Data Lake Analytics 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="3bda3-535">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="3bda3-536">Data Lake Store 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="3bda3-536">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="3bda3-537">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="3bda3-537">DocuemntDB</span></span>

* <span data-ttu-id="3bda3-538">DocumentDB︰新增列出連接字串的支援 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="3bda3-538">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="3bda3-539">VM</span><span class="sxs-lookup"><span data-stu-id="3bda3-539">VM</span></span>

* <span data-ttu-id="3bda3-540">[Compute] 將 AppGateway 支援新增至虛擬機器擴展集建立 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="3bda3-540">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="3bda3-541">[VM/VMSS] 改良的磁碟快取支援 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="3bda3-541">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="3bda3-542">VM/VMSS︰併入入口網站所使用的認證驗證邏輯 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="3bda3-542">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="3bda3-543">新增 wait 命令和 --no-wait 支援 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="3bda3-543">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="3bda3-544">虛擬機器擴展集︰支援 * 列出跨 VM 的執行個體檢視 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="3bda3-544">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="3bda3-545">新增 VM 和虛擬機器擴展集的 --祕密 ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="3bda3-545">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="3bda3-546">可使用特殊的 VHD 來建立 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="3bda3-546">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="3bda3-547">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="3bda3-547">February 27, 2017</span></span>

<span data-ttu-id="3bda3-548">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="3bda3-548">Version 2.0.0</span></span>

<span data-ttu-id="3bda3-549">此版本的 Azure CLI 2.0 是第一個「正式運作」版本。</span><span class="sxs-lookup"><span data-stu-id="3bda3-549">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="3bda3-550">正式運作適用於下列的命令模組︰</span><span class="sxs-lookup"><span data-stu-id="3bda3-550">General availability applies to these command modules:</span></span>
- <span data-ttu-id="3bda3-551">Container Service (ACS)</span><span class="sxs-lookup"><span data-stu-id="3bda3-551">Container Service (acs)</span></span>
- <span data-ttu-id="3bda3-552">計算 (包含 Resource Manager、VM、虛擬機器擴展集、受控磁碟)</span><span class="sxs-lookup"><span data-stu-id="3bda3-552">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="3bda3-553">網路功能</span><span class="sxs-lookup"><span data-stu-id="3bda3-553">Networking</span></span>
- <span data-ttu-id="3bda3-554">儲存體</span><span class="sxs-lookup"><span data-stu-id="3bda3-554">Storage</span></span>

<span data-ttu-id="3bda3-555">這些命令模組可用在生產環境中，且受標準 Microsoft SLA 支援。</span><span class="sxs-lookup"><span data-stu-id="3bda3-555">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="3bda3-556">您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)開啟問題。</span><span class="sxs-lookup"><span data-stu-id="3bda3-556">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="3bda3-557">您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。您可以從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="3bda3-557">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="3bda3-558">這些模組中的命令很穩定，且不應該變更此版 Azure CLI 之未來版本的語法。</span><span class="sxs-lookup"><span data-stu-id="3bda3-558">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="3bda3-559">若要確認的 CLI 的版本，請使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="3bda3-559">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="3bda3-560">輸出會列出 CLI 本身的版本 (此版本中為 2.0.0)、個別的命令模組，以及您所使用的 Python 和 GCC 版本。</span><span class="sxs-lookup"><span data-stu-id="3bda3-560">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="3bda3-561">些命令模組會有 "b*n*" 或 "rc*n*" 後置詞。</span><span class="sxs-lookup"><span data-stu-id="3bda3-561">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="3bda3-562">這些命令模組仍處於預覽狀態，且未來會正式運作。</span><span class="sxs-lookup"><span data-stu-id="3bda3-562">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="3bda3-563">我們也有 CLI 的夜間預覽組建。</span><span class="sxs-lookup"><span data-stu-id="3bda3-563">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="3bda3-564">如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。</span><span class="sxs-lookup"><span data-stu-id="3bda3-564">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="3bda3-565">您可以透過下列方式來報告夜間預覽組建的問題︰</span><span class="sxs-lookup"><span data-stu-id="3bda3-565">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="3bda3-566">在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)中報告問題</span><span class="sxs-lookup"><span data-stu-id="3bda3-566">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="3bda3-567">連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="3bda3-567">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="3bda3-568">從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="3bda3-568">Provide feedback from the command line with the `az feedback` command.</span></span>

