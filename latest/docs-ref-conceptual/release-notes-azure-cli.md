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
ms.openlocfilehash: 429b099dabd27d9356e88791f955ec52acd2a5f9
ms.sourcegitcommit: 9b36c15dc0e10024e23b8018604f5ef63c025de1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="c9aa2-104">Azure CLI 2.0 版本資訊</span><span class="sxs-lookup"><span data-stu-id="c9aa2-104">Azure CLI 2.0 release notes</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="c9aa2-105">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-105">October 24, 2017</span></span>

<span data-ttu-id="c9aa2-106">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="c9aa2-106">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="c9aa2-107">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-107">Core</span></span>

* <span data-ttu-id="c9aa2-108">將 `2017-03-09-profile` 更新為取用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-108">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="c9aa2-109">ACR</span><span class="sxs-lookup"><span data-stu-id="c9aa2-109">ACR</span></span>

* <span data-ttu-id="c9aa2-110">已將資源管理更新為指向`2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-110">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="c9aa2-111">已將「自備儲存體」SKU 變更為「傳統」</span><span class="sxs-lookup"><span data-stu-id="c9aa2-111">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="c9aa2-112">已將「登錄 SKU」重新命名為「基本」、「標準」和「進階」</span><span class="sxs-lookup"><span data-stu-id="c9aa2-112">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-113">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-113">ACS</span></span>

* <span data-ttu-id="c9aa2-114">[預覽] 已新增 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-114">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="c9aa2-115">已修正 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-115">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-116">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-116">Appservice</span></span>

* <span data-ttu-id="c9aa2-117">已修正下載的 `webapp` 記錄可能無效的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-117">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="c9aa2-118">元件</span><span class="sxs-lookup"><span data-stu-id="c9aa2-118">Component</span></span>

* <span data-ttu-id="c9aa2-119">已為所有的安裝程式和確認提示新增更清楚的取代訊息</span><span class="sxs-lookup"><span data-stu-id="c9aa2-119">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="c9aa2-120">監視</span><span class="sxs-lookup"><span data-stu-id="c9aa2-120">Monitor</span></span>

* <span data-ttu-id="c9aa2-121">已新增 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-121">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-122">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-122">Resource</span></span>

* <span data-ttu-id="c9aa2-123">已修正與 `group export` 中最新版本 msrest 相依性不相容的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-123">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="c9aa2-124">已修正 `policy assignment create` 以與內建的原則定義和原則集合定義搭配使用</span><span class="sxs-lookup"><span data-stu-id="c9aa2-124">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-125">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-125">VM</span></span>

* <span data-ttu-id="c9aa2-126">已將引數 `--accelerated-networking` 新增至 `vmss create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-126">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="c9aa2-127">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-127">October 9, 2017</span></span>

<span data-ttu-id="c9aa2-128">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="c9aa2-128">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="c9aa2-129">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-129">Core</span></span>

* <span data-ttu-id="c9aa2-130">新增在 Azure Stack 中在結尾處使用斜線處理 ADFS 授權 URL 的方式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-130">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-131">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-131">Appservice</span></span>

* <span data-ttu-id="c9aa2-132">新增新命令`webapp update` 的一般更新</span><span class="sxs-lookup"><span data-stu-id="c9aa2-132">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="c9aa2-133">批次</span><span class="sxs-lookup"><span data-stu-id="c9aa2-133">Batch</span></span>

* <span data-ttu-id="c9aa2-134">更新為 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="c9aa2-134">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="c9aa2-135">更新 VirtualMachineConfiguration 的 `--image` 選項以支援 publish:offer:sku:version 以外的 ARM 映像參考</span><span class="sxs-lookup"><span data-stu-id="c9aa2-135">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="c9aa2-136">新增 Batch 延伸模組命令的新 CLI 延伸模型支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-136">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="c9aa2-137">移除元件模型中的 Batch 支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-137">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="c9aa2-138">Batchai</span><span class="sxs-lookup"><span data-stu-id="c9aa2-138">Batchai</span></span>

* <span data-ttu-id="c9aa2-139">Batch AI 模組的初始版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-139">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="c9aa2-140">Keyvault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-140">Keyvault</span></span>

* <span data-ttu-id="c9aa2-141">修正在 Azure Stack 上使用 ADFS 時，Key Vault 驗證的問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-141">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="c9aa2-142">(#4448)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-142">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="c9aa2-143">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-143">Network</span></span>

* <span data-ttu-id="c9aa2-144">將 `application-gateway address-pool create` 的 `--server` 引數變更為可選用，以允許空白的位址集區</span><span class="sxs-lookup"><span data-stu-id="c9aa2-144">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="c9aa2-145">更新 `traffic-manager` 以支援最新功能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-145">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-146">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-146">Resource</span></span>

* <span data-ttu-id="c9aa2-147">新增 `--resource-group/-g` 選項的支援，將資源群組名稱變更為 `group`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-147">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="c9aa2-148">新增 `account lock` 命令以搭配訂用帳戶層級鎖定使用</span><span class="sxs-lookup"><span data-stu-id="c9aa2-148">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="c9aa2-149">新增 `group lock` 命令以搭配群組層級鎖定使用</span><span class="sxs-lookup"><span data-stu-id="c9aa2-149">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="c9aa2-150">新增 `resource lock` 命令以搭配資源層級鎖定使用</span><span class="sxs-lookup"><span data-stu-id="c9aa2-150">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="c9aa2-151">Sql</span><span class="sxs-lookup"><span data-stu-id="c9aa2-151">Sql</span></span>

* <span data-ttu-id="c9aa2-152">新增使用「攜帶您自己的金鑰」進行 SQL 透明資料加密 (TDE) 和 TDE 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-152">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="c9aa2-153">新增 `db list-deleted` 命令和 `db restore --deleted-time` 參數，以便尋找和還原已刪除的資料庫</span><span class="sxs-lookup"><span data-stu-id="c9aa2-153">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="c9aa2-154">新增 `db op list` 和 `db op cancel`，提供在資料庫上列出清單和取消處理中作業的功能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-154">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-155">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-155">Storage</span></span>

* <span data-ttu-id="c9aa2-156">新增檔案共用快照集的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-156">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-157">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-157">Vm</span></span>

* <span data-ttu-id="c9aa2-158">修正 `vm show` 中使用 `-d` 導致遺漏私人 IP 位址所造成的損毀</span><span class="sxs-lookup"><span data-stu-id="c9aa2-158">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="c9aa2-159">[預覽] 新增輪流升級至`vmss create` 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-159">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="c9aa2-160">新增使用 `vm encryption enable` 更新加密設定的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-160">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="c9aa2-161">在 `vm create` 中新增 `--os-disk-size-gb` 參數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-161">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="c9aa2-162">在 `vmss create` 中新增適用於 Windows 的 `--license-type` 參數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-162">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="c9aa2-163">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-163">September 22, 2017</span></span>

<span data-ttu-id="c9aa2-164">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="c9aa2-164">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-165">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-165">Resource</span></span>

* <span data-ttu-id="c9aa2-166">已新增顯示內建原則定義的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-166">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="c9aa2-167">已新增建立原則定義的支援模式參數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-167">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="c9aa2-168">已新增對於 `managedapp definition create` UI 定義及範本的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-168">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="c9aa2-169">[重大變更] 已變更 `managedapp` 資源類型，從 `appliances` 變為 `applications`，且從 `applianceDefinitions` 變為 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-169">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-170">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-170">Network</span></span>

* <span data-ttu-id="c9aa2-171">已新增可用性區域，以支援 `network lb` 和 `network public-ip` 子命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-171">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="c9aa2-172">已新增對 `express-route` 的 IPv6 Microsoft 對等互連支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-172">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="c9aa2-173">已新增 `asg` 應用程式安全性群組命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-173">Added `asg` application security group commands</span></span>
* <span data-ttu-id="c9aa2-174">將 `--application-security-groups` 引數新增至 `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-174">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="c9aa2-175">已將 `--source-asgs` 和 `--destination-asgs` 引數新增至 `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-175">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="c9aa2-176">已將 `--ddos-protection` 和 `--vm-protection` 引數新增至 `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-176">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="c9aa2-177">已新增 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-177">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-178">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-178">Storage</span></span>

* <span data-ttu-id="c9aa2-179">已修正更新 SDK 後 `storage account network-rule` 命令可能會失敗的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-179">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="c9aa2-180">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="c9aa2-180">Eventgrid</span></span>

* <span data-ttu-id="c9aa2-181">已更新 Azure Event Grid Python SDK 以使用較新的 API 版本 "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="c9aa2-181">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="c9aa2-182">SQL</span><span class="sxs-lookup"><span data-stu-id="c9aa2-182">SQL</span></span>

* <span data-ttu-id="c9aa2-183">已將 `sql server list` 引數 `--resource-group` 變更為可選。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-183">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="c9aa2-184">如果未指定，會傳回訂用帳戶中所有的 sql 伺服器</span><span class="sxs-lookup"><span data-stu-id="c9aa2-184">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="c9aa2-185">已將 `--no-wait` 參數新增至 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-185">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="c9aa2-186">Keyvault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-186">Keyvault</span></span>

* <span data-ttu-id="c9aa2-187">已新增從 proxy 後方支援 Keyvault 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-187">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-188">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-188">VM</span></span>

* <span data-ttu-id="c9aa2-189">已新增 `[vm|vmss|disk] create` 的可用性區域支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-189">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="c9aa2-190">已修正使用 `--app-gateway ID` 與 `vmss create` 會導致失敗的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-190">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="c9aa2-191">已將引數 `--asgs` 新增至 `vm create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-191">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="c9aa2-192">已新增使用 `vm run-command` 在 VM 上執行命令的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-192">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="c9aa2-193">[預覽] 已新增使用 `vmss encryption` 加密 VMSS 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-193">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="c9aa2-194">已新增使用 `vm perform-maintenance` 在 VM 上執行維護工作的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-194">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-195">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-195">ACS</span></span>

* <span data-ttu-id="c9aa2-196">[預覽] 已針對 ACS 預覽區域，將 `--orchestrator-release` 引數新增至 `acs create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-196">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-197">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-197">Appservice</span></span>

* <span data-ttu-id="c9aa2-198">已新增使用 `webapp auth [update|show]` 更新並顯示驗證設定的功能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-198">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="c9aa2-199">備份</span><span class="sxs-lookup"><span data-stu-id="c9aa2-199">Backup</span></span>

* <span data-ttu-id="c9aa2-200">預覽版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-200">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="c9aa2-201">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-201">September 11, 2017</span></span>

<span data-ttu-id="c9aa2-202">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="c9aa2-202">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="c9aa2-203">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-203">Core</span></span>

* <span data-ttu-id="c9aa2-204">啟用命令模組以在遙測中設定自己的相互關聯識別碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-204">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="c9aa2-205">修正當遙測設為診斷模式時的 JSON 傾印問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-205">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-206">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-206">Acs</span></span>

* <span data-ttu-id="c9aa2-207">已新增 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-207">Added `acs list-locations` command</span></span>
* <span data-ttu-id="c9aa2-208">讓 `ssh-key-file` 隨附預期的預設值</span><span class="sxs-lookup"><span data-stu-id="c9aa2-208">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-209">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-209">Appservice</span></span>

* <span data-ttu-id="c9aa2-210">新增在資源群組中建立 Web 應用程式，而非在作用中服務計劃中建立 Web 應用程式的功能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-210">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="c9aa2-211">CDN</span><span class="sxs-lookup"><span data-stu-id="c9aa2-211">CDN</span></span>

* <span data-ttu-id="c9aa2-212">修正 `cdn custom-domain create` 的「CustomDomain 無法互動」錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-212">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="c9aa2-213">分機</span><span class="sxs-lookup"><span data-stu-id="c9aa2-213">Extension</span></span>

* <span data-ttu-id="c9aa2-214">初始版本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-214">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="c9aa2-215">Keyvault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-215">Keyvault</span></span>

* <span data-ttu-id="c9aa2-216">修正對 `keyvault set-policy` 的權限區分大小寫的問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-216">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-217">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-217">Network</span></span>

* <span data-ttu-id="c9aa2-218">已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-218">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c9aa2-219">己針對 `vnet subnet create/update` 將 `--private-access-services` 引數重新命名為 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-219">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="c9aa2-220">已將多個 IP 和連接埠範圍的支援新增至 `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-220">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="c9aa2-221">已將 SKU 的支援新增至 `lb create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-221">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c9aa2-222">已將 SKU 的支援新增至 `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-222">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-223">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-223">Resource</span></span>

* <span data-ttu-id="c9aa2-224">允許在 `policy definition create` 及 `policy definition update` 中傳送資源原則參數定義</span><span class="sxs-lookup"><span data-stu-id="c9aa2-224">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="c9aa2-225">允許為 `policy assignment create` 傳送參數值</span><span class="sxs-lookup"><span data-stu-id="c9aa2-225">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="c9aa2-226">允許為所有參數傳送 JSON 或檔案</span><span class="sxs-lookup"><span data-stu-id="c9aa2-226">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="c9aa2-227">遞增的 API 版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-227">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="c9aa2-228">SQL</span><span class="sxs-lookup"><span data-stu-id="c9aa2-228">SQL</span></span>

* <span data-ttu-id="c9aa2-229">已新增 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-229">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-230">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-230">VM</span></span>

* <span data-ttu-id="c9aa2-231">已修正：在提供 `--scope` 之前不指派存取權</span><span class="sxs-lookup"><span data-stu-id="c9aa2-231">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="c9aa2-232">已修正：使用相同延伸模組命名作為入口網站</span><span class="sxs-lookup"><span data-stu-id="c9aa2-232">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="c9aa2-233">已從 `[vm|vmss] create` 輸出移除 `subscription`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-233">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="c9aa2-234">已修正：`[vm|vmss] create` 儲存體 SKU 不會套用至搭配映像的資料磁碟</span><span class="sxs-lookup"><span data-stu-id="c9aa2-234">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="c9aa2-235">已修正：`vm format-secret --secrets` 不會接受新行分隔識別碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-235">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="c9aa2-236">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-236">August 31, 2017</span></span>

<span data-ttu-id="c9aa2-237">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="c9aa2-237">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="c9aa2-238">Keyvault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-238">Keyvault</span></span>

* <span data-ttu-id="c9aa2-239">修正試著自動使用 `secret download` 解析祕密編碼時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-239">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="c9aa2-240">Sf</span><span class="sxs-lookup"><span data-stu-id="c9aa2-240">Sf</span></span>

* <span data-ttu-id="c9aa2-241">取代所有命令，以利於 Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-241">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-242">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-242">Storage</span></span>

* <span data-ttu-id="c9aa2-243">修正無法在不支援 NetworkACL 功能的區域中建立儲存體帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-243">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="c9aa2-244">若指定內容類型和內容編碼，則判斷 Blob 及檔案上傳期間的內容類型及內容編碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-244">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="c9aa2-245">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-245">August 28, 2017</span></span>

<span data-ttu-id="c9aa2-246">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="c9aa2-246">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="c9aa2-247">CLI</span><span class="sxs-lookup"><span data-stu-id="c9aa2-247">CLI</span></span>

* <span data-ttu-id="c9aa2-248">已將法律注意事項新增至 `--version`。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-248">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-249">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-249">ACS</span></span>

* <span data-ttu-id="c9aa2-250">已更正預覽區域。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-250">Corrected preview regions.</span></span>
* <span data-ttu-id="c9aa2-251">已正確格式化預設 `dns_name_prefix`。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-251">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="c9aa2-252">最佳化的 acs 命令輸出。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-252">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-253">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-253">Appservice</span></span>

* <span data-ttu-id="c9aa2-254">[新變更] 已修正 `az webapp config appsettings [delete|set]` 輸出中的不一致</span><span class="sxs-lookup"><span data-stu-id="c9aa2-254">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="c9aa2-255">已針對 `az webapp config container set --docker-custom-image-name` 新增 `-i` 的新別名</span><span class="sxs-lookup"><span data-stu-id="c9aa2-255">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="c9aa2-256">已公開 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-256">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="c9aa2-257">已公開 `az webapp delete` 中的新引數，可保留應用程式服務計劃、計量或 DNS 註冊</span><span class="sxs-lookup"><span data-stu-id="c9aa2-257">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="c9aa2-258">已修正：正確偵測到位置設定</span><span class="sxs-lookup"><span data-stu-id="c9aa2-258">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="c9aa2-259">IoT</span><span class="sxs-lookup"><span data-stu-id="c9aa2-259">IoT</span></span>

* <span data-ttu-id="c9aa2-260">已修正 #3934：建立原則時無法再清除現有的原則</span><span class="sxs-lookup"><span data-stu-id="c9aa2-260">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-261">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-261">Network</span></span>

* <span data-ttu-id="c9aa2-262">[新變更] 已將 `vnet list-private-access-services` 重新命名為 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-262">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c9aa2-263">[新變更] 已將 `--private-access-services` 選項重新命名為適用於 `vnet subnet [create|update]` 的 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-263">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="c9aa2-264">已將多個 IP 和連接埠範圍的支援新增至 `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-264">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="c9aa2-265">已將 SKU 的支援新增至 `lb create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-265">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c9aa2-266">已將 SKU 的支援新增至 `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-266">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="c9aa2-267">設定檔</span><span class="sxs-lookup"><span data-stu-id="c9aa2-267">Profile</span></span>

* <span data-ttu-id="c9aa2-268">已公開 `--msi` 和 `--msi-port`，可使用虛擬機器的身分識別登入</span><span class="sxs-lookup"><span data-stu-id="c9aa2-268">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c9aa2-269">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c9aa2-269">Service Fabric</span></span>

* <span data-ttu-id="c9aa2-270">預覽版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-270">Preview release</span></span>
* <span data-ttu-id="c9aa2-271">簡化的登錄使用者/命令的密碼規則</span><span class="sxs-lookup"><span data-stu-id="c9aa2-271">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="c9aa2-272">已修正使用者即使在參數中傳遞之後的密碼提示</span><span class="sxs-lookup"><span data-stu-id="c9aa2-272">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="c9aa2-273">已新增空白 `registry_cred` 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-273">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-274">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-274">Storage</span></span>

* <span data-ttu-id="c9aa2-275">已啟用設定 blob 層</span><span class="sxs-lookup"><span data-stu-id="c9aa2-275">Enabled setting blob tier</span></span>
* <span data-ttu-id="c9aa2-276">已將 `--bypass` 和 `--default-action` 引數新增至 `storage account [create|update]` 以支援服務通道</span><span class="sxs-lookup"><span data-stu-id="c9aa2-276">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="c9aa2-277">新增的命令可將 VNET 規則和以 IP 作為基礎的規則新增至 `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-277">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="c9aa2-278">透過客戶管理的金鑰啟用服務加密</span><span class="sxs-lookup"><span data-stu-id="c9aa2-278">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="c9aa2-279">[新變更] 已將 `--encryption` 選項重新命名為適用於 `az storage account create and az storage account update` 命令的 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-279">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="c9aa2-280">已修正 #4220：`az storage account update encryption` - 語法不相符</span><span class="sxs-lookup"><span data-stu-id="c9aa2-280">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-281">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-281">VM</span></span>

* <span data-ttu-id="c9aa2-282">已修正使用 `--instance-id *` 時會顯示 `vmss get-instance-view` 的額外錯誤資訊的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-282">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="c9aa2-283">已將 `--lb-sku` 的支援新增至 `vmss create`：</span><span class="sxs-lookup"><span data-stu-id="c9aa2-283">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="c9aa2-284">從 `[vm|vmss] create` 的系統管理員名稱封鎖清單移除人力名稱</span><span class="sxs-lookup"><span data-stu-id="c9aa2-284">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="c9aa2-285">已修正在無法從映像擷取計劃資訊時，`[vm|vmss] create` 會擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-285">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="c9aa2-286">已修正使用內部 LB 建立 vmms scaleset 時的損毀</span><span class="sxs-lookup"><span data-stu-id="c9aa2-286">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="c9aa2-287">已修正 `--no-wait` 引數無法與 `vm availability-set create` 搭配使用的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-287">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="c9aa2-288">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-288">August 15, 2017</span></span>

<span data-ttu-id="c9aa2-289">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="c9aa2-289">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-290">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-290">ACS</span></span>

* <span data-ttu-id="c9aa2-291">已更正 kubernetes 的 sshMaster0 連接埠號碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-291">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-292">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-292">Appservice</span></span>

* <span data-ttu-id="c9aa2-293">已修正建立以新 git 作為基礎的 Linux WebApp 時的例外狀況</span><span class="sxs-lookup"><span data-stu-id="c9aa2-293">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="c9aa2-294">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c9aa2-294">Event Grid</span></span>

* <span data-ttu-id="c9aa2-295">已新增 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="c9aa2-295">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="c9aa2-296">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-296">August 11, 2017</span></span>

<span data-ttu-id="c9aa2-297">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="c9aa2-297">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-298">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-298">ACS</span></span>

* <span data-ttu-id="c9aa2-299">新增更多預覽區域</span><span class="sxs-lookup"><span data-stu-id="c9aa2-299">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="c9aa2-300">批次</span><span class="sxs-lookup"><span data-stu-id="c9aa2-300">Batch</span></span>

* <span data-ttu-id="c9aa2-301">更新為 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c9aa2-301">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="c9aa2-302">已新增新的命令顯示作業的工作計數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-302">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="c9aa2-303">已修正資源檔案 SAS URL 處理中的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-303">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="c9aa2-304">Batch 帳戶端點現在支援選擇性的 'https://' 前置詞</span><span class="sxs-lookup"><span data-stu-id="c9aa2-304">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="c9aa2-305">支援將超過 100 個工作的清單新增至作業</span><span class="sxs-lookup"><span data-stu-id="c9aa2-305">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="c9aa2-306">已新增載入擴充功能命令模組的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="c9aa2-306">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="c9aa2-307">元件</span><span class="sxs-lookup"><span data-stu-id="c9aa2-307">Component</span></span>

* <span data-ttu-id="c9aa2-308">已新增對 'az component' 命令的取代警告</span><span class="sxs-lookup"><span data-stu-id="c9aa2-308">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="c9aa2-309">容器</span><span class="sxs-lookup"><span data-stu-id="c9aa2-309">Container</span></span>

* <span data-ttu-id="c9aa2-310">`create`：已修正環境變數內不允許等號的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-310">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="c9aa2-311">資料湖存放區</span><span class="sxs-lookup"><span data-stu-id="c9aa2-311">Data Lake Store</span></span>

* <span data-ttu-id="c9aa2-312">已啟用進度控制項</span><span class="sxs-lookup"><span data-stu-id="c9aa2-312">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="c9aa2-313">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c9aa2-313">Event Grid</span></span>

* <span data-ttu-id="c9aa2-314">初始版本</span><span class="sxs-lookup"><span data-stu-id="c9aa2-314">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-315">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-315">Network</span></span>

* <span data-ttu-id="c9aa2-316">`lb`：已修正省略某些子資源名稱時未正確解析的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-316">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="c9aa2-317">`application-gateway {subresource} delete`：已修正無法接受 `--no-wait` 的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-317">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="c9aa2-318">`application-gateway http-settings update`：已修正無法關閉 `--connection-draining-timeout` 的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-318">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="c9aa2-319">已修正非預期關鍵字引數 `sa_data_size_kilobyes` 與 `az network vpn-connection ipsec-policy add` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-319">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="c9aa2-320">設定檔</span><span class="sxs-lookup"><span data-stu-id="c9aa2-320">Profile</span></span>

* <span data-ttu-id="c9aa2-321">`account list`：已新增 `--refresh`，可從伺服器同步處理最新的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="c9aa2-321">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-322">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-322">Storage</span></span>

* <span data-ttu-id="c9aa2-323">使用指派身分識別的系統來啟用更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="c9aa2-323">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-324">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-324">VM</span></span>

* <span data-ttu-id="c9aa2-325">`availability-set`：已在轉換上公開容錯網域計數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-325">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="c9aa2-326">已公開 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-326">Exposed `list-skus` command</span></span>
* <span data-ttu-id="c9aa2-327">支援無需建立角色指派即可指定身分識別</span><span class="sxs-lookup"><span data-stu-id="c9aa2-327">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="c9aa2-328">在連結資料磁碟上套用儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="c9aa2-328">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="c9aa2-329">已移除使用受控磁碟時的預設作業系統磁碟名稱和儲存體 SKU</span><span class="sxs-lookup"><span data-stu-id="c9aa2-329">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="c9aa2-330">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-330">July 28, 2017</span></span>

<span data-ttu-id="c9aa2-331">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="c9aa2-331">Version 2.0.12</span></span>

* <span data-ttu-id="c9aa2-332">已新增容器命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-332">Added container commands</span></span>
* <span data-ttu-id="c9aa2-333">已新增計費和耗用模組</span><span class="sxs-lookup"><span data-stu-id="c9aa2-333">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="c9aa2-334">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-334">Core</span></span>

* <span data-ttu-id="c9aa2-335">包含憑證之服務主體的輸出 SDK 驗證資訊</span><span class="sxs-lookup"><span data-stu-id="c9aa2-335">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="c9aa2-336">已修正部署進度例外狀況</span><span class="sxs-lookup"><span data-stu-id="c9aa2-336">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="c9aa2-337">從目前的雲端使用 arm 端點來建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="c9aa2-337">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="c9aa2-338">clouds.config 檔案的改良並行處理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-338">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="c9aa2-339">重新整理每個命令執行的用戶端要求識別碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-339">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="c9aa2-340">使用正確的 SDK 設定檔建立訂用帳戶用戶端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-340">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="c9aa2-341">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-341">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c9aa2-342">已新增透過 jmespath 查詢挑選資料表輸出欄位的支援 (#3581)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-342">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="c9aa2-343">已改善剖析引數的靜音和使用手勢的附加記錄 (#3434)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-343">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="c9aa2-344">使用正確的 SDK 設定檔建立訂用帳戶用戶端</span><span class="sxs-lookup"><span data-stu-id="c9aa2-344">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="c9aa2-345">將所有現有的記錄檔移到最新的資料夾</span><span class="sxs-lookup"><span data-stu-id="c9aa2-345">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="c9aa2-346">已修正 VM/VMSS 建立的等冪 (#3586)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-346">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="c9aa2-347">命令路徑不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="c9aa2-347">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="c9aa2-348">特定布林型別參數不再區分大小寫</span><span class="sxs-lookup"><span data-stu-id="c9aa2-348">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="c9aa2-349">支援在內部部署伺服器上登入 ADFS，例如 Azure Stack</span><span class="sxs-lookup"><span data-stu-id="c9aa2-349">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="c9aa2-350">已修正並行寫入 clouds.config (#3255)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-350">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="c9aa2-351">ACR</span><span class="sxs-lookup"><span data-stu-id="c9aa2-351">ACR</span></span>

* <span data-ttu-id="c9aa2-352">已新增受控登錄的 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-352">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="c9aa2-353">支援受控登錄的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="c9aa2-353">Support SKU update for managed registries</span></span>
* <span data-ttu-id="c9aa2-354">已新增使用受控 SKU 的受控登錄</span><span class="sxs-lookup"><span data-stu-id="c9aa2-354">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="c9aa2-355">已新增使用 ACR Webhook 命令模組的受控登錄 Webhook</span><span class="sxs-lookup"><span data-stu-id="c9aa2-355">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="c9aa2-356">已新增使用 ACR 登入命令進行 AAD 驗證</span><span class="sxs-lookup"><span data-stu-id="c9aa2-356">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="c9aa2-357">已新增 Docker 存放庫、資訊清單及標籤的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-357">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-358">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-358">ACS</span></span>

* <span data-ttu-id="c9aa2-359">支援 2017-07-01 版 API</span><span class="sxs-lookup"><span data-stu-id="c9aa2-359">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-360">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-360">Appservice</span></span>

* <span data-ttu-id="c9aa2-361">已修正列出 Linux Webapp 不會傳回任何項目的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-361">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="c9aa2-362">支援從 ACR 擷取認證</span><span class="sxs-lookup"><span data-stu-id="c9aa2-362">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="c9aa2-363">將 `appservice web` 底下的所有命令移除</span><span class="sxs-lookup"><span data-stu-id="c9aa2-363">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="c9aa2-364">命令輸出中的遮罩 Docker 登錄密碼 (#3656)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-364">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="c9aa2-365">請確定在 macOS 上使用預設瀏覽器不會發生錯誤 (#3623)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-365">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="c9aa2-366">改善的 `webapp log tail` 和 `webapp log download` 說明 (#3624)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-366">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="c9aa2-367">已公開可設定靜態路由的 `traffic-routing` 命令 (#3566)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-367">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="c9aa2-368">已新增設定原始檔控制中的可靠性修正 (#3245)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-368">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="c9aa2-369">已從適用於 Windows webapps 的 `webapp config update` 移除不支援的 `--node-version` 引數。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-369">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="c9aa2-370">請改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-370">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="c9aa2-371">批次</span><span class="sxs-lookup"><span data-stu-id="c9aa2-371">Batch</span></span>

* <span data-ttu-id="c9aa2-372">已更新至 Batch SDK 3.0.0 並支援集區中的低優先權 VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-372">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="c9aa2-373">已將 `pool create` 選項 `--target-dedicated` 重新命名為 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-373">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="c9aa2-374">已新增 `pool create` 選項 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-374">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="c9aa2-375">CDN</span><span class="sxs-lookup"><span data-stu-id="c9aa2-375">CDN</span></span>

* <span data-ttu-id="c9aa2-376">當 `--profile-name` 所指定的設定檔不存在時，已針對 `cdn endpoint list` 提供更好的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-376">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="c9aa2-377">雲端</span><span class="sxs-lookup"><span data-stu-id="c9aa2-377">Cloud</span></span>

* <span data-ttu-id="c9aa2-378">已將雲端中繼資料端點的 API 版本變更為 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-378">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="c9aa2-379">不需要資源庫端點</span><span class="sxs-lookup"><span data-stu-id="c9aa2-379">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="c9aa2-380">支援只向 ARM 資源管理員端點註冊雲端</span><span class="sxs-lookup"><span data-stu-id="c9aa2-380">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="c9aa2-381">已提供 `cloud set` 的選項，可在選取目前的雲端時選擇設定檔</span><span class="sxs-lookup"><span data-stu-id="c9aa2-381">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="c9aa2-382">已公開 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-382">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c9aa2-383">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c9aa2-383">CosmosDB</span></span>

* <span data-ttu-id="c9aa2-384">已修正允許使用自訂的分割區索引鍵來建立集合</span><span class="sxs-lookup"><span data-stu-id="c9aa2-384">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="c9aa2-385">已新增集合預設 TTL 的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-385">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c9aa2-386">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c9aa2-386">Data Lake Analytics</span></span>

* <span data-ttu-id="c9aa2-387">已新增在 `dla account compute-policy` 標題下計算原則管理的命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-387">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="c9aa2-388">已新增 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-388">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="c9aa2-389">已新增 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-389">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c9aa2-390">資料湖存放區</span><span class="sxs-lookup"><span data-stu-id="c9aa2-390">Data Lake Store</span></span>

* <span data-ttu-id="c9aa2-391">已新增在 `dls account update` 中使用者受控金鑰保存庫金鑰旋轉的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-391">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="c9aa2-392">已更新基礎 Data Lake Store filesystem SDK 版本，從而解決效能問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-392">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="c9aa2-393">已新增命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-393">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="c9aa2-394">此命令會嘗試啟用使用者所提供用於將 Data Lake Store 帳戶中之資料加密的 Key Vault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-394">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="c9aa2-395">互動式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-395">Interactive</span></span>

* <span data-ttu-id="c9aa2-396">已使用快取的命令來改善啟動時間</span><span class="sxs-lookup"><span data-stu-id="c9aa2-396">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="c9aa2-397">已增加測試涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="c9aa2-397">Increased test coverage</span></span>
* <span data-ttu-id="c9aa2-398">已增強 '?' 手勢以便同時插入下一個命令中</span><span class="sxs-lookup"><span data-stu-id="c9aa2-398">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="c9aa2-399">已修正包含設定檔 2017-03-09-profile-preview 的互動式錯誤 (#3587)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-399">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="c9aa2-400">已允許 `--version` 作為互動式模式的參數 (#3645)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-400">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="c9aa2-401">停止從驗證完成擲回錯誤的互動模式 (#3570)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-401">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="c9aa2-402">範本部署的進度報告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-402">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c9aa2-403">已新增 `--progress` 旗標</span><span class="sxs-lookup"><span data-stu-id="c9aa2-403">Added `--progress` flag</span></span>
* <span data-ttu-id="c9aa2-404">已從完成將 `--debug` 和 `--verbose` 移除</span><span class="sxs-lookup"><span data-stu-id="c9aa2-404">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="c9aa2-405">已從完成將 `interactive` 移除 (#3324)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-405">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="c9aa2-406">IoT</span><span class="sxs-lookup"><span data-stu-id="c9aa2-406">IoT</span></span>

* <span data-ttu-id="c9aa2-407">已修正建立原則時無法再清除現有的原則。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-407">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="c9aa2-408">(#3934)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-408">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="c9aa2-409">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="c9aa2-409">Key vault</span></span>

* <span data-ttu-id="c9aa2-410">已新增金鑰保存庫復原功能的命令：</span><span class="sxs-lookup"><span data-stu-id="c9aa2-410">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="c9aa2-411">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-411">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="c9aa2-412">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-412">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c9aa2-413">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-413">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c9aa2-414">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-414">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="c9aa2-415">已新增服務主體金鑰保存庫整合 (#3133)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-415">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="c9aa2-416">已將金鑰保存庫資料平面更新為 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-416">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="c9aa2-417">(#3307)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-417">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="c9aa2-418">實驗室</span><span class="sxs-lookup"><span data-stu-id="c9aa2-418">Lab</span></span>

* <span data-ttu-id="c9aa2-419">已新增透過 `az lab vm claim` 在實驗室中宣告任何 VM 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-419">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="c9aa2-420">已新增 `az lab vm list` 和 `az lab vm show` 的資料表輸出格式器</span><span class="sxs-lookup"><span data-stu-id="c9aa2-420">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="c9aa2-421">監視</span><span class="sxs-lookup"><span data-stu-id="c9aa2-421">Monitor</span></span>

* <span data-ttu-id="c9aa2-422">使用 `monitor autoscale-settings get-parameters-template` 命令修正範本檔案 (#3349)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-422">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="c9aa2-423">已將 `monitor alert-rule-incidents list` 重新命名為 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-423">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="c9aa2-424">已將 `monitor alert-rule-incidents show` 重新命名為 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-424">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="c9aa2-425">已將 `monitor metric-defintions list` 重新命名為 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-425">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="c9aa2-426">已將 `monitor alert-rules` 重新命名為 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-426">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="c9aa2-427">已變更 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="c9aa2-427">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="c9aa2-428">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="c9aa2-428">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="c9aa2-429">新增多個參數以簡化規則建立程序</span><span class="sxs-lookup"><span data-stu-id="c9aa2-429">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="c9aa2-430">已不再需要 `location`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-430">`location` no longer required</span></span>
  * <span data-ttu-id="c9aa2-431">新增目標的名稱和 ID 支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-431">Add name and ID support for target</span></span>
  * <span data-ttu-id="c9aa2-432">已移除 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-432">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="c9aa2-433">已不再需要將 `is-enabled` 重新命名為 `enabled`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-433">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="c9aa2-434">`description` 預設值現在會以所提供的條件作為基礎</span><span class="sxs-lookup"><span data-stu-id="c9aa2-434">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="c9aa2-435">新增範例來協助釐清新格式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-435">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="c9aa2-436">支援 `monitor metric` 命令的名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-436">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="c9aa2-437">已將便利性引數和範例新增至 `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-437">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-438">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-438">Network</span></span>

* <span data-ttu-id="c9aa2-439">已新增 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-439">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="c9aa2-440">已將 `--private-access-services` 引數新增至 `vnet subnet create` 和 `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-440">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="c9aa2-441">已修正 `application-gateway redirect-config create` 會失敗的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-441">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="c9aa2-442">已修正 `application-gateway redirect-config update` 無法與 `--no-wait` 搭配運作的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-442">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="c9aa2-443">已修正使用 `--servers` 引數搭配 `application-gateway address-pool create` 和 `application-gateway address-pool update` 時的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-443">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="c9aa2-444">已新增 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-444">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="c9aa2-445">已將命令新增至 `application-gateway ssl-policy`：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-445">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="c9aa2-446">已將引數新增至 `application-gateway ssl-policy set`：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-446">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="c9aa2-447">已將引數新增至 `application-gateway http-settings create` 和 `application-gateway http-settings update`：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-447">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="c9aa2-448">已將引數新增至 `application-gateway url-path-map create` 和 `application-gateway url-path-map update`：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-448">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="c9aa2-449">已將引數 `--redirect-config` 新增至 `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-449">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="c9aa2-450">已將 `--no-wait` 的支援新增至 `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-450">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="c9aa2-451">已將引數新增至 `application-gateway probe create` 和 `application-gateway probe update`：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-451">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="c9aa2-452">已將引數 `--redirect-config` 新增至 `application-gateway rule create` 和 `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-452">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="c9aa2-453">已將 `--accelerated-networking` 的支援新增至 `nic create` 和 `nic update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-453">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="c9aa2-454">已從 `nic create` 移除 `--internal-dns-name-suffix` 引數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-454">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="c9aa2-455">已將 `--dns-servers` 的支援新增至 `nic update` 和 `nic create`：已新增 --dns-servers 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-455">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="c9aa2-456">已修正 `local-gateway create` 忽略 `--local-address-prefixes` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-456">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="c9aa2-457">已將 `--dns-servers` 的支援新增至 `vnet update`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-457">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="c9aa2-458">已修正使用 `express-route peering create` 時建立不含路由篩選條件之對等互連的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-458">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="c9aa2-459">已修正 `--provider` 和 `--bandwidth` 引數無法使用 `express-route update` 的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-459">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="c9aa2-460">已修正 `network watcher show-topology` 預設邏輯的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-460">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="c9aa2-461">已改良 `network list-usages` 的輸出格式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-461">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="c9aa2-462">如果只有一個，請使用 `application-gateway http-listener create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="c9aa2-462">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="c9aa2-463">如果只有一個，請使用 `application-gateway rule create` 的預設位址集區、HTTP 設定和 HTTP 接聽程式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-463">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="c9aa2-464">如果只有一個，請使用 `lb rule create` 的預設前端 IP 和後端集區</span><span class="sxs-lookup"><span data-stu-id="c9aa2-464">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="c9aa2-465">如果只有一個，請使用 `lb inbound-nat-rule create` 的預設前端 IP</span><span class="sxs-lookup"><span data-stu-id="c9aa2-465">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="c9aa2-466">設定檔</span><span class="sxs-lookup"><span data-stu-id="c9aa2-466">Profile</span></span>

* <span data-ttu-id="c9aa2-467">支援使用受管理的身分識別在 VM 內部登入</span><span class="sxs-lookup"><span data-stu-id="c9aa2-467">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="c9aa2-468">支援 SDK 驗證檔案格式的 `account show` 輸出</span><span class="sxs-lookup"><span data-stu-id="c9aa2-468">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="c9aa2-469">使用 '--expanded-view' 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="c9aa2-469">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="c9aa2-470">已新增 `get-access-token` 命令，以提供原始 AAD 權杖</span><span class="sxs-lookup"><span data-stu-id="c9aa2-470">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="c9aa2-471">支援透過沒有相關聯訂用帳戶的使用者帳戶進行登入</span><span class="sxs-lookup"><span data-stu-id="c9aa2-471">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="c9aa2-472">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-472">RDBMS</span></span>

* <span data-ttu-id="c9aa2-473">支援列出跨訂用帳戶的伺服器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-473">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="c9aa2-474">已修正因遺漏 `% server_type` 而未處理 `%s` (#3393)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-474">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="c9aa2-475">已修正文件來源對應並已新增 CI 工作以進行確認 (#3361)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-475">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="c9aa2-476">已修正 MySQL 和 PostgreSQL 說明 (#3369)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-476">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-477">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-477">Resource</span></span>

* <span data-ttu-id="c9aa2-478">已改善遺漏 `group deployment create` 參數的提示</span><span class="sxs-lookup"><span data-stu-id="c9aa2-478">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="c9aa2-479">已改善 `--parameters KEY=VALUE` 語法的剖析</span><span class="sxs-lookup"><span data-stu-id="c9aa2-479">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="c9aa2-480">已修正無法再使用 `@<file>` 語法辨識 `group deployment create` 參數檔案的問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-480">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="c9aa2-481">支援 `resource` 和 `managedapp` 命令的 `--ids` 引數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-481">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="c9aa2-482">已修正某些剖析和錯誤訊息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-482">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="c9aa2-483">已修正 `lock` 命令的 `--resource-type` 剖析，以接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-483">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="c9aa2-484">已新增範本連結範本的參數檢查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-484">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="c9aa2-485">已新增使用 `KEY=VALUE` 語法指定部署參數的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-485">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="c9aa2-486">角色</span><span class="sxs-lookup"><span data-stu-id="c9aa2-486">Role</span></span>

* <span data-ttu-id="c9aa2-487">支援 SDK 驗證檔案格式的 `create-for-rbac` 輸出</span><span class="sxs-lookup"><span data-stu-id="c9aa2-487">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="c9aa2-488">已清除在刪除服務主體時的角色指派和相關 AAD 應用程式 (#3610)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-488">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="c9aa2-489">包含 `app create` 引數 `--start-date` 和 `--end-date` 描述中的時間格式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-489">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="c9aa2-490">使用 `--expanded-view` 時，顯示取代警告</span><span class="sxs-lookup"><span data-stu-id="c9aa2-490">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="c9aa2-491">已新增金鑰保存庫整合至 `create-for-rbac` 和 `reset-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="c9aa2-491">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c9aa2-492">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c9aa2-492">Service Fabric</span></span>
* <span data-ttu-id="c9aa2-493">已修正應用程式中的大型檔案在上傳時被截斷的問題 (#3666)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-493">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="c9aa2-494">已新增適用於 Service Fabric 命令的測試 (#3424)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-494">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="c9aa2-495">已修正許多 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-495">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="c9aa2-496">SQL</span><span class="sxs-lookup"><span data-stu-id="c9aa2-496">SQL</span></span>

* <span data-ttu-id="c9aa2-497">已移除中斷的 `sql server create` `--identity` 參數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-497">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="c9aa2-498">已從 `sql server create` 和 `sql server update` 命令輸出移除密碼值</span><span class="sxs-lookup"><span data-stu-id="c9aa2-498">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="c9aa2-499">已新增命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="c9aa2-499">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-500">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-500">Storage</span></span>

* <span data-ttu-id="c9aa2-501">已從 `storage blob list`、`storage container list` 和 `storage share list` 命令移除 `--marker` 選項 (#3745)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-501">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="c9aa2-502">已啟用建立 https 專用儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="c9aa2-502">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="c9aa2-503">已更新儲存體計量、記錄和 cors 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-503">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="c9aa2-504">已從 CORS 新增改換措辭例外狀況訊息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-504">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="c9aa2-505">已將產生器轉換為下載批次命令不重複原則執行模式中的清單 (#3592)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-505">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="c9aa2-506">已修正 blob 下載批次不重複原則執行問題 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-506">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-507">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-507">VM</span></span>

* <span data-ttu-id="c9aa2-508">支援設定 NSG</span><span class="sxs-lookup"><span data-stu-id="c9aa2-508">Support configuring nsg</span></span>
* <span data-ttu-id="c9aa2-509">已修正 DNS 伺服器未正確設定的錯誤</span><span class="sxs-lookup"><span data-stu-id="c9aa2-509">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="c9aa2-510">支援受管理的服務身分識別</span><span class="sxs-lookup"><span data-stu-id="c9aa2-510">Support managed service identities</span></span>
* <span data-ttu-id="c9aa2-511">已修正 `cmss create` 與現有負載平衡器需要 `--backend-pool-name` 的問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-511">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="c9aa2-512">請使用開頭為 0 的 `vm image create` lun 建立 DataDisk</span><span class="sxs-lookup"><span data-stu-id="c9aa2-512">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="c9aa2-513">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-513">May 10, 2017</span></span>

<span data-ttu-id="c9aa2-514">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="c9aa2-514">Version 2.0.6</span></span>

* <span data-ttu-id="c9aa2-515">documentdb 已重新命名為 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="c9aa2-515">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="c9aa2-516">新增 rdbms (mysql、postgres)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-516">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="c9aa2-517">包含 Data Lake Analytics 和 Data Lake Store 模組。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-517">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="c9aa2-518">包含「辨識服務」模組。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-518">Include Cognitive Services module.</span></span>
* <span data-ttu-id="c9aa2-519">包含 Service Fabric 模組。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-519">Include Service Fabric module.</span></span>
* <span data-ttu-id="c9aa2-520">包含「互動式」模組 (az-shell 的重新命名)。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-520">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="c9aa2-521">新增對 CDN 命令的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-521">Add support for CDN commands.</span></span>
* <span data-ttu-id="c9aa2-522">移除「容器」模組。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-522">Remove Container module.</span></span>
* <span data-ttu-id="c9aa2-523">新增 'az -v' 作為 'az --version' 的捷徑 ([#2926 (英文)](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-523">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="c9aa2-524">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-524">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="c9aa2-525">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-525">Core</span></span>

* <span data-ttu-id="c9aa2-526">核心：捕捉未註冊提供者所造成的例外狀況，並自動註冊該提供者</span><span class="sxs-lookup"><span data-stu-id="c9aa2-526">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="c9aa2-527">效能：將 adal 權杖快取保存在記憶體中，直到程序結束為止 ([#2603 (英文)](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-527">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="c9aa2-528">修正從十六進位指紋 -o tsv 傳回的位元組 ([#3053 (英文)](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-528">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="c9aa2-529">增強 Key Vault 憑證下載和 AAD SP 的整合 ([#3003 (英文)](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-529">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="c9aa2-530">在 ‘az —version’ 中新增 Python 位置 ([#2986 (英文)](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-530">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="c9aa2-531">登入：支援在沒有訂用帳戶時進行登入 ([#2929 (英文)](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-531">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="c9aa2-532">核心：修正使用服務主體登入兩次時所發生的失敗 ([#2800 (英文)](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-532">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="c9aa2-533">核心：允許透過環境變數設定 accessTokens.json 的檔案路徑 ([#2605 (英文)](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-533">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="c9aa2-534">核心：允許將已設定的預設值套用到選擇性引數 ([#2703 (英文)](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-534">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="c9aa2-535">核心：提升效能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-535">core: Improved performance</span></span>
* <span data-ttu-id="c9aa2-536">核心：自訂 CA 憑證 - 支援設定 REQUESTS_CA_BUNDLE 環境變數</span><span class="sxs-lookup"><span data-stu-id="c9aa2-536">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="c9aa2-537">核心：雲端組態 - 如果未設定「管理」端點，則使用「資源管理員」端點</span><span class="sxs-lookup"><span data-stu-id="c9aa2-537">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="c9aa2-538">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-538">ACS</span></span>

* <span data-ttu-id="c9aa2-539">將主要和代理程式計數修正為整數，而不是字串</span><span class="sxs-lookup"><span data-stu-id="c9aa2-539">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="c9aa2-540">公開 'az acs create --no-wait' 和 'az acs wait' 以進行非同步建立</span><span class="sxs-lookup"><span data-stu-id="c9aa2-540">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="c9aa2-541">公開 'az acs create --validate' 以進行試執行驗證</span><span class="sxs-lookup"><span data-stu-id="c9aa2-541">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="c9aa2-542">在進行 scale 命令的 PUT 呼叫之前，先移除 Windows 設定檔 ([#2755 (英文)](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-542">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="c9aa2-543">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-543">AppService</span></span>

* <span data-ttu-id="c9aa2-544">functionapp：新增完整的 functionapp 支援，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="c9aa2-544">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="c9aa2-545">新增 Team Services (vsts) 作為 "appservice web source-control config" 的持續傳遞選項</span><span class="sxs-lookup"><span data-stu-id="c9aa2-545">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="c9aa2-546">建立 "az webapp" 以取代 "az appservice web" (用於回溯相容性，"az appservice web" 的存續期將再延續 2 個版本)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-546">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="c9aa2-547">公開引數以在執行 webapp create 時設定部署和「執行階段堆疊」</span><span class="sxs-lookup"><span data-stu-id="c9aa2-547">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="c9aa2-548">公開 "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="c9aa2-548">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="c9aa2-549">支援設定連接字串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-549">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="c9aa2-550">支援附帶預覽功能的位置交換</span><span class="sxs-lookup"><span data-stu-id="c9aa2-550">support slot swap with preview</span></span>
* <span data-ttu-id="c9aa2-551">修飾來自 appservice 命令的錯誤 ([#2948 (英文)](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-551">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="c9aa2-552">使用 App Service 方案的資源群組來進行憑證作業 ([#2750 (英文)](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-552">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c9aa2-553">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c9aa2-553">CosmosDB</span></span>

* <span data-ttu-id="c9aa2-554">將 documentdb 模組重新命名為 cosmosdb。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-554">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="c9aa2-555">新增對 documentdb 資料層 API 的支援：資料庫和集合管理</span><span class="sxs-lookup"><span data-stu-id="c9aa2-555">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="c9aa2-556">新增對在資料庫帳戶上啟用自動容錯移轉的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-556">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="c9aa2-557">新增對新一致性原則 ConsistentPrefix 的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-557">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c9aa2-558">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c9aa2-558">Data Lake Analytics</span></span>

* <span data-ttu-id="c9aa2-559">修正依工作清單的結果和狀態篩選會導致擲回錯誤的 Bug。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-559">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="c9aa2-560">新增對下列新類別目錄項目類型的支援：套件。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-560">Add support for new catalog item type: package.</span></span> <span data-ttu-id="c9aa2-561">透過 `az dla catalog package` 進行存取</span><span class="sxs-lookup"><span data-stu-id="c9aa2-561">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="c9aa2-562">能夠從資料庫內列出下列類別目錄項目 (不需指定結構描述)：</span><span class="sxs-lookup"><span data-stu-id="c9aa2-562">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="c9aa2-563">資料表</span><span class="sxs-lookup"><span data-stu-id="c9aa2-563">Table</span></span>
  * <span data-ttu-id="c9aa2-564">資料表值函式</span><span class="sxs-lookup"><span data-stu-id="c9aa2-564">Table valued function</span></span>
  * <span data-ttu-id="c9aa2-565">檢視</span><span class="sxs-lookup"><span data-stu-id="c9aa2-565">View</span></span>
  * <span data-ttu-id="c9aa2-566">資料表統計資料。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-566">Table Statistics.</span></span> <span data-ttu-id="c9aa2-567">這也可以使用結構描述來列出，但不需要指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-567">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c9aa2-568">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c9aa2-568">Data Lake Store</span></span>

* <span data-ttu-id="c9aa2-569">更新基礎檔案系統 SDK 的版本，以提供更佳的支援來處理伺服器端節流情況。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-569">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="c9aa2-570">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-570">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="c9aa2-571">遺失 access show 的說明。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-571">missed help for access show.</span></span> <span data-ttu-id="c9aa2-572">將新增此說明。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-572">adding it.</span></span> <span data-ttu-id="c9aa2-573">([#2743 (英文)](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-573">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="c9aa2-574">尋找</span><span class="sxs-lookup"><span data-stu-id="c9aa2-574">Find</span></span>

* <span data-ttu-id="c9aa2-575">改善搜尋結果，並允許進行搜尋索引版本控制</span><span class="sxs-lookup"><span data-stu-id="c9aa2-575">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="c9aa2-576">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c9aa2-576">KeyVault</span></span>

* <span data-ttu-id="c9aa2-577">BC：`az keyvault certificate download`將 -e 從字串或二進位變更為 PEM 或 DER，來以更佳的方式代表選項</span><span class="sxs-lookup"><span data-stu-id="c9aa2-577">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="c9aa2-578">BC：從 `keyvault certificate create` 中移除 --expires 和 --not-before，因為服務不支援這些參數。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-578">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="c9aa2-579">在 `keyvault certificate create` 中新增 --validity 參數，以選擇性地覆寫 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="c9aa2-579">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="c9aa2-580">修正 `keyvault certificate get-default-policy` 中公開 'expires' 和 'not_before' 但未公開 'validity_in_months' 的問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-580">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="c9aa2-581">用於匯入 pem 和 pfx 的 keyvault 修正 ([#2754 (英文)](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-581">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="c9aa2-582">實驗室</span><span class="sxs-lookup"><span data-stu-id="c9aa2-582">Lab</span></span>

* <span data-ttu-id="c9aa2-583">新增適用於實驗室中環境的 create、show、delete 及 list 命令。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-583">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="c9aa2-584">新增 show 和 list 命令以檢視實驗室中的 ARM 範本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-584">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="c9aa2-585">在 `az lab vm list` 中新增 --environment 旗標，以在實驗室中依環境篩選 VM。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-585">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="c9aa2-586">新增便利命令 `az lab formula export-artifacts` 以匯出實驗室公式內的構件結構。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-586">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="c9aa2-587">新增命令以管理實驗室內的密碼。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-587">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="c9aa2-588">監視</span><span class="sxs-lookup"><span data-stu-id="c9aa2-588">Monitor</span></span>

* <span data-ttu-id="c9aa2-589">Bug 修正：建立 `az alert-rules create` 的 `--actions` 模型以取用 JSON 字串 ([#3009 (英文)](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-589">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="c9aa2-590">Bug 修正：diagnostic-settings create 不接受來自 show 命令的記錄/計量 ([#2913 (英文)](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-590">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="c9aa2-591">網路</span><span class="sxs-lookup"><span data-stu-id="c9aa2-591">Network</span></span>

* <span data-ttu-id="c9aa2-592">新增 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-592">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="c9aa2-593">新增對 `network watcher packet-capture create` 之 `--filters` 參數的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-593">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="c9aa2-594">新增對「應用程式閘道」連線清空的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-594">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="c9aa2-595">新增對「應用程式閘道」WAF 規則集組態的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-595">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="c9aa2-596">新增對 ExpressRoute 路由篩選和規則的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-596">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="c9aa2-597">新增對 TrafficManager 地理路由的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-597">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="c9aa2-598">新增對 VPN 連線原則型流量選取器的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-598">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="c9aa2-599">新增對 VPN 連線 IPSec 原則的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-599">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="c9aa2-600">修正 `vpn-connection create` 搭配使用 `--no-wait` 或 `--validate` 參數時的 Bug。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-600">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="c9aa2-601">新增對「主動-主動」VNet 閘道的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-601">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="c9aa2-602">從 `network vpn-connection list/show` 命令移除 Null 值。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-602">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="c9aa2-603">BC：修正 `vpn-connection create` 之輸出中的 Bug</span><span class="sxs-lookup"><span data-stu-id="c9aa2-603">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="c9aa2-604">修正未正確剖析 'vpn-connection create' 之 '--key-length' 引數的 Bug。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-604">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="c9aa2-605">修正 `dns zone import` 中未正確匯入記錄的 Bug。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-605">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="c9aa2-606">修正 `traffic-manager endpoint update` 無法運作的 Bug。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-606">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="c9aa2-607">新增 'network watcher' 預覽命令。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-607">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="c9aa2-608">設定檔</span><span class="sxs-lookup"><span data-stu-id="c9aa2-608">Profile</span></span>

* <span data-ttu-id="c9aa2-609">支援在找不到訂用帳戶時進行登入 ([#2560 (英文)](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-609">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="c9aa2-610">在 az account set --subscription 中支援短參數名稱 ([#2980 (英文)](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-610">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="c9aa2-611">Redis</span><span class="sxs-lookup"><span data-stu-id="c9aa2-611">Redis</span></span>

* <span data-ttu-id="c9aa2-612">新增 update 命令，這也會為 redis 快取新增調整能力</span><span class="sxs-lookup"><span data-stu-id="c9aa2-612">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="c9aa2-613">取代 'update-settings' 命令。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-613">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="c9aa2-614">資源</span><span class="sxs-lookup"><span data-stu-id="c9aa2-614">Resource</span></span>

* <span data-ttu-id="c9aa2-615">新增 managedapp 和 managedapp definition 命令 ([#2985 (英文)](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-615">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="c9aa2-616">支援 'provider operation' 命令 ([#2908 (英文)](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-616">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="c9aa2-617">支援一般 resource create ([#2606 (英文)](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-617">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="c9aa2-618">修正資源剖析和 api 版本查詢。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-618">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="c9aa2-619">([#2781 (英文)](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-619">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="c9aa2-620">新增 az lock update 的文件。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-620">Add docs for az lock update.</span></span> <span data-ttu-id="c9aa2-621">([#2702 (英文)](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-621">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="c9aa2-622">如果您嘗試列出不存在之群組的資源，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-622">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="c9aa2-623">([#2769 (英文)](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-623">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="c9aa2-624">[計算] 修正 VMSS 和 VM 可用性設定組更新的相關問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-624">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="c9aa2-625">([#2773 (英文)](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-625">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="c9aa2-626">修正 parent-resource-path 為 None 時的 lock create 和 delete ([#2742 (英文)](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-626">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="c9aa2-627">角色</span><span class="sxs-lookup"><span data-stu-id="c9aa2-627">Role</span></span>

* <span data-ttu-id="c9aa2-628">create-for-rbac：確保 SP 的結束日期不會超過憑證的到期日 ([#2989 (英文)](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-628">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="c9aa2-629">RBAC：新增對 'ad group' 的完整支援 ([#2016 (英文)](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-629">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="c9aa2-630">角色：修正 role definition update 上的問題 ([#2745 (英文)](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-630">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="c9aa2-631">create-for-rbac：確保系統會挑選使用者提供的密碼</span><span class="sxs-lookup"><span data-stu-id="c9aa2-631">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="c9aa2-632">SQL</span><span class="sxs-lookup"><span data-stu-id="c9aa2-632">SQL</span></span>

* <span data-ttu-id="c9aa2-633">新增 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-633">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="c9aa2-634">SQL - 能夠直接連接到資源提供者 ([#2832 (英文)](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-634">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="c9aa2-635">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-635">Storage</span></span>

* <span data-ttu-id="c9aa2-636">`storage account create` 之資源群組位置的預設位置。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-636">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="c9aa2-637">新增對遞增 blob 複製的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-637">Add support for incremental blob copy</span></span>
* <span data-ttu-id="c9aa2-638">新增對大型區塊 blob 上傳的支援</span><span class="sxs-lookup"><span data-stu-id="c9aa2-638">Add support for large block blob upload</span></span>
* <span data-ttu-id="c9aa2-639">當要上傳的檔案大於 200 GB 時，將區塊大小變更為 100 MB</span><span class="sxs-lookup"><span data-stu-id="c9aa2-639">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-640">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-640">VM</span></span>

* <span data-ttu-id="c9aa2-641">avail-set：將 UD&FD 網域計數設定為選用</span><span class="sxs-lookup"><span data-stu-id="c9aa2-641">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="c9aa2-642">注意：主權雲端中的 VM 命令。請避免使用受管理磁碟相關的功能，包括下列功能：</span><span class="sxs-lookup"><span data-stu-id="c9aa2-642">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="c9aa2-643">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="c9aa2-643">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="c9aa2-644">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="c9aa2-644">az vm/vmss disk</span></span>
  3. <span data-ttu-id="c9aa2-645">在 "az vm/vmss create" 內，請使用 "—use-unmanaged-disk" 來避免使用受管理的磁碟。其他命令應該可運作</span><span class="sxs-lookup"><span data-stu-id="c9aa2-645">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="c9aa2-646">vm/vmss：改進產生 SSH 金鑰組時的警告文字</span><span class="sxs-lookup"><span data-stu-id="c9aa2-646">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="c9aa2-647">vm/vmss：支援從需要方案資訊的市場映像進行建立 ([#1209 (英文)](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-647">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="c9aa2-648">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-648">April 3, 2017</span></span>

<span data-ttu-id="c9aa2-649">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="c9aa2-649">Version 2.0.2</span></span>

<span data-ttu-id="c9aa2-650">在這一版中，我們發行了 ACR、Batch、KeyVault 和 SQL 元件。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-650">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="c9aa2-651">核心</span><span class="sxs-lookup"><span data-stu-id="c9aa2-651">Core</span></span>

* <span data-ttu-id="c9aa2-652">將 ACR、實驗室、監視及尋找模組新增至預設清單。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-652">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="c9aa2-653">Login︰略過錯誤的租用戶 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-653">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="c9aa2-654">Login︰將預設訂用帳戶設定為具有「已啟用」狀態的訂用帳戶 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-654">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="c9aa2-655">將 wait 命令和 --no-wait 支援新增至多個命令 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-655">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c9aa2-656">Core︰支援使用憑證的服務主體登入 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-656">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="c9aa2-657">新增遺漏範本參數的提示。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-657">Add prompting for missing template parameters.</span></span> <span data-ttu-id="c9aa2-658">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-658">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="c9aa2-659">支援設定諸如預設資源群組、預設 web、預設 VM 等常見引數的預設值</span><span class="sxs-lookup"><span data-stu-id="c9aa2-659">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="c9aa2-660">支援登入特定的租用戶</span><span class="sxs-lookup"><span data-stu-id="c9aa2-660">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="c9aa2-661">ACS</span><span class="sxs-lookup"><span data-stu-id="c9aa2-661">ACS</span></span>

* <span data-ttu-id="c9aa2-662">[ACS] 新增設定預設 ACS 叢集的支援 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-662">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="c9aa2-663">新增 SSH 金鑰密碼提示的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-663">Add support for ssh key password prompting.</span></span> <span data-ttu-id="c9aa2-664">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-664">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="c9aa2-665">新增 Windows 叢集的支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-665">Add support for windows clusters.</span></span> <span data-ttu-id="c9aa2-666">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-666">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="c9aa2-667">將角色從擁有者切換為參與者。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-667">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="c9aa2-668">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-668">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="c9aa2-669">AppService</span><span class="sxs-lookup"><span data-stu-id="c9aa2-669">AppService</span></span>

* <span data-ttu-id="c9aa2-670">appservice︰取得用於 DNS A 記錄之外部 IP 位址的支援 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-670">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="c9aa2-671">appservice︰支援繫結萬用字元憑證 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-671">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="c9aa2-672">appservice︰支援列出發行設定檔 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-672">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="c9aa2-673">AppService - 設定之後觸發原始檔控制同步處理 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-673">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="c9aa2-674">DataLake</span><span class="sxs-lookup"><span data-stu-id="c9aa2-674">DataLake</span></span>

* <span data-ttu-id="c9aa2-675">Data Lake Analytics 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-675">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="c9aa2-676">Data Lake Store 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-676">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="c9aa2-677">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="c9aa2-677">DocuemntDB</span></span>

* <span data-ttu-id="c9aa2-678">DocumentDB︰新增列出連接字串的支援 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-678">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="c9aa2-679">VM</span><span class="sxs-lookup"><span data-stu-id="c9aa2-679">VM</span></span>

* <span data-ttu-id="c9aa2-680">[Compute] 將 AppGateway 支援新增至虛擬機器擴展集建立 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-680">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="c9aa2-681">[VM/VMSS] 改良的磁碟快取支援 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-681">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="c9aa2-682">VM/VMSS︰併入入口網站所使用的認證驗證邏輯 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-682">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="c9aa2-683">新增 wait 命令和 --no-wait 支援 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-683">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c9aa2-684">虛擬機器擴展集︰支援 * 列出跨 VM 的執行個體檢視 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-684">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="c9aa2-685">新增 VM 和虛擬機器擴展集的 --祕密 ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-685">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="c9aa2-686">可使用特殊的 VHD 來建立 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="c9aa2-686">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="c9aa2-687">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="c9aa2-687">February 27, 2017</span></span>

<span data-ttu-id="c9aa2-688">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="c9aa2-688">Version 2.0.0</span></span>

<span data-ttu-id="c9aa2-689">此版本的 Azure CLI 2.0 是第一個「正式運作」版本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-689">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="c9aa2-690">正式運作適用於下列的命令模組︰</span><span class="sxs-lookup"><span data-stu-id="c9aa2-690">General availability applies to these command modules:</span></span>
- <span data-ttu-id="c9aa2-691">Container Service (ACS)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-691">Container Service (acs)</span></span>
- <span data-ttu-id="c9aa2-692">計算 (包含 Resource Manager、VM、虛擬機器擴展集、受控磁碟)</span><span class="sxs-lookup"><span data-stu-id="c9aa2-692">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="c9aa2-693">網路功能</span><span class="sxs-lookup"><span data-stu-id="c9aa2-693">Networking</span></span>
- <span data-ttu-id="c9aa2-694">儲存體</span><span class="sxs-lookup"><span data-stu-id="c9aa2-694">Storage</span></span>

<span data-ttu-id="c9aa2-695">這些命令模組可用在生產環境中，且受標準 Microsoft SLA 支援。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-695">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="c9aa2-696">您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)開啟問題。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-696">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="c9aa2-697">您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。您可以從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-697">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="c9aa2-698">這些模組中的命令很穩定，且不應該變更此版 Azure CLI 之未來版本的語法。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-698">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="c9aa2-699">若要確認的 CLI 的版本，請使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-699">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="c9aa2-700">輸出會列出 CLI 本身的版本 (此版本中為 2.0.0)、個別的命令模組，以及您所使用的 Python 和 GCC 版本。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-700">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="c9aa2-701">些命令模組會有 "b*n*" 或 "rc*n*" 後置詞。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-701">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="c9aa2-702">這些命令模組仍處於預覽狀態，且未來會正式運作。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-702">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="c9aa2-703">我們也有 CLI 的夜間預覽組建。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-703">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="c9aa2-704">如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-704">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="c9aa2-705">您可以透過下列方式來報告夜間預覽組建的問題︰</span><span class="sxs-lookup"><span data-stu-id="c9aa2-705">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="c9aa2-706">在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)中報告問題</span><span class="sxs-lookup"><span data-stu-id="c9aa2-706">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="c9aa2-707">連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-707">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="c9aa2-708">從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="c9aa2-708">Provide feedback from the command line with the `az feedback` command.</span></span>

