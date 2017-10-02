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
ms.openlocfilehash: 72630c52b5e6afd69809ff19145717c0d65e0252
ms.sourcegitcommit: 3a490ae3a2a1b2e63a062806f9b720fa4c6be01e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/25/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="02df7-104">Azure CLI 2.0 版本資訊</span><span class="sxs-lookup"><span data-stu-id="02df7-104">Azure CLI 2.0 release notes</span></span>

## <a name="september-22-2017"></a><span data-ttu-id="02df7-105">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="02df7-105">September 22, 2017</span></span>

<span data-ttu-id="02df7-106">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="02df7-106">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="02df7-107">資源</span><span class="sxs-lookup"><span data-stu-id="02df7-107">Resource</span></span>

* <span data-ttu-id="02df7-108">已新增顯示內建原則定義的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-108">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="02df7-109">已新增建立原則定義的支援模式參數</span><span class="sxs-lookup"><span data-stu-id="02df7-109">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="02df7-110">已新增對於 `managedapp definition create` UI 定義及範本的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-110">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="02df7-111">[重大變更] 已變更 `managedapp` 資源類型，從 `appliances` 變為 `applications`，且從 `applianceDefinitions` 變為 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="02df7-111">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="02df7-112">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-112">Network</span></span>

* <span data-ttu-id="02df7-113">已新增可用性區域，以支援 `network lb` 和 `network public-ip` 子命令</span><span class="sxs-lookup"><span data-stu-id="02df7-113">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="02df7-114">已新增對 `express-route` 的 IPv6 Microsoft 對等互連支援</span><span class="sxs-lookup"><span data-stu-id="02df7-114">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="02df7-115">已新增 `asg` 應用程式安全性群組命令</span><span class="sxs-lookup"><span data-stu-id="02df7-115">Added `asg` application security group commands</span></span>
* <span data-ttu-id="02df7-116">將 `--application-security-groups` 引數新增至 `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="02df7-116">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="02df7-117">已將 `--source-asgs` 和 `--destination-asgs` 引數新增至 `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="02df7-117">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="02df7-118">已將 `--ddos-protection` 和 `--vm-protection` 引數新增至 `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="02df7-118">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="02df7-119">已新增 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-119">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-120">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-120">Storage</span></span>

* <span data-ttu-id="02df7-121">已修正更新 SDK 後 `storage account network-rule` 命令可能會失敗的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-121">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="02df7-122">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="02df7-122">Eventgrid</span></span>

* <span data-ttu-id="02df7-123">已更新 Azure Event Grid Python SDK 以使用較新的 API 版本 "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="02df7-123">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="02df7-124">SQL</span><span class="sxs-lookup"><span data-stu-id="02df7-124">SQL</span></span>

* <span data-ttu-id="02df7-125">已將 `sql server list` 引數 `--resource-group` 變更為可選。</span><span class="sxs-lookup"><span data-stu-id="02df7-125">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="02df7-126">如果未指定，會傳回訂用帳戶中所有的 sql 伺服器</span><span class="sxs-lookup"><span data-stu-id="02df7-126">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="02df7-127">已將 `--no-wait` 參數新增至 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="02df7-127">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="02df7-128">Keyvault</span><span class="sxs-lookup"><span data-stu-id="02df7-128">Keyvault</span></span>

* <span data-ttu-id="02df7-129">已新增從 proxy 後方支援 Keyvault 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-129">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-130">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-130">VM</span></span>

* <span data-ttu-id="02df7-131">已新增 `[vm|vmss|disk] create` 的可用性區域支援</span><span class="sxs-lookup"><span data-stu-id="02df7-131">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="02df7-132">已修正使用 `--app-gateway ID` 與 `vmss create` 會導致失敗的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-132">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="02df7-133">已將引數 `--asgs` 新增至 `vm create`</span><span class="sxs-lookup"><span data-stu-id="02df7-133">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="02df7-134">已新增使用 `vm run-command` 在 VM 上執行命令的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-134">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="02df7-135">[預覽] 已新增使用 `vmss encryption` 加密 VMSS 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-135">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="02df7-136">已新增使用 `vm perform-maintenance` 在 VM 上執行維護工作的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-136">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-137">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-137">ACS</span></span>

* <span data-ttu-id="02df7-138">[預覽] 已針對 ACS 預覽區域，將 `--orchestrator-release` 引數新增至 `acs create`</span><span class="sxs-lookup"><span data-stu-id="02df7-138">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-139">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-139">Appservice</span></span>

* <span data-ttu-id="02df7-140">已新增使用 `webapp auth [update|show]` 更新並顯示驗證設定的功能</span><span class="sxs-lookup"><span data-stu-id="02df7-140">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="02df7-141">備份</span><span class="sxs-lookup"><span data-stu-id="02df7-141">Backup</span></span>

* <span data-ttu-id="02df7-142">預覽版本</span><span class="sxs-lookup"><span data-stu-id="02df7-142">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="02df7-143">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="02df7-143">September 11, 2017</span></span>

<span data-ttu-id="02df7-144">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="02df7-144">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="02df7-145">核心</span><span class="sxs-lookup"><span data-stu-id="02df7-145">Core</span></span>

* <span data-ttu-id="02df7-146">啟用命令模組以在遙測中設定自己的相互關聯識別碼</span><span class="sxs-lookup"><span data-stu-id="02df7-146">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="02df7-147">修正當遙測設為診斷模式時的 JSON 傾印問題</span><span class="sxs-lookup"><span data-stu-id="02df7-147">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-148">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-148">Acs</span></span>

* <span data-ttu-id="02df7-149">已新增 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-149">Added `acs list-locations` command</span></span>
* <span data-ttu-id="02df7-150">讓 `ssh-key-file` 隨附預期的預設值</span><span class="sxs-lookup"><span data-stu-id="02df7-150">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-151">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-151">Appservice</span></span>

* <span data-ttu-id="02df7-152">新增在資源群組中建立 Web 應用程式，而非在作用中服務計劃中建立 Web 應用程式的功能</span><span class="sxs-lookup"><span data-stu-id="02df7-152">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="02df7-153">CDN</span><span class="sxs-lookup"><span data-stu-id="02df7-153">CDN</span></span>

* <span data-ttu-id="02df7-154">修正 `cdn custom-domain create` 的「CustomDomain 無法互動」錯誤。</span><span class="sxs-lookup"><span data-stu-id="02df7-154">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="02df7-155">分機</span><span class="sxs-lookup"><span data-stu-id="02df7-155">Extension</span></span>

* <span data-ttu-id="02df7-156">初始版本。</span><span class="sxs-lookup"><span data-stu-id="02df7-156">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="02df7-157">Keyvault</span><span class="sxs-lookup"><span data-stu-id="02df7-157">Keyvault</span></span>

* <span data-ttu-id="02df7-158">修正對 `keyvault set-policy` 的權限區分大小寫的問題。</span><span class="sxs-lookup"><span data-stu-id="02df7-158">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="02df7-159">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-159">Network</span></span>

* <span data-ttu-id="02df7-160">已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="02df7-160">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="02df7-161">己針對 `vnet subnet create/update` 將 `--private-access-services` 引數重新命名為 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="02df7-161">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="02df7-162">已將多個 IP 和連接埠範圍的支援新增至 `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="02df7-162">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="02df7-163">已將 SKU 的支援新增至 `lb create`</span><span class="sxs-lookup"><span data-stu-id="02df7-163">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="02df7-164">已將 SKU 的支援新增至 `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="02df7-164">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="02df7-165">資源</span><span class="sxs-lookup"><span data-stu-id="02df7-165">Resource</span></span>

* <span data-ttu-id="02df7-166">允許在 `policy definition create` 及 `policy definition update` 中傳送資源原則參數定義</span><span class="sxs-lookup"><span data-stu-id="02df7-166">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="02df7-167">允許為 `policy assignment create` 傳送參數值</span><span class="sxs-lookup"><span data-stu-id="02df7-167">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="02df7-168">允許為所有參數傳送 JSON 或檔案</span><span class="sxs-lookup"><span data-stu-id="02df7-168">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="02df7-169">遞增的 API 版本</span><span class="sxs-lookup"><span data-stu-id="02df7-169">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="02df7-170">SQL</span><span class="sxs-lookup"><span data-stu-id="02df7-170">SQL</span></span>

* <span data-ttu-id="02df7-171">已新增 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-171">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-172">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-172">VM</span></span>

* <span data-ttu-id="02df7-173">已修正：在提供 `--scope` 之前不指派存取權</span><span class="sxs-lookup"><span data-stu-id="02df7-173">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="02df7-174">已修正：使用相同延伸模組命名作為入口網站</span><span class="sxs-lookup"><span data-stu-id="02df7-174">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="02df7-175">已從 `[vm|vmss] create` 輸出移除 `subscription`</span><span class="sxs-lookup"><span data-stu-id="02df7-175">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="02df7-176">已修正：`[vm|vmss] create` 儲存體 SKU 不會套用至搭配映像的資料磁碟</span><span class="sxs-lookup"><span data-stu-id="02df7-176">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="02df7-177">已修正：`vm format-secret --secrets` 不會接受新行分隔識別碼</span><span class="sxs-lookup"><span data-stu-id="02df7-177">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="02df7-178">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="02df7-178">August 31, 2017</span></span>

<span data-ttu-id="02df7-179">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="02df7-179">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="02df7-180">Keyvault</span><span class="sxs-lookup"><span data-stu-id="02df7-180">Keyvault</span></span>

* <span data-ttu-id="02df7-181">修正試著自動使用 `secret download` 解析祕密編碼時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-181">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="02df7-182">Sf</span><span class="sxs-lookup"><span data-stu-id="02df7-182">Sf</span></span>

* <span data-ttu-id="02df7-183">取代所有命令，以利於 Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="02df7-183">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-184">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-184">Storage</span></span>

* <span data-ttu-id="02df7-185">修正無法在不支援 NetworkACL 功能的區域中建立儲存體帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-185">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="02df7-186">若指定內容類型和內容編碼，則判斷 Blob 及檔案上傳期間的內容類型及內容編碼</span><span class="sxs-lookup"><span data-stu-id="02df7-186">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="02df7-187">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="02df7-187">August 28, 2017</span></span>

<span data-ttu-id="02df7-188">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="02df7-188">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="02df7-189">CLI</span><span class="sxs-lookup"><span data-stu-id="02df7-189">CLI</span></span>

* <span data-ttu-id="02df7-190">已將法律注意事項新增至 `--version`。</span><span class="sxs-lookup"><span data-stu-id="02df7-190">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-191">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-191">ACS</span></span>

* <span data-ttu-id="02df7-192">已更正預覽區域。</span><span class="sxs-lookup"><span data-stu-id="02df7-192">Corrected preview regions.</span></span>
* <span data-ttu-id="02df7-193">已正確格式化預設 `dns_name_prefix`。</span><span class="sxs-lookup"><span data-stu-id="02df7-193">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="02df7-194">最佳化的 acs 命令輸出。</span><span class="sxs-lookup"><span data-stu-id="02df7-194">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-195">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-195">Appservice</span></span>

* <span data-ttu-id="02df7-196">[新變更] 已修正 `az webapp config appsettings [delete|set]` 輸出中的不一致</span><span class="sxs-lookup"><span data-stu-id="02df7-196">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="02df7-197">已針對 `az webapp config container set --docker-custom-image-name` 新增 `-i` 的新別名</span><span class="sxs-lookup"><span data-stu-id="02df7-197">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="02df7-198">已公開 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="02df7-198">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="02df7-199">已公開 `az webapp delete` 中的新引數，可保留應用程式服務計劃、計量或 DNS 註冊</span><span class="sxs-lookup"><span data-stu-id="02df7-199">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="02df7-200">已修正：正確偵測到位置設定</span><span class="sxs-lookup"><span data-stu-id="02df7-200">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="02df7-201">IoT</span><span class="sxs-lookup"><span data-stu-id="02df7-201">IoT</span></span>

* <span data-ttu-id="02df7-202">已修正 #3934：建立原則時無法再清除現有的原則</span><span class="sxs-lookup"><span data-stu-id="02df7-202">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="02df7-203">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-203">Network</span></span>

* <span data-ttu-id="02df7-204">[新變更] 已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="02df7-204">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="02df7-205">[新變更] 已將 `--private-access-services` 選項重新命名為適用於 `vnet subnet [create|update]` 的 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="02df7-205">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="02df7-206">已將多個 IP 和連接埠範圍的支援新增至 `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="02df7-206">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="02df7-207">已將 SKU 的支援新增至 `lb create`</span><span class="sxs-lookup"><span data-stu-id="02df7-207">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="02df7-208">已將 SKU 的支援新增至 `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="02df7-208">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="02df7-209">設定檔</span><span class="sxs-lookup"><span data-stu-id="02df7-209">Profile</span></span>

* <span data-ttu-id="02df7-210">已公開 `--msi` 和 `--msi-port`，可使用虛擬機器的身分識別登入</span><span class="sxs-lookup"><span data-stu-id="02df7-210">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="02df7-211">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="02df7-211">Service Fabric</span></span>

* <span data-ttu-id="02df7-212">預覽版本</span><span class="sxs-lookup"><span data-stu-id="02df7-212">Preview release</span></span>
* <span data-ttu-id="02df7-213">簡化的登錄使用者/命令的密碼規則</span><span class="sxs-lookup"><span data-stu-id="02df7-213">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="02df7-214">已修正使用者即使在參數中傳遞之後的密碼提示</span><span class="sxs-lookup"><span data-stu-id="02df7-214">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="02df7-215">已新增空白 `registry_cred` 的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-215">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-216">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-216">Storage</span></span>

* <span data-ttu-id="02df7-217">已啟用設定 blob 層</span><span class="sxs-lookup"><span data-stu-id="02df7-217">Enabled setting blob tier</span></span>
* <span data-ttu-id="02df7-218">已將 `--bypass` 和 `--default-action` 引數新增至 `storage account [create|update]` 以支援服務通道</span><span class="sxs-lookup"><span data-stu-id="02df7-218">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="02df7-219">新增的命令可將 VNET 規則和以 IP 作為基礎的規則新增至 `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="02df7-219">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="02df7-220">透過客戶管理的金鑰啟用服務加密</span><span class="sxs-lookup"><span data-stu-id="02df7-220">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="02df7-221">[新變更] 已將 `--encryption` 選項重新命名為適用於 `az storage account create and az storage account update` 命令的 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="02df7-221">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="02df7-222">已修正 #4220：`az storage account update encryption` - 語法不相符</span><span class="sxs-lookup"><span data-stu-id="02df7-222">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-223">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-223">VM</span></span>

* <span data-ttu-id="02df7-224">已修正使用 `--instance-id *` 時會顯示 `vmss get-instance-view` 的額外錯誤資訊的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-224">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="02df7-225">已將 `--lb-sku` 的支援新增至 `vmss create`：</span><span class="sxs-lookup"><span data-stu-id="02df7-225">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="02df7-226">從 `[vm|vmss] create` 的系統管理員名稱封鎖清單移除人力名稱</span><span class="sxs-lookup"><span data-stu-id="02df7-226">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="02df7-227">已修正在無法從映像擷取計劃資訊時，`[vm|vmss] create` 會擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-227">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="02df7-228">已修正使用內部 LB 建立 vmms scaleset 時的損毀</span><span class="sxs-lookup"><span data-stu-id="02df7-228">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="02df7-229">已修正 `--no-wait` 引數無法與 `vm availability-set create` 搭配使用的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-229">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="02df7-230">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="02df7-230">August 15, 2017</span></span>

<span data-ttu-id="02df7-231">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="02df7-231">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-232">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-232">ACS</span></span>

* <span data-ttu-id="02df7-233">已更正 kubernetes 的 sshMaster0 連接埠號碼</span><span class="sxs-lookup"><span data-stu-id="02df7-233">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-234">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-234">Appservice</span></span>

* <span data-ttu-id="02df7-235">已修正建立以新 git 作為基礎的 Linux WebApp 時的例外狀況</span><span class="sxs-lookup"><span data-stu-id="02df7-235">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="02df7-236">Event Grid</span><span class="sxs-lookup"><span data-stu-id="02df7-236">Event Grid</span></span>

* <span data-ttu-id="02df7-237">已新增 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="02df7-237">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="02df7-238">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="02df7-238">August 11, 2017</span></span>

<span data-ttu-id="02df7-239">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="02df7-239">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-240">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-240">ACS</span></span>

* <span data-ttu-id="02df7-241">新增更多預覽區域</span><span class="sxs-lookup"><span data-stu-id="02df7-241">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="02df7-242">批次</span><span class="sxs-lookup"><span data-stu-id="02df7-242">Batch</span></span>

* <span data-ttu-id="02df7-243">更新為 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="02df7-243">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="02df7-244">已新增新的命令顯示作業的工作計數</span><span class="sxs-lookup"><span data-stu-id="02df7-244">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="02df7-245">已修正資源檔案 SAS URL 處理中的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-245">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="02df7-246">Batch 帳戶端點現在支援選擇性的 'https://' 前置詞</span><span class="sxs-lookup"><span data-stu-id="02df7-246">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="02df7-247">支援將超過 100 個工作的清單新增至作業</span><span class="sxs-lookup"><span data-stu-id="02df7-247">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="02df7-248">已新增載入擴充功能命令模組的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="02df7-248">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="02df7-249">元件</span><span class="sxs-lookup"><span data-stu-id="02df7-249">Component</span></span>

* <span data-ttu-id="02df7-250">已新增對 'az component' 命令的取代警告</span><span class="sxs-lookup"><span data-stu-id="02df7-250">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="02df7-251">容器</span><span class="sxs-lookup"><span data-stu-id="02df7-251">Container</span></span>

* <span data-ttu-id="02df7-252">`create`：已修正環境變數內不允許等號的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-252">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="02df7-253">資料湖存放區</span><span class="sxs-lookup"><span data-stu-id="02df7-253">Data Lake Store</span></span>

* <span data-ttu-id="02df7-254">已啟用進度控制項</span><span class="sxs-lookup"><span data-stu-id="02df7-254">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="02df7-255">Event Grid</span><span class="sxs-lookup"><span data-stu-id="02df7-255">Event Grid</span></span>

* <span data-ttu-id="02df7-256">初始版本</span><span class="sxs-lookup"><span data-stu-id="02df7-256">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="02df7-257">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-257">Network</span></span>

* <span data-ttu-id="02df7-258">`lb`：已修正省略某些子資源名稱時未正確解析的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-258">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="02df7-259">`application-gateway {subresource} delete`：已修正無法接受 `--no-wait` 的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-259">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="02df7-260">`application-gateway http-settings update`：已修正無法關閉 `--connection-draining-timeout` 的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-260">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="02df7-261">已修正非預期關鍵字引數 `sa_data_size_kilobyes` 與 `az network vpn-connection ipsec-policy add` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-261">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="02df7-262">設定檔</span><span class="sxs-lookup"><span data-stu-id="02df7-262">Profile</span></span>

* <span data-ttu-id="02df7-263">`account list`：已新增 `--refresh`，可從伺服器同步處理最新的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="02df7-263">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-264">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-264">Storage</span></span>

* <span data-ttu-id="02df7-265">使用指派身分識別的系統來啟用更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="02df7-265">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-266">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-266">VM</span></span>

* <span data-ttu-id="02df7-267">`availability-set`：已在轉換上公開容錯網域計數</span><span class="sxs-lookup"><span data-stu-id="02df7-267">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="02df7-268">已公開 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-268">Exposed `list-skus` command</span></span>
* <span data-ttu-id="02df7-269">支援無需建立角色指派即可指定身分識別</span><span class="sxs-lookup"><span data-stu-id="02df7-269">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="02df7-270">在連結資料磁碟上套用儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="02df7-270">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="02df7-271">已移除使用受控磁碟時的預設作業系統磁碟名稱和儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="02df7-271">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="02df7-272">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="02df7-272">July 28, 2017</span></span>

<span data-ttu-id="02df7-273">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="02df7-273">Version 2.0.12</span></span>

* <span data-ttu-id="02df7-274">已新增容器命令</span><span class="sxs-lookup"><span data-stu-id="02df7-274">Added container commands</span></span>
* <span data-ttu-id="02df7-275">已新增計費和耗用模組</span><span class="sxs-lookup"><span data-stu-id="02df7-275">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="02df7-276">核心</span><span class="sxs-lookup"><span data-stu-id="02df7-276">Core</span></span>

* <span data-ttu-id="02df7-277">包含憑證之服務主體的輸出 SDK 驗證資訊</span><span class="sxs-lookup"><span data-stu-id="02df7-277">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="02df7-278">已修正部署進度例外狀況</span><span class="sxs-lookup"><span data-stu-id="02df7-278">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="02df7-279">從目前的雲端使用 arm 端點來建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="02df7-279">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="02df7-280">clouds.config 檔案的改良並行處理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="02df7-280">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="02df7-281">重新整理每個命令執行的用戶端要求識別碼</span><span class="sxs-lookup"><span data-stu-id="02df7-281">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="02df7-282">使用正確的 SDK 設定檔建立訂用帳戶用戶端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="02df7-282">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="02df7-283">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="02df7-283">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="02df7-284">已新增透過 jmespath 查詢挑選資料表輸出欄位的支援 (#3581)</span><span class="sxs-lookup"><span data-stu-id="02df7-284">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="02df7-285">已改善剖析引數的靜音和使用手勢的附加記錄 (#3434)</span><span class="sxs-lookup"><span data-stu-id="02df7-285">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="02df7-286">使用正確的 SDK 設定檔建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="02df7-286">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="02df7-287">將所有現有的記錄檔移到最新的資料夾</span><span class="sxs-lookup"><span data-stu-id="02df7-287">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="02df7-288">已修正 VM/VMSS 建立的等冪 (#3586)</span><span class="sxs-lookup"><span data-stu-id="02df7-288">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="02df7-289">命令路徑不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="02df7-289">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="02df7-290">特定布林型別參數不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="02df7-290">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="02df7-291">支援在內部部署伺服器上登入 ADFS，例如 Azure Stack</span><span class="sxs-lookup"><span data-stu-id="02df7-291">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="02df7-292">已修正並行寫入 clouds.config (#3255)</span><span class="sxs-lookup"><span data-stu-id="02df7-292">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="02df7-293">ACR</span><span class="sxs-lookup"><span data-stu-id="02df7-293">ACR</span></span>

* <span data-ttu-id="02df7-294">已新增受控登錄的 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-294">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="02df7-295">支援受控登錄的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="02df7-295">Support SKU update for managed registries</span></span>
* <span data-ttu-id="02df7-296">已新增使用受控 SKU 的受控登錄</span><span class="sxs-lookup"><span data-stu-id="02df7-296">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="02df7-297">已新增使用 ACR Webhook 命令模組的受控登錄 Webhook</span><span class="sxs-lookup"><span data-stu-id="02df7-297">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="02df7-298">已新增使用 ACR 登入命令進行 AAD 驗證</span><span class="sxs-lookup"><span data-stu-id="02df7-298">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="02df7-299">已新增 Docker 存放庫、資訊清單及標籤的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-299">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-300">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-300">ACS</span></span>

* <span data-ttu-id="02df7-301">支援 2017-07-01 版 API</span><span class="sxs-lookup"><span data-stu-id="02df7-301">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-302">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-302">Appservice</span></span>

* <span data-ttu-id="02df7-303">已修正列出 Linux Webapp 不會傳回任何項目的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-303">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="02df7-304">支援從 ACR 擷取認證</span><span class="sxs-lookup"><span data-stu-id="02df7-304">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="02df7-305">將 `appservice web` 底下的所有命令移除</span><span class="sxs-lookup"><span data-stu-id="02df7-305">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="02df7-306">命令輸出中的遮罩 Docker 登錄密碼 (#3656)</span><span class="sxs-lookup"><span data-stu-id="02df7-306">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="02df7-307">請確定在 macOS 上使用預設瀏覽器不會發生錯誤 (#3623)</span><span class="sxs-lookup"><span data-stu-id="02df7-307">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="02df7-308">改善的 `webapp log tail` 和 `webapp log download` 說明 (#3624)</span><span class="sxs-lookup"><span data-stu-id="02df7-308">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="02df7-309">已公開可設定靜態路由的 `traffic-routing` 命令 (#3566)</span><span class="sxs-lookup"><span data-stu-id="02df7-309">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="02df7-310">已新增設定原始檔控制中的可靠性修正 (#3245)</span><span class="sxs-lookup"><span data-stu-id="02df7-310">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="02df7-311">已從適用於 Windows webapps 的 `webapp config update` 移除不支援的 `--node-version` 引數。</span><span class="sxs-lookup"><span data-stu-id="02df7-311">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="02df7-312">請改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span><span class="sxs-lookup"><span data-stu-id="02df7-312">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="02df7-313">批次</span><span class="sxs-lookup"><span data-stu-id="02df7-313">Batch</span></span>

* <span data-ttu-id="02df7-314">已更新至 Batch SDK 3.0.0 並支援集區中的低優先權 VM</span><span class="sxs-lookup"><span data-stu-id="02df7-314">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="02df7-315">已將 `pool create` 選項 `--target-dedicated` 重新命名為 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="02df7-315">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="02df7-316">已新增 `pool create` 選項 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="02df7-316">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="02df7-317">CDN</span><span class="sxs-lookup"><span data-stu-id="02df7-317">CDN</span></span>

* <span data-ttu-id="02df7-318">當 `--profile-name` 所指定的設定檔不存在時，已針對 `cdn endpoint list` 提供更好的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="02df7-318">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="02df7-319">雲端</span><span class="sxs-lookup"><span data-stu-id="02df7-319">Cloud</span></span>

* <span data-ttu-id="02df7-320">已將雲端中繼資料端點的 API 版本變更為 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="02df7-320">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="02df7-321">不需要資源庫端點</span><span class="sxs-lookup"><span data-stu-id="02df7-321">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="02df7-322">支援只向 ARM 資源管理員端點註冊雲端</span><span class="sxs-lookup"><span data-stu-id="02df7-322">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="02df7-323">已提供 `cloud set` 的選項，可在選取目前的雲端時選擇設定檔</span><span class="sxs-lookup"><span data-stu-id="02df7-323">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="02df7-324">已公開 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="02df7-324">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="02df7-325">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="02df7-325">CosmosDB</span></span>

* <span data-ttu-id="02df7-326">已修正允許使用自訂的分割區索引鍵來建立集合</span><span class="sxs-lookup"><span data-stu-id="02df7-326">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="02df7-327">已新增集合預設 TTL 的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-327">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="02df7-328">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="02df7-328">Data Lake Analytics</span></span>

* <span data-ttu-id="02df7-329">已新增在 `dla account compute-policy` 標題下計算原則管理的命令</span><span class="sxs-lookup"><span data-stu-id="02df7-329">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="02df7-330">已新增 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="02df7-330">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="02df7-331">已新增 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="02df7-331">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="02df7-332">資料湖存放區</span><span class="sxs-lookup"><span data-stu-id="02df7-332">Data Lake Store</span></span>

* <span data-ttu-id="02df7-333">已新增在 `dls account update` 中使用者受控金鑰保存庫金鑰旋轉的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-333">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="02df7-334">已更新基礎 Data Lake Store filesystem SDK 版本，從而解決效能問題</span><span class="sxs-lookup"><span data-stu-id="02df7-334">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="02df7-335">已新增命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="02df7-335">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="02df7-336">此命令會嘗試啟用使用者所提供用於將 Data Lake Store 帳戶中之資料加密的 Key Vault</span><span class="sxs-lookup"><span data-stu-id="02df7-336">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="02df7-337">互動式</span><span class="sxs-lookup"><span data-stu-id="02df7-337">Interactive</span></span>

* <span data-ttu-id="02df7-338">已使用快取的命令來改善啟動時間</span><span class="sxs-lookup"><span data-stu-id="02df7-338">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="02df7-339">已增加測試涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="02df7-339">Increased test coverage</span></span>
* <span data-ttu-id="02df7-340">已增強 '?' 手勢以便同時插入下一個命令中</span><span class="sxs-lookup"><span data-stu-id="02df7-340">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="02df7-341">已修正包含設定檔 2017-03-09-profile-preview 的互動式錯誤 (#3587)</span><span class="sxs-lookup"><span data-stu-id="02df7-341">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="02df7-342">已允許 `--version` 作為互動式模式的參數 (#3645)</span><span class="sxs-lookup"><span data-stu-id="02df7-342">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="02df7-343">停止從驗證完成擲回錯誤的互動模式 (#3570)</span><span class="sxs-lookup"><span data-stu-id="02df7-343">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="02df7-344">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="02df7-344">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="02df7-345">已新增 `--progress` 旗標</span><span class="sxs-lookup"><span data-stu-id="02df7-345">Added `--progress` flag</span></span>
* <span data-ttu-id="02df7-346">已從完成將 `--debug` 和 `--verbose` 移除</span><span class="sxs-lookup"><span data-stu-id="02df7-346">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="02df7-347">已從完成將 `interactive` 移除 (#3324)</span><span class="sxs-lookup"><span data-stu-id="02df7-347">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="02df7-348">IoT</span><span class="sxs-lookup"><span data-stu-id="02df7-348">IoT</span></span>

* <span data-ttu-id="02df7-349">已修正建立原則時無法再清除現有的原則。</span><span class="sxs-lookup"><span data-stu-id="02df7-349">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="02df7-350">(#3934)</span><span class="sxs-lookup"><span data-stu-id="02df7-350">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="02df7-351">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="02df7-351">Key vault</span></span>

* <span data-ttu-id="02df7-352">已新增金鑰保存庫復原功能的命令：</span><span class="sxs-lookup"><span data-stu-id="02df7-352">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="02df7-353">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="02df7-353">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="02df7-354">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="02df7-354">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="02df7-355">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="02df7-355">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="02df7-356">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="02df7-356">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="02df7-357">已新增服務主體金鑰保存庫整合 (#3133)</span><span class="sxs-lookup"><span data-stu-id="02df7-357">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="02df7-358">已將金鑰保存庫資料平面更新為 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="02df7-358">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="02df7-359">(#3307)</span><span class="sxs-lookup"><span data-stu-id="02df7-359">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="02df7-360">實驗室</span><span class="sxs-lookup"><span data-stu-id="02df7-360">Lab</span></span>

* <span data-ttu-id="02df7-361">已新增透過 `az lab vm claim` 在實驗室中宣告任何 VM 的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-361">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="02df7-362">已新增 `az lab vm list` 和 `az lab vm show` 的資料表輸出格式器</span><span class="sxs-lookup"><span data-stu-id="02df7-362">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="02df7-363">監視</span><span class="sxs-lookup"><span data-stu-id="02df7-363">Monitor</span></span>

* <span data-ttu-id="02df7-364">使用 `monitor autoscale-settings get-parameters-template` 命令修正範本檔案 (#3349)</span><span class="sxs-lookup"><span data-stu-id="02df7-364">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="02df7-365">已將 `monitor alert-rule-incidents list` 重新命名為 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="02df7-365">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="02df7-366">已將 `monitor alert-rule-incidents show` 重新命名為 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="02df7-366">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="02df7-367">已將 `monitor metric-defintions list` 重新命名為 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="02df7-367">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="02df7-368">已將 `monitor alert-rules` 重新命名為 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="02df7-368">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="02df7-369">已變更 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="02df7-369">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="02df7-370">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="02df7-370">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="02df7-371">新增多個參數以簡化規則建立程序</span><span class="sxs-lookup"><span data-stu-id="02df7-371">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="02df7-372">已不再需要 `location`</span><span class="sxs-lookup"><span data-stu-id="02df7-372">`location` no longer required</span></span>
  * <span data-ttu-id="02df7-373">新增目標的名稱和 ID 支援</span><span class="sxs-lookup"><span data-stu-id="02df7-373">Add name and ID support for target</span></span>
  * <span data-ttu-id="02df7-374">已移除 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="02df7-374">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="02df7-375">已不再需要將 `is-enabled` 重新命名為 `enabled`</span><span class="sxs-lookup"><span data-stu-id="02df7-375">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="02df7-376">`description` 預設值現在會以所提供的條件作為基礎</span><span class="sxs-lookup"><span data-stu-id="02df7-376">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="02df7-377">新增範例來協助釐清新格式</span><span class="sxs-lookup"><span data-stu-id="02df7-377">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="02df7-378">支援 `monitor metric` 命令的名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="02df7-378">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="02df7-379">已將便利性引數和範例新增至 `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="02df7-379">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="02df7-380">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-380">Network</span></span>

* <span data-ttu-id="02df7-381">已新增 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-381">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="02df7-382">已將 `--private-access-services` 引數新增至 `vnet subnet create` 和 `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="02df7-382">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="02df7-383">已修正 `application-gateway redirect-config create` 會失敗的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-383">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="02df7-384">已修正 `application-gateway redirect-config update` 無法與 `--no-wait` 搭配運作的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-384">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="02df7-385">已修正使用 `--servers` 引數搭配 `application-gateway address-pool create` 和 `application-gateway address-pool update` 時的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-385">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="02df7-386">已新增 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-386">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="02df7-387">已將命令新增至 `application-gateway ssl-policy`：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="02df7-387">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="02df7-388">已將引數新增至 `application-gateway ssl-policy set`：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="02df7-388">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="02df7-389">已將引數新增至 `application-gateway http-settings create` 和 `application-gateway http-settings update`：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="02df7-389">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="02df7-390">已將引數新增至 `application-gateway url-path-map create` 和 `application-gateway url-path-map update`：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="02df7-390">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="02df7-391">已將引數 `--redirect-config` 新增至 `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="02df7-391">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="02df7-392">已將 `--no-wait` 的支援新增至 `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="02df7-392">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="02df7-393">已將引數新增至 `application-gateway probe create` 和 `application-gateway probe update`：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="02df7-393">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="02df7-394">已將引數 `--redirect-config` 新增至 `application-gateway rule create` 和 `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="02df7-394">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="02df7-395">已將 `--accelerated-networking` 的支援新增至 `nic create` 和 `nic update`</span><span class="sxs-lookup"><span data-stu-id="02df7-395">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="02df7-396">已從 `nic create` 移除 `--internal-dns-name-suffix` 引數</span><span class="sxs-lookup"><span data-stu-id="02df7-396">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="02df7-397">已將 `--dns-servers` 的支援新增至 `nic update` 和 `nic create`：已新增 --dns-servers 的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-397">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="02df7-398">已修正 `local-gateway create` 忽略 `--local-address-prefixes` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-398">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="02df7-399">已將 `--dns-servers` 的支援新增至 `vnet update`</span><span class="sxs-lookup"><span data-stu-id="02df7-399">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="02df7-400">已修正使用 `express-route peering create` 時建立不含路由篩選條件之對等互連的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-400">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="02df7-401">已修正 `--provider` 和 `--bandwidth` 引數無法使用 `express-route update` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-401">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="02df7-402">已修正 `network watcher show-topology` 預設邏輯的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-402">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="02df7-403">已改良 `network list-usages` 的輸出格式</span><span class="sxs-lookup"><span data-stu-id="02df7-403">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="02df7-404">如果只有一個，請使用 `application-gateway http-listener create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="02df7-404">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="02df7-405">如果只有一個，請使用 `application-gateway rule create` 的預設位址集區、HTTP 設定和 HTTP 接聽程式</span><span class="sxs-lookup"><span data-stu-id="02df7-405">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="02df7-406">如果只有一個，請使用 `lb rule create` 的預設前端 IP 和後端集區</span><span class="sxs-lookup"><span data-stu-id="02df7-406">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="02df7-407">如果只有一個，請使用 `lb inbound-nat-rule create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="02df7-407">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="02df7-408">設定檔</span><span class="sxs-lookup"><span data-stu-id="02df7-408">Profile</span></span>

* <span data-ttu-id="02df7-409">支援使用受管理的身分識別在 VM 內部登入</span><span class="sxs-lookup"><span data-stu-id="02df7-409">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="02df7-410">支援 SDK 驗證檔案格式的 `account show` 輸出</span><span class="sxs-lookup"><span data-stu-id="02df7-410">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="02df7-411">使用 '--expanded-view' 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="02df7-411">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="02df7-412">已新增 `get-access-token` 命令，以提供原始 AAD 權杖</span><span class="sxs-lookup"><span data-stu-id="02df7-412">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="02df7-413">支援透過沒有相關聯訂用帳戶的使用者帳戶進行登入</span><span class="sxs-lookup"><span data-stu-id="02df7-413">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="02df7-414">RDBMS</span><span class="sxs-lookup"><span data-stu-id="02df7-414">RDBMS</span></span>

* <span data-ttu-id="02df7-415">支援列出跨訂用帳戶的伺服器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="02df7-415">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="02df7-416">已修正因遺漏 `% server_type` 而未處理 `%s` (#3393)</span><span class="sxs-lookup"><span data-stu-id="02df7-416">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="02df7-417">已修正文件來源對應並已新增 CI 工作以進行確認 (#3361)</span><span class="sxs-lookup"><span data-stu-id="02df7-417">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="02df7-418">已修正 MySQL 和 PostgreSQL 說明 (#3369)</span><span class="sxs-lookup"><span data-stu-id="02df7-418">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="02df7-419">資源</span><span class="sxs-lookup"><span data-stu-id="02df7-419">Resource</span></span>

* <span data-ttu-id="02df7-420">已改善遺漏 `group deployment create` 參數的提示</span><span class="sxs-lookup"><span data-stu-id="02df7-420">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="02df7-421">已改善 `--parameters KEY=VALUE` 語法的剖析</span><span class="sxs-lookup"><span data-stu-id="02df7-421">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="02df7-422">已修正無法再使用 `@<file>` 語法辨識 `group deployment create` 參數檔案的問題</span><span class="sxs-lookup"><span data-stu-id="02df7-422">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="02df7-423">支援 `resource` 和 `managedapp` 命令的 `--ids` 引數</span><span class="sxs-lookup"><span data-stu-id="02df7-423">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="02df7-424">已修正某些剖析和錯誤訊息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="02df7-424">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="02df7-425">已修正 `lock` 命令的 `--resource-type` 剖析，以接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="02df7-425">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="02df7-426">已新增範本連結範本的參數檢查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="02df7-426">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="02df7-427">已新增使用 `KEY=VALUE` 語法指定部署參數的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-427">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="02df7-428">角色</span><span class="sxs-lookup"><span data-stu-id="02df7-428">Role</span></span>

* <span data-ttu-id="02df7-429">支援 SDK 驗證檔案格式的 `create-for-rbac` 輸出</span><span class="sxs-lookup"><span data-stu-id="02df7-429">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="02df7-430">已清除在刪除服務主體時的角色指派和相關 AAD 應用程式 (#3610)</span><span class="sxs-lookup"><span data-stu-id="02df7-430">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="02df7-431">包含 `app create` 引數 `--start-date` 和 `--end-date` 描述中的時間格式</span><span class="sxs-lookup"><span data-stu-id="02df7-431">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="02df7-432">使用 `--expanded-view` 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="02df7-432">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="02df7-433">已新增金鑰保存庫整合至 `create-for-rbac` 和 `reset-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="02df7-433">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="02df7-434">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="02df7-434">Service Fabric</span></span>
* <span data-ttu-id="02df7-435">已修正應用程式中的大型檔案在上傳時被截斷的問題 (#3666)</span><span class="sxs-lookup"><span data-stu-id="02df7-435">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="02df7-436">已新增適用於 Service Fabric 命令的測試 (#3424)</span><span class="sxs-lookup"><span data-stu-id="02df7-436">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="02df7-437">已修正許多 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="02df7-437">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="02df7-438">SQL</span><span class="sxs-lookup"><span data-stu-id="02df7-438">SQL</span></span>

* <span data-ttu-id="02df7-439">已移除中斷的 `sql server create` `--identity` 參數</span><span class="sxs-lookup"><span data-stu-id="02df7-439">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="02df7-440">已從 `sql server create` 和 `sql server update` 命令輸出移除密碼值</span><span class="sxs-lookup"><span data-stu-id="02df7-440">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="02df7-441">已新增命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="02df7-441">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-442">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-442">Storage</span></span>

* <span data-ttu-id="02df7-443">已從 `storage blob list`、`storage container list` 和 `storage share list` 命令移除 `--marker` 選項 (#3745)</span><span class="sxs-lookup"><span data-stu-id="02df7-443">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="02df7-444">已啟用建立 https 專用儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="02df7-444">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="02df7-445">已更新儲存體計量、記錄和 cors 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="02df7-445">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="02df7-446">已從 CORS 新增改換措辭例外狀況訊息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="02df7-446">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="02df7-447">已將產生器轉換為下載批次命令不重複原則執行模式中的清單 (#3592)</span><span class="sxs-lookup"><span data-stu-id="02df7-447">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="02df7-448">已修正 blob 下載批次不重複原則執行問題 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="02df7-448">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-449">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-449">VM</span></span>

* <span data-ttu-id="02df7-450">支援設定 NSG</span><span class="sxs-lookup"><span data-stu-id="02df7-450">Support configuring nsg</span></span>
* <span data-ttu-id="02df7-451">已修正 DNS 伺服器未正確設定的錯誤</span><span class="sxs-lookup"><span data-stu-id="02df7-451">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="02df7-452">支援受管理的服務身分識別</span><span class="sxs-lookup"><span data-stu-id="02df7-452">Support managed service identities</span></span>
* <span data-ttu-id="02df7-453">已修正 `cmss create` 與現有負載平衡器需要 `--backend-pool-name` 的問題。</span><span class="sxs-lookup"><span data-stu-id="02df7-453">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="02df7-454">請使用開頭為 0 的 `vm image create` lun 建立 DataDisk</span><span class="sxs-lookup"><span data-stu-id="02df7-454">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="02df7-455">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="02df7-455">May 10, 2017</span></span>

<span data-ttu-id="02df7-456">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="02df7-456">Version 2.0.6</span></span>

* <span data-ttu-id="02df7-457">documentdb 已重新命名為 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="02df7-457">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="02df7-458">新增 rdbms (mysql、postgres)</span><span class="sxs-lookup"><span data-stu-id="02df7-458">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="02df7-459">包含 Data Lake Analytics 和 Data Lake Store 模組。</span><span class="sxs-lookup"><span data-stu-id="02df7-459">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="02df7-460">包含「辨識服務」模組。</span><span class="sxs-lookup"><span data-stu-id="02df7-460">Include Cognitive Services module.</span></span>
* <span data-ttu-id="02df7-461">包含 Service Fabric 模組。</span><span class="sxs-lookup"><span data-stu-id="02df7-461">Include Service Fabric module.</span></span>
* <span data-ttu-id="02df7-462">包含「互動式」模組 (az-shell 的重新命名)。</span><span class="sxs-lookup"><span data-stu-id="02df7-462">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="02df7-463">新增對 CDN 命令的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-463">Add support for CDN commands.</span></span>
* <span data-ttu-id="02df7-464">移除「容器」模組。</span><span class="sxs-lookup"><span data-stu-id="02df7-464">Remove Container module.</span></span>
* <span data-ttu-id="02df7-465">新增 'az -v' 作為 'az --version' 的捷徑 ([#2926 (英文)](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="02df7-465">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="02df7-466">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="02df7-466">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="02df7-467">核心</span><span class="sxs-lookup"><span data-stu-id="02df7-467">Core</span></span>

* <span data-ttu-id="02df7-468">核心：捕捉未註冊提供者所造成的例外狀況，並自動註冊該提供者</span><span class="sxs-lookup"><span data-stu-id="02df7-468">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="02df7-469">效能：將 adal 權杖快取保存在記憶體中，直到程序結束為止 ([#2603 (英文)](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="02df7-469">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="02df7-470">修正從十六進位指紋 -o tsv 傳回的位元組 ([#3053 (英文)](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="02df7-470">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="02df7-471">增強 Key Vault 憑證下載和 AAD SP 的整合 ([#3003 (英文)](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="02df7-471">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="02df7-472">在 ‘az —version’ 中新增 Python 位置 ([#2986 (英文)](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="02df7-472">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="02df7-473">登入：支援在沒有訂用帳戶時進行登入 ([#2929 (英文)](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="02df7-473">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="02df7-474">核心：修正使用服務主體登入兩次時所發生的失敗 ([#2800 (英文)](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="02df7-474">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="02df7-475">核心：允許透過環境變數設定 accessTokens.json 的檔案路徑 ([#2605 (英文)](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="02df7-475">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="02df7-476">核心：允許將已設定的預設值套用到選擇性引數 ([#2703 (英文)](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="02df7-476">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="02df7-477">核心：提升效能</span><span class="sxs-lookup"><span data-stu-id="02df7-477">core: Improved performance</span></span>
* <span data-ttu-id="02df7-478">核心：自訂 CA 憑證 - 支援設定 REQUESTS_CA_BUNDLE 環境變數</span><span class="sxs-lookup"><span data-stu-id="02df7-478">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="02df7-479">核心：雲端組態 - 如果未設定「管理」端點，則使用「資源管理員」端點</span><span class="sxs-lookup"><span data-stu-id="02df7-479">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="02df7-480">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-480">ACS</span></span>

* <span data-ttu-id="02df7-481">將主要和代理程式計數修正為整數，而不是字串</span><span class="sxs-lookup"><span data-stu-id="02df7-481">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="02df7-482">公開 'az acs create --no-wait' 和 'az acs wait' 以進行非同步建立</span><span class="sxs-lookup"><span data-stu-id="02df7-482">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="02df7-483">公開 'az acs create --validate' 以進行試執行驗證</span><span class="sxs-lookup"><span data-stu-id="02df7-483">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="02df7-484">在進行 scale 命令的 PUT 呼叫之前，先移除 Windows 設定檔 ([#2755 (英文)](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="02df7-484">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="02df7-485">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-485">AppService</span></span>

* <span data-ttu-id="02df7-486">functionapp：新增完整的 functionapp 支援，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="02df7-486">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="02df7-487">新增 Team Services (vsts) 作為 "appservice web source-control config" 的持續傳遞選項</span><span class="sxs-lookup"><span data-stu-id="02df7-487">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="02df7-488">建立 "az webapp" 以取代 "az appservice web" (用於回溯相容性，"az appservice web" 的存續期將再延續 2 個版本)</span><span class="sxs-lookup"><span data-stu-id="02df7-488">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="02df7-489">公開引數以在執行 webapp create 時設定部署和「執行階段堆疊」</span><span class="sxs-lookup"><span data-stu-id="02df7-489">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="02df7-490">公開 "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="02df7-490">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="02df7-491">支援設定連接字串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="02df7-491">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="02df7-492">支援附帶預覽功能的位置交換</span><span class="sxs-lookup"><span data-stu-id="02df7-492">support slot swap with preview</span></span>
* <span data-ttu-id="02df7-493">修飾來自 appservice 命令的錯誤 ([#2948 (英文)](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="02df7-493">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="02df7-494">使用 App Service 方案的資源群組來進行憑證作業 ([#2750 (英文)](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="02df7-494">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="02df7-495">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="02df7-495">CosmosDB</span></span>

* <span data-ttu-id="02df7-496">將 documentdb 模組重新命名為 cosmosdb。</span><span class="sxs-lookup"><span data-stu-id="02df7-496">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="02df7-497">新增對 documentdb 資料層 API 的支援：資料庫和集合管理</span><span class="sxs-lookup"><span data-stu-id="02df7-497">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="02df7-498">新增對在資料庫帳戶上啟用自動容錯移轉的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-498">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="02df7-499">新增對新一致性原則 ConsistentPrefix 的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-499">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="02df7-500">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="02df7-500">Data Lake Analytics</span></span>

* <span data-ttu-id="02df7-501">修正依工作清單的結果和狀態篩選會導致擲回錯誤的 Bug。</span><span class="sxs-lookup"><span data-stu-id="02df7-501">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="02df7-502">新增對下列新類別目錄項目類型的支援：套件。</span><span class="sxs-lookup"><span data-stu-id="02df7-502">Add support for new catalog item type: package.</span></span> <span data-ttu-id="02df7-503">透過 `az dla catalog package` 進行存取</span><span class="sxs-lookup"><span data-stu-id="02df7-503">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="02df7-504">能夠從資料庫內列出下列類別目錄項目 (不需指定結構描述)：</span><span class="sxs-lookup"><span data-stu-id="02df7-504">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="02df7-505">資料表</span><span class="sxs-lookup"><span data-stu-id="02df7-505">Table</span></span>
  * <span data-ttu-id="02df7-506">資料表值函式</span><span class="sxs-lookup"><span data-stu-id="02df7-506">Table valued function</span></span>
  * <span data-ttu-id="02df7-507">檢視</span><span class="sxs-lookup"><span data-stu-id="02df7-507">View</span></span>
  * <span data-ttu-id="02df7-508">資料表統計資料。</span><span class="sxs-lookup"><span data-stu-id="02df7-508">Table Statistics.</span></span> <span data-ttu-id="02df7-509">這也可以使用結構描述來列出，但不需要指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="02df7-509">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="02df7-510">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="02df7-510">Data Lake Store</span></span>

* <span data-ttu-id="02df7-511">更新基礎檔案系統 SDK 的版本，以提供更佳的支援來處理伺服器端節流情況。</span><span class="sxs-lookup"><span data-stu-id="02df7-511">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="02df7-512">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="02df7-512">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="02df7-513">遺失 access show 的說明。</span><span class="sxs-lookup"><span data-stu-id="02df7-513">missed help for access show.</span></span> <span data-ttu-id="02df7-514">將新增此說明。</span><span class="sxs-lookup"><span data-stu-id="02df7-514">adding it.</span></span> <span data-ttu-id="02df7-515">([#2743 (英文)](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="02df7-515">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="02df7-516">尋找</span><span class="sxs-lookup"><span data-stu-id="02df7-516">Find</span></span>

* <span data-ttu-id="02df7-517">改善搜尋結果，並允許進行搜尋索引版本控制</span><span class="sxs-lookup"><span data-stu-id="02df7-517">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="02df7-518">KeyVault</span><span class="sxs-lookup"><span data-stu-id="02df7-518">KeyVault</span></span>

* <span data-ttu-id="02df7-519">BC：`az keyvault certificate download`將 -e 從字串或二進位變更為 PEM 或 DER，來以更佳的方式代表選項</span><span class="sxs-lookup"><span data-stu-id="02df7-519">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="02df7-520">BC：從 `keyvault certificate create` 中移除 --expires 和 --not-before，因為服務不支援這些參數。</span><span class="sxs-lookup"><span data-stu-id="02df7-520">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="02df7-521">在 `keyvault certificate create` 中新增 --validity 參數，以選擇性地覆寫 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="02df7-521">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="02df7-522">修正 `keyvault certificate get-default-policy` 中公開 'expires' 和 'not_before' 但未公開 'validity_in_months' 的問題。</span><span class="sxs-lookup"><span data-stu-id="02df7-522">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="02df7-523">用於匯入 pem 和 pfx 的 keyvault 修正 ([#2754 (英文)](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="02df7-523">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="02df7-524">實驗室</span><span class="sxs-lookup"><span data-stu-id="02df7-524">Lab</span></span>

* <span data-ttu-id="02df7-525">新增適用於實驗室中環境的 create、show、delete 及 list 命令。</span><span class="sxs-lookup"><span data-stu-id="02df7-525">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="02df7-526">新增 show 和 list 命令以檢視實驗室中的 ARM 範本。</span><span class="sxs-lookup"><span data-stu-id="02df7-526">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="02df7-527">在 `az lab vm list` 中新增 --environment 旗標，以在實驗室中依環境篩選 VM。</span><span class="sxs-lookup"><span data-stu-id="02df7-527">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="02df7-528">新增便利命令 `az lab formula export-artifacts` 以匯出實驗室公式內的構件結構。</span><span class="sxs-lookup"><span data-stu-id="02df7-528">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="02df7-529">新增命令以管理實驗室內的密碼。</span><span class="sxs-lookup"><span data-stu-id="02df7-529">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="02df7-530">監視</span><span class="sxs-lookup"><span data-stu-id="02df7-530">Monitor</span></span>

* <span data-ttu-id="02df7-531">Bug 修正：建立 `az alert-rules create` 的 `--actions` 模型以取用 JSON 字串 ([#3009 (英文)](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="02df7-531">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="02df7-532">Bug 修正：diagnostic-settings create 不接受來自 show 命令的記錄/計量 ([#2913 (英文)](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="02df7-532">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="02df7-533">網路</span><span class="sxs-lookup"><span data-stu-id="02df7-533">Network</span></span>

* <span data-ttu-id="02df7-534">新增 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="02df7-534">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="02df7-535">新增對 `network watcher packet-capture create` 之 `--filters` 參數的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-535">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="02df7-536">新增對「應用程式閘道」連線清空的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-536">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="02df7-537">新增對「應用程式閘道」WAF 規則集組態的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-537">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="02df7-538">新增對 ExpressRoute 路由篩選和規則的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-538">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="02df7-539">新增對 TrafficManager 地理路由的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-539">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="02df7-540">新增對 VPN 連線原則型流量選取器的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-540">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="02df7-541">新增對 VPN 連線 IPSec 原則的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-541">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="02df7-542">修正 `vpn-connection create` 搭配使用 `--no-wait` 或 `--validate` 參數時的 Bug。</span><span class="sxs-lookup"><span data-stu-id="02df7-542">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="02df7-543">新增對「主動-主動」VNet 閘道的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-543">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="02df7-544">從 `network vpn-connection list/show` 命令移除 Null 值。</span><span class="sxs-lookup"><span data-stu-id="02df7-544">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="02df7-545">BC：修正 `vpn-connection create` 之輸出中的 Bug</span><span class="sxs-lookup"><span data-stu-id="02df7-545">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="02df7-546">修正未正確剖析 'vpn-connection create' 之 '--key-length' 引數的 Bug。</span><span class="sxs-lookup"><span data-stu-id="02df7-546">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="02df7-547">修正 `dns zone import` 中未正確匯入記錄的 Bug。</span><span class="sxs-lookup"><span data-stu-id="02df7-547">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="02df7-548">修正 `traffic-manager endpoint update` 無法運作的 Bug。</span><span class="sxs-lookup"><span data-stu-id="02df7-548">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="02df7-549">新增 'network watcher' 預覽命令。</span><span class="sxs-lookup"><span data-stu-id="02df7-549">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="02df7-550">設定檔</span><span class="sxs-lookup"><span data-stu-id="02df7-550">Profile</span></span>

* <span data-ttu-id="02df7-551">支援在找不到訂用帳戶時進行登入 ([#2560 (英文)](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="02df7-551">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="02df7-552">在 az account set --subscription 中支援短參數名稱 ([#2980 (英文)](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="02df7-552">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="02df7-553">Redis</span><span class="sxs-lookup"><span data-stu-id="02df7-553">Redis</span></span>

* <span data-ttu-id="02df7-554">新增 update 命令，這也會為 redis 快取新增調整能力</span><span class="sxs-lookup"><span data-stu-id="02df7-554">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="02df7-555">取代 'update-settings' 命令。</span><span class="sxs-lookup"><span data-stu-id="02df7-555">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="02df7-556">資源</span><span class="sxs-lookup"><span data-stu-id="02df7-556">Resource</span></span>

* <span data-ttu-id="02df7-557">新增 managedapp 和 managedapp definition 命令 ([#2985 (英文)](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="02df7-557">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="02df7-558">支援 'provider operation' 命令 ([#2908 (英文)](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="02df7-558">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="02df7-559">支援一般 resource create ([#2606 (英文)](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="02df7-559">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="02df7-560">修正資源剖析和 api 版本查詢。</span><span class="sxs-lookup"><span data-stu-id="02df7-560">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="02df7-561">([#2781 (英文)](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="02df7-561">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="02df7-562">新增 az lock update 的文件。</span><span class="sxs-lookup"><span data-stu-id="02df7-562">Add docs for az lock update.</span></span> <span data-ttu-id="02df7-563">([#2702 (英文)](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="02df7-563">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="02df7-564">如果您嘗試列出不存在之群組的資源，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="02df7-564">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="02df7-565">([#2769 (英文)](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="02df7-565">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="02df7-566">[計算] 修正 VMSS 和 VM 可用性設定組更新的相關問題。</span><span class="sxs-lookup"><span data-stu-id="02df7-566">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="02df7-567">([#2773 (英文)](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="02df7-567">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="02df7-568">修正 parent-resource-path 為 None 時的 lock create 和 delete ([#2742 (英文)](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="02df7-568">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="02df7-569">角色</span><span class="sxs-lookup"><span data-stu-id="02df7-569">Role</span></span>

* <span data-ttu-id="02df7-570">create-for-rbac：確保 SP 的結束日期不會超過憑證的到期日 ([#2989 (英文)](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="02df7-570">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="02df7-571">RBAC：新增對 'ad group' 的完整支援 ([#2016 (英文)](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="02df7-571">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="02df7-572">角色：修正 role definition update 上的問題 ([#2745 (英文)](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="02df7-572">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="02df7-573">create-for-rbac：確保系統會挑選使用者提供的密碼</span><span class="sxs-lookup"><span data-stu-id="02df7-573">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="02df7-574">SQL</span><span class="sxs-lookup"><span data-stu-id="02df7-574">SQL</span></span>

* <span data-ttu-id="02df7-575">新增 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="02df7-575">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="02df7-576">SQL - 能夠直接連接到資源提供者 ([#2832 (英文)](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="02df7-576">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="02df7-577">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-577">Storage</span></span>

* <span data-ttu-id="02df7-578">`storage account create` 之資源群組位置的預設位置。</span><span class="sxs-lookup"><span data-stu-id="02df7-578">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="02df7-579">新增對遞增 blob 複製的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-579">Add support for incremental blob copy</span></span>
* <span data-ttu-id="02df7-580">新增對大型區塊 blob 上傳的支援</span><span class="sxs-lookup"><span data-stu-id="02df7-580">Add support for large block blob upload</span></span>
* <span data-ttu-id="02df7-581">當要上傳的檔案大於 200 GB 時，將區塊大小變更為 100 MB</span><span class="sxs-lookup"><span data-stu-id="02df7-581">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-582">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-582">VM</span></span>

* <span data-ttu-id="02df7-583">avail-set：將 UD&FD 網域計數設定為選用</span><span class="sxs-lookup"><span data-stu-id="02df7-583">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="02df7-584">注意：主權雲端中的 VM 命令。請避免使用受管理磁碟相關的功能，包括下列功能：</span><span class="sxs-lookup"><span data-stu-id="02df7-584">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="02df7-585">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="02df7-585">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="02df7-586">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="02df7-586">az vm/vmss disk</span></span>
  3. <span data-ttu-id="02df7-587">在 "az vm/vmss create" 內，請使用 "—use-unmanaged-disk" 來避免使用受管理的磁碟。其他命令應該可運作</span><span class="sxs-lookup"><span data-stu-id="02df7-587">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="02df7-588">vm/vmss：改進產生 SSH 金鑰組時的警告文字</span><span class="sxs-lookup"><span data-stu-id="02df7-588">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="02df7-589">vm/vmss：支援從需要方案資訊的市場映像進行建立 ([#1209 (英文)](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="02df7-589">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="02df7-590">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="02df7-590">April 3, 2017</span></span>

<span data-ttu-id="02df7-591">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="02df7-591">Version 2.0.2</span></span>

<span data-ttu-id="02df7-592">在這一版中，我們發行了 ACR、Batch、KeyVault 和 SQL 元件。</span><span class="sxs-lookup"><span data-stu-id="02df7-592">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="02df7-593">核心</span><span class="sxs-lookup"><span data-stu-id="02df7-593">Core</span></span>

* <span data-ttu-id="02df7-594">將 ACR、實驗室、監視及尋找模組新增至預設清單。</span><span class="sxs-lookup"><span data-stu-id="02df7-594">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="02df7-595">Login︰略過錯誤的租用戶 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="02df7-595">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="02df7-596">Login︰將預設訂用帳戶設定為具有「已啟用」狀態的訂用帳戶 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="02df7-596">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="02df7-597">將 wait 命令和 --no-wait 支援新增至多個命令 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="02df7-597">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="02df7-598">Core︰支援使用憑證的服務主體登入 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="02df7-598">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="02df7-599">新增遺漏範本參數的提示。</span><span class="sxs-lookup"><span data-stu-id="02df7-599">Add prompting for missing template parameters.</span></span> <span data-ttu-id="02df7-600">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="02df7-600">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="02df7-601">支援設定諸如預設資源群組、預設 web、預設 VM 等常見引數的預設值</span><span class="sxs-lookup"><span data-stu-id="02df7-601">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="02df7-602">支援登入特定的租用戶</span><span class="sxs-lookup"><span data-stu-id="02df7-602">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="02df7-603">ACS</span><span class="sxs-lookup"><span data-stu-id="02df7-603">ACS</span></span>

* <span data-ttu-id="02df7-604">[ACS] 新增設定預設 ACS 叢集的支援 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="02df7-604">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="02df7-605">新增 SSH 金鑰密碼提示的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-605">Add support for ssh key password prompting.</span></span> <span data-ttu-id="02df7-606">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="02df7-606">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="02df7-607">新增 Windows 叢集的支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-607">Add support for windows clusters.</span></span> <span data-ttu-id="02df7-608">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="02df7-608">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="02df7-609">將角色從擁有者切換為參與者。</span><span class="sxs-lookup"><span data-stu-id="02df7-609">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="02df7-610">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="02df7-610">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="02df7-611">AppService</span><span class="sxs-lookup"><span data-stu-id="02df7-611">AppService</span></span>

* <span data-ttu-id="02df7-612">appservice︰取得用於 DNS A 記錄之外部 IP 位址的支援 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="02df7-612">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="02df7-613">appservice︰支援繫結萬用字元憑證 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="02df7-613">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="02df7-614">appservice︰支援列出發行設定檔 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="02df7-614">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="02df7-615">AppService - 設定之後觸發原始檔控制同步處理 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="02df7-615">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="02df7-616">DataLake</span><span class="sxs-lookup"><span data-stu-id="02df7-616">DataLake</span></span>

* <span data-ttu-id="02df7-617">Data Lake Analytics 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="02df7-617">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="02df7-618">Data Lake Store 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="02df7-618">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="02df7-619">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="02df7-619">DocuemntDB</span></span>

* <span data-ttu-id="02df7-620">DocumentDB︰新增列出連接字串的支援 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="02df7-620">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="02df7-621">VM</span><span class="sxs-lookup"><span data-stu-id="02df7-621">VM</span></span>

* <span data-ttu-id="02df7-622">[Compute] 將 AppGateway 支援新增至虛擬機器擴展集建立 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="02df7-622">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="02df7-623">[VM/VMSS] 改良的磁碟快取支援 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="02df7-623">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="02df7-624">VM/VMSS︰併入入口網站所使用的認證驗證邏輯 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="02df7-624">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="02df7-625">新增 wait 命令和 --no-wait 支援 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="02df7-625">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="02df7-626">虛擬機器擴展集︰支援 * 列出跨 VM 的執行個體檢視 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="02df7-626">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="02df7-627">新增 VM 和虛擬機器擴展集的 --祕密 ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="02df7-627">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="02df7-628">可使用特殊的 VHD 來建立 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="02df7-628">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="02df7-629">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="02df7-629">February 27, 2017</span></span>

<span data-ttu-id="02df7-630">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="02df7-630">Version 2.0.0</span></span>

<span data-ttu-id="02df7-631">此版本的 Azure CLI 2.0 是第一個「正式運作」版本。</span><span class="sxs-lookup"><span data-stu-id="02df7-631">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="02df7-632">正式運作適用於下列的命令模組︰</span><span class="sxs-lookup"><span data-stu-id="02df7-632">General availability applies to these command modules:</span></span>
- <span data-ttu-id="02df7-633">Container Service (ACS)</span><span class="sxs-lookup"><span data-stu-id="02df7-633">Container Service (acs)</span></span>
- <span data-ttu-id="02df7-634">計算 (包含 Resource Manager、VM、虛擬機器擴展集、受控磁碟)</span><span class="sxs-lookup"><span data-stu-id="02df7-634">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="02df7-635">網路功能</span><span class="sxs-lookup"><span data-stu-id="02df7-635">Networking</span></span>
- <span data-ttu-id="02df7-636">儲存體</span><span class="sxs-lookup"><span data-stu-id="02df7-636">Storage</span></span>

<span data-ttu-id="02df7-637">這些命令模組可用在生產環境中，且受標準 Microsoft SLA 支援。</span><span class="sxs-lookup"><span data-stu-id="02df7-637">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="02df7-638">您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)開啟問題。</span><span class="sxs-lookup"><span data-stu-id="02df7-638">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="02df7-639">您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。您可以從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="02df7-639">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="02df7-640">這些模組中的命令很穩定，且不應該變更此版 Azure CLI 之未來版本的語法。</span><span class="sxs-lookup"><span data-stu-id="02df7-640">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="02df7-641">若要確認的 CLI 的版本，請使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="02df7-641">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="02df7-642">輸出會列出 CLI 本身的版本 (此版本中為 2.0.0)、個別的命令模組，以及您所使用的 Python 和 GCC 版本。</span><span class="sxs-lookup"><span data-stu-id="02df7-642">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="02df7-643">些命令模組會有 "b*n*" 或 "rc*n*" 後置詞。</span><span class="sxs-lookup"><span data-stu-id="02df7-643">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="02df7-644">這些命令模組仍處於預覽狀態，且未來會正式運作。</span><span class="sxs-lookup"><span data-stu-id="02df7-644">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="02df7-645">我們也有 CLI 的夜間預覽組建。</span><span class="sxs-lookup"><span data-stu-id="02df7-645">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="02df7-646">如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。</span><span class="sxs-lookup"><span data-stu-id="02df7-646">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="02df7-647">您可以透過下列方式來報告夜間預覽組建的問題︰</span><span class="sxs-lookup"><span data-stu-id="02df7-647">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="02df7-648">在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)中報告問題</span><span class="sxs-lookup"><span data-stu-id="02df7-648">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="02df7-649">連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="02df7-649">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="02df7-650">從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="02df7-650">Provide feedback from the command line with the `az feedback` command.</span></span>

