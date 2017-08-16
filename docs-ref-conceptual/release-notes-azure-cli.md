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
ms.contentlocale: zh-TW
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="b89b3-104">Azure CLI 2.0 版本資訊</span><span class="sxs-lookup"><span data-stu-id="b89b3-104">Azure CLI 2.0 release notes</span></span>

## <a name="may-10-2017"></a><span data-ttu-id="b89b3-105">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b89b3-105">May 10, 2017</span></span>

<span data-ttu-id="b89b3-106">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="b89b3-106">Version 2.0.6</span></span>

* <span data-ttu-id="b89b3-107">documentdb 已重新命名為 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="b89b3-107">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="b89b3-108">新增 rdbms (mysql、postgres)</span><span class="sxs-lookup"><span data-stu-id="b89b3-108">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="b89b3-109">包含 Data Lake Analytics 和 Data Lake Store 模組。</span><span class="sxs-lookup"><span data-stu-id="b89b3-109">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="b89b3-110">包含「辨識服務」模組。</span><span class="sxs-lookup"><span data-stu-id="b89b3-110">Include Cognitive Services module.</span></span>
* <span data-ttu-id="b89b3-111">包含 Service Fabric 模組。</span><span class="sxs-lookup"><span data-stu-id="b89b3-111">Include Service Fabric module.</span></span>
* <span data-ttu-id="b89b3-112">包含「互動式」模組 (az-shell 的重新命名)。</span><span class="sxs-lookup"><span data-stu-id="b89b3-112">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="b89b3-113">新增對 CDN 命令的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-113">Add support for CDN commands.</span></span>
* <span data-ttu-id="b89b3-114">移除「容器」模組。</span><span class="sxs-lookup"><span data-stu-id="b89b3-114">Remove Container module.</span></span>
* <span data-ttu-id="b89b3-115">新增 'az -v' 作為 'az --version' 的捷徑 ([#2926 (英文)](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="b89b3-115">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="b89b3-116">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b89b3-116">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="b89b3-117">核心</span><span class="sxs-lookup"><span data-stu-id="b89b3-117">Core</span></span>

* <span data-ttu-id="b89b3-118">核心：捕捉未註冊提供者所造成的例外狀況，並自動註冊該提供者</span><span class="sxs-lookup"><span data-stu-id="b89b3-118">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="b89b3-119">效能：將 adal 權杖快取保存在記憶體中，直到程序結束為止 ([#2603 (英文)](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="b89b3-119">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="b89b3-120">修正從十六進位指紋 -o tsv 傳回的位元組 ([#3053 (英文)](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="b89b3-120">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="b89b3-121">增強 Key Vault 憑證下載和 AAD SP 的整合 ([#3003 (英文)](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="b89b3-121">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="b89b3-122">在 ‘az —version’ 中新增 Python 位置 ([#2986 (英文)](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="b89b3-122">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="b89b3-123">登入：支援在沒有訂用帳戶時進行登入 ([#2929 (英文)](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="b89b3-123">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="b89b3-124">核心：修正使用服務主體登入兩次時所發生的失敗 ([#2800 (英文)](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="b89b3-124">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="b89b3-125">核心：允許透過環境變數設定 accessTokens.json 的檔案路徑 ([#2605 (英文)](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="b89b3-125">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="b89b3-126">核心：允許將已設定的預設值套用到選擇性引數 ([#2703 (英文)](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="b89b3-126">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="b89b3-127">核心：提升效能</span><span class="sxs-lookup"><span data-stu-id="b89b3-127">core: Improved performance</span></span>
* <span data-ttu-id="b89b3-128">核心：自訂 CA 憑證 - 支援設定 REQUESTS_CA_BUNDLE 環境變數</span><span class="sxs-lookup"><span data-stu-id="b89b3-128">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="b89b3-129">核心：雲端組態 - 如果未設定「管理」端點，則使用「資源管理員」端點</span><span class="sxs-lookup"><span data-stu-id="b89b3-129">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="b89b3-130">ACS</span><span class="sxs-lookup"><span data-stu-id="b89b3-130">ACS</span></span>

* <span data-ttu-id="b89b3-131">將主要和代理程式計數修正為整數，而不是字串</span><span class="sxs-lookup"><span data-stu-id="b89b3-131">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="b89b3-132">公開 'az acs create --no-wait' 和 'az acs wait' 以進行非同步建立</span><span class="sxs-lookup"><span data-stu-id="b89b3-132">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="b89b3-133">公開 'az acs create --validate' 以進行試執行驗證</span><span class="sxs-lookup"><span data-stu-id="b89b3-133">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="b89b3-134">在進行 scale 命令的 PUT 呼叫之前，先移除 Windows 設定檔 ([#2755 (英文)](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="b89b3-134">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="b89b3-135">AppService</span><span class="sxs-lookup"><span data-stu-id="b89b3-135">AppService</span></span>

* <span data-ttu-id="b89b3-136">functionapp：新增完整的 functionapp 支援，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="b89b3-136">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="b89b3-137">新增 Team Services (vsts) 作為 "appservice web source-control config" 的持續傳遞選項</span><span class="sxs-lookup"><span data-stu-id="b89b3-137">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="b89b3-138">建立 "az webapp" 以取代 "az appservice web" (用於回溯相容性，"az appservice web" 的存續期將再延續 2 個版本)</span><span class="sxs-lookup"><span data-stu-id="b89b3-138">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="b89b3-139">公開引數以在執行 webapp create 時設定部署和「執行階段堆疊」</span><span class="sxs-lookup"><span data-stu-id="b89b3-139">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="b89b3-140">公開 "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="b89b3-140">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="b89b3-141">支援設定連接字串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="b89b3-141">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="b89b3-142">支援附帶預覽功能的位置交換</span><span class="sxs-lookup"><span data-stu-id="b89b3-142">support slot swap with preview</span></span>
* <span data-ttu-id="b89b3-143">修飾來自 appservice 命令的錯誤 ([#2948 (英文)](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="b89b3-143">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="b89b3-144">使用 App Service 方案的資源群組來進行憑證作業 ([#2750 (英文)](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="b89b3-144">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b89b3-145">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b89b3-145">CosmosDB</span></span>

* <span data-ttu-id="b89b3-146">將 documentdb 模組重新命名為 cosmosdb。</span><span class="sxs-lookup"><span data-stu-id="b89b3-146">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="b89b3-147">新增對 documentdb 資料層 API 的支援：資料庫和集合管理</span><span class="sxs-lookup"><span data-stu-id="b89b3-147">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="b89b3-148">新增對在資料庫帳戶上啟用自動容錯移轉的支援</span><span class="sxs-lookup"><span data-stu-id="b89b3-148">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="b89b3-149">新增對新一致性原則 ConsistentPrefix 的支援</span><span class="sxs-lookup"><span data-stu-id="b89b3-149">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b89b3-150">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b89b3-150">Data Lake Analytics</span></span>

* <span data-ttu-id="b89b3-151">修正依工作清單的結果和狀態篩選會導致擲回錯誤的 Bug。</span><span class="sxs-lookup"><span data-stu-id="b89b3-151">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="b89b3-152">新增對下列新類別目錄項目類型的支援：套件。</span><span class="sxs-lookup"><span data-stu-id="b89b3-152">Add support for new catalog item type: package.</span></span> <span data-ttu-id="b89b3-153">透過 `az dla catalog package` 進行存取</span><span class="sxs-lookup"><span data-stu-id="b89b3-153">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="b89b3-154">能夠從資料庫內列出下列類別目錄項目 (不需指定結構描述)：</span><span class="sxs-lookup"><span data-stu-id="b89b3-154">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="b89b3-155">資料表</span><span class="sxs-lookup"><span data-stu-id="b89b3-155">Table</span></span>
  * <span data-ttu-id="b89b3-156">資料表值函式</span><span class="sxs-lookup"><span data-stu-id="b89b3-156">Table valued function</span></span>
  * <span data-ttu-id="b89b3-157">檢視</span><span class="sxs-lookup"><span data-stu-id="b89b3-157">View</span></span>
  * <span data-ttu-id="b89b3-158">資料表統計資料。</span><span class="sxs-lookup"><span data-stu-id="b89b3-158">Table Statistics.</span></span> <span data-ttu-id="b89b3-159">這也可以使用結構描述來列出，但不需要指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="b89b3-159">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b89b3-160">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b89b3-160">Data Lake Store</span></span>

* <span data-ttu-id="b89b3-161">更新基礎檔案系統 SDK 的版本，以提供更佳的支援來處理伺服器端節流情況。</span><span class="sxs-lookup"><span data-stu-id="b89b3-161">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="b89b3-162">提升套件載入和命令執行的效能 ([#2819 (英文)](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b89b3-162">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="b89b3-163">遺失 access show 的說明。</span><span class="sxs-lookup"><span data-stu-id="b89b3-163">missed help for access show.</span></span> <span data-ttu-id="b89b3-164">將新增此說明。</span><span class="sxs-lookup"><span data-stu-id="b89b3-164">adding it.</span></span> <span data-ttu-id="b89b3-165">([#2743 (英文)](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="b89b3-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="b89b3-166">尋找</span><span class="sxs-lookup"><span data-stu-id="b89b3-166">Find</span></span>

* <span data-ttu-id="b89b3-167">改善搜尋結果，並允許進行搜尋索引版本控制</span><span class="sxs-lookup"><span data-stu-id="b89b3-167">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="b89b3-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b89b3-168">KeyVault</span></span>

* <span data-ttu-id="b89b3-169">BC：`az keyvault certificate download`將 -e 從字串或二進位變更為 PEM 或 DER，來以更佳的方式代表選項</span><span class="sxs-lookup"><span data-stu-id="b89b3-169">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="b89b3-170">BC：從 `keyvault certificate create` 中移除 --expires 和 --not-before，因為服務不支援這些參數。</span><span class="sxs-lookup"><span data-stu-id="b89b3-170">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="b89b3-171">在 `keyvault certificate create` 中新增 --validity 參數，以選擇性地覆寫 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="b89b3-171">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="b89b3-172">修正 `keyvault certificate get-default-policy` 中公開 'expires' 和 'not_before' 但未公開 'validity_in_months' 的問題。</span><span class="sxs-lookup"><span data-stu-id="b89b3-172">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="b89b3-173">用於匯入 pem 和 pfx 的 keyvault 修正 ([#2754 (英文)](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="b89b3-173">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="b89b3-174">實驗室</span><span class="sxs-lookup"><span data-stu-id="b89b3-174">Lab</span></span>

* <span data-ttu-id="b89b3-175">新增適用於實驗室中環境的 create、show、delete 及 list 命令。</span><span class="sxs-lookup"><span data-stu-id="b89b3-175">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="b89b3-176">新增 show 和 list 命令以檢視實驗室中的 ARM 範本。</span><span class="sxs-lookup"><span data-stu-id="b89b3-176">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="b89b3-177">在 `az lab vm list` 中新增 --environment 旗標，以在實驗室中依環境篩選 VM。</span><span class="sxs-lookup"><span data-stu-id="b89b3-177">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="b89b3-178">新增便利命令 `az lab formula export-artifacts` 以匯出實驗室公式內的構件結構。</span><span class="sxs-lookup"><span data-stu-id="b89b3-178">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="b89b3-179">新增命令以管理實驗室內的密碼。</span><span class="sxs-lookup"><span data-stu-id="b89b3-179">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="b89b3-180">監視</span><span class="sxs-lookup"><span data-stu-id="b89b3-180">Monitor</span></span>

* <span data-ttu-id="b89b3-181">Bug 修正：建立 `az alert-rules create` 的 `--actions` 模型以取用 JSON 字串 ([#3009 (英文)](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="b89b3-181">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="b89b3-182">Bug 修正：diagnostic-settings create 不接受來自 show 命令的記錄/計量 ([#2913 (英文)](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="b89b3-182">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="b89b3-183">網路</span><span class="sxs-lookup"><span data-stu-id="b89b3-183">Network</span></span>

* <span data-ttu-id="b89b3-184">新增 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="b89b3-184">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="b89b3-185">新增對 `network watcher packet-capture create` 之 `--filters` 參數的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-185">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="b89b3-186">新增對「應用程式閘道」連線清空的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-186">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="b89b3-187">新增對「應用程式閘道」WAF 規則集組態的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-187">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="b89b3-188">新增對 ExpressRoute 路由篩選和規則的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-188">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="b89b3-189">新增對 TrafficManager 地理路由的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-189">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="b89b3-190">新增對 VPN 連線原則型流量選取器的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-190">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="b89b3-191">新增對 VPN 連線 IPSec 原則的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-191">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="b89b3-192">修正 `vpn-connection create` 搭配使用 `--no-wait` 或 `--validate` 參數時的 Bug。</span><span class="sxs-lookup"><span data-stu-id="b89b3-192">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="b89b3-193">新增對「主動-主動」VNet 閘道的支援</span><span class="sxs-lookup"><span data-stu-id="b89b3-193">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="b89b3-194">從 `network vpn-connection list/show` 命令移除 Null 值。</span><span class="sxs-lookup"><span data-stu-id="b89b3-194">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="b89b3-195">BC：修正 `vpn-connection create` 之輸出中的 Bug</span><span class="sxs-lookup"><span data-stu-id="b89b3-195">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="b89b3-196">修正未正確剖析 'vpn-connection create' 之 '--key-length' 引數的 Bug。</span><span class="sxs-lookup"><span data-stu-id="b89b3-196">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="b89b3-197">修正 `dns zone import` 中未正確匯入記錄的 Bug。</span><span class="sxs-lookup"><span data-stu-id="b89b3-197">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="b89b3-198">修正 `traffic-manager endpoint update` 無法運作的 Bug。</span><span class="sxs-lookup"><span data-stu-id="b89b3-198">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="b89b3-199">新增 'network watcher' 預覽命令。</span><span class="sxs-lookup"><span data-stu-id="b89b3-199">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="b89b3-200">設定檔</span><span class="sxs-lookup"><span data-stu-id="b89b3-200">Profile</span></span>

* <span data-ttu-id="b89b3-201">支援在找不到訂用帳戶時進行登入 ([#2560 (英文)](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="b89b3-201">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="b89b3-202">在 az account set --subscription 中支援短參數名稱 ([#2980 (英文)](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="b89b3-202">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="b89b3-203">Redis</span><span class="sxs-lookup"><span data-stu-id="b89b3-203">Redis</span></span>

* <span data-ttu-id="b89b3-204">新增 update 命令，這也會為 redis 快取新增調整能力</span><span class="sxs-lookup"><span data-stu-id="b89b3-204">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="b89b3-205">取代 'update-settings' 命令。</span><span class="sxs-lookup"><span data-stu-id="b89b3-205">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="b89b3-206">資源</span><span class="sxs-lookup"><span data-stu-id="b89b3-206">Resource</span></span>

* <span data-ttu-id="b89b3-207">新增 managedapp 和 managedapp definition 命令 ([#2985 (英文)](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="b89b3-207">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="b89b3-208">支援 'provider operation' 命令 ([#2908 (英文)](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="b89b3-208">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="b89b3-209">支援一般 resource create ([#2606 (英文)](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="b89b3-209">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="b89b3-210">修正資源剖析和 api 版本查詢。</span><span class="sxs-lookup"><span data-stu-id="b89b3-210">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="b89b3-211">([#2781 (英文)](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="b89b3-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="b89b3-212">新增 az lock update 的文件。</span><span class="sxs-lookup"><span data-stu-id="b89b3-212">Add docs for az lock update.</span></span> <span data-ttu-id="b89b3-213">([#2702 (英文)](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="b89b3-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="b89b3-214">如果您嘗試列出不存在之群組的資源，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b89b3-214">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="b89b3-215">([#2769 (英文)](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="b89b3-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="b89b3-216">[計算] 修正 VMSS 和 VM 可用性設定組更新的相關問題。</span><span class="sxs-lookup"><span data-stu-id="b89b3-216">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="b89b3-217">([#2773 (英文)](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="b89b3-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="b89b3-218">修正 parent-resource-path 為 None 時的 lock create 和 delete ([#2742 (英文)](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="b89b3-218">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="b89b3-219">角色</span><span class="sxs-lookup"><span data-stu-id="b89b3-219">Role</span></span>

* <span data-ttu-id="b89b3-220">create-for-rbac：確保 SP 的結束日期不會超過憑證的到期日 ([#2989 (英文)](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="b89b3-220">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="b89b3-221">RBAC：新增對 'ad group' 的完整支援 ([#2016 (英文)](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="b89b3-221">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="b89b3-222">角色：修正 role definition update 上的問題 ([#2745 (英文)](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="b89b3-222">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="b89b3-223">create-for-rbac：確保系統會挑選使用者提供的密碼</span><span class="sxs-lookup"><span data-stu-id="b89b3-223">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="b89b3-224">SQL</span><span class="sxs-lookup"><span data-stu-id="b89b3-224">SQL</span></span>

* <span data-ttu-id="b89b3-225">新增 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="b89b3-225">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="b89b3-226">SQL - 能夠直接連接到資源提供者 ([#2832 (英文)](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="b89b3-226">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="b89b3-227">儲存體</span><span class="sxs-lookup"><span data-stu-id="b89b3-227">Storage</span></span>

* <span data-ttu-id="b89b3-228">`storage account create` 之資源群組位置的預設位置。</span><span class="sxs-lookup"><span data-stu-id="b89b3-228">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="b89b3-229">新增對遞增 blob 複製的支援</span><span class="sxs-lookup"><span data-stu-id="b89b3-229">Add support for incremental blob copy</span></span>
* <span data-ttu-id="b89b3-230">新增對大型區塊 blob 上傳的支援</span><span class="sxs-lookup"><span data-stu-id="b89b3-230">Add support for large block blob upload</span></span>
* <span data-ttu-id="b89b3-231">當要上傳的檔案大於 200 GB 時，將區塊大小變更為 100 MB</span><span class="sxs-lookup"><span data-stu-id="b89b3-231">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="b89b3-232">VM</span><span class="sxs-lookup"><span data-stu-id="b89b3-232">VM</span></span>

* <span data-ttu-id="b89b3-233">avail-set：將 UD&FD 網域計數設定為選用</span><span class="sxs-lookup"><span data-stu-id="b89b3-233">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="b89b3-234">注意：主權雲端中的 VM 命令。請避免使用受管理磁碟相關的功能，包括下列功能：</span><span class="sxs-lookup"><span data-stu-id="b89b3-234">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="b89b3-235">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="b89b3-235">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="b89b3-236">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="b89b3-236">az vm/vmss disk</span></span>
  3. <span data-ttu-id="b89b3-237">在 "az vm/vmss create" 內，請使用 "—use-unmanaged-disk" 來避免使用受管理的磁碟。其他命令應該可運作</span><span class="sxs-lookup"><span data-stu-id="b89b3-237">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="b89b3-238">vm/vmss：改進產生 SSH 金鑰組時的警告文字</span><span class="sxs-lookup"><span data-stu-id="b89b3-238">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="b89b3-239">vm/vmss：支援從需要方案資訊的市場映像進行建立 ([#1209 (英文)](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="b89b3-239">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="b89b3-240">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b89b3-240">April 3, 2017</span></span>

<span data-ttu-id="b89b3-241">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="b89b3-241">Version 2.0.2</span></span>

<span data-ttu-id="b89b3-242">在這一版中，我們發行了 ACR、Batch、KeyVault 和 SQL 元件。</span><span class="sxs-lookup"><span data-stu-id="b89b3-242">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="b89b3-243">核心</span><span class="sxs-lookup"><span data-stu-id="b89b3-243">Core</span></span>

* <span data-ttu-id="b89b3-244">將 ACR、實驗室、監視及尋找模組新增至預設清單。</span><span class="sxs-lookup"><span data-stu-id="b89b3-244">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="b89b3-245">Login︰略過錯誤的租用戶 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="b89b3-245">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="b89b3-246">Login︰將預設訂用帳戶設定為具有「已啟用」狀態的訂用帳戶 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="b89b3-246">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="b89b3-247">將 wait 命令和 --no-wait 支援新增至多個命令 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b89b3-247">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b89b3-248">Core︰支援使用憑證的服務主體登入 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="b89b3-248">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="b89b3-249">新增遺漏範本參數的提示。</span><span class="sxs-lookup"><span data-stu-id="b89b3-249">Add prompting for missing template parameters.</span></span> <span data-ttu-id="b89b3-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="b89b3-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="b89b3-251">支援設定諸如預設資源群組、預設 web、預設 VM 等常見引數的預設值</span><span class="sxs-lookup"><span data-stu-id="b89b3-251">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="b89b3-252">支援登入特定的租用戶</span><span class="sxs-lookup"><span data-stu-id="b89b3-252">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="b89b3-253">ACS</span><span class="sxs-lookup"><span data-stu-id="b89b3-253">ACS</span></span>

* [<span data-ttu-id="b89b3-254">ACS] 新增設定預設 ACS 叢集的支援 ([#2554</span><span class="sxs-lookup"><span data-stu-id="b89b3-254">ACS] Adding support for configuring a default ACS cluster ([#2554</span></span>](https://github.com/Azure/azure-cli/pull/2554))
* <span data-ttu-id="b89b3-255">新增 SSH 金鑰密碼提示的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-255">Add support for ssh key password prompting.</span></span> <span data-ttu-id="b89b3-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="b89b3-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="b89b3-257">新增 Windows 叢集的支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-257">Add support for windows clusters.</span></span> <span data-ttu-id="b89b3-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="b89b3-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="b89b3-259">將角色從擁有者切換為參與者。</span><span class="sxs-lookup"><span data-stu-id="b89b3-259">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="b89b3-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="b89b3-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="b89b3-261">AppService</span><span class="sxs-lookup"><span data-stu-id="b89b3-261">AppService</span></span>

* <span data-ttu-id="b89b3-262">appservice︰取得用於 DNS A 記錄之外部 IP 位址的支援 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="b89b3-262">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="b89b3-263">appservice︰支援繫結萬用字元憑證 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="b89b3-263">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="b89b3-264">appservice︰支援列出發行設定檔 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="b89b3-264">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="b89b3-265">AppService - 設定之後觸發原始檔控制同步處理 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="b89b3-265">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="b89b3-266">DataLake</span><span class="sxs-lookup"><span data-stu-id="b89b3-266">DataLake</span></span>

* <span data-ttu-id="b89b3-267">Data Lake Analytics 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="b89b3-267">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="b89b3-268">Data Lake Store 模組的初始版本。</span><span class="sxs-lookup"><span data-stu-id="b89b3-268">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="b89b3-269">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="b89b3-269">DocuemntDB</span></span>

* <span data-ttu-id="b89b3-270">DocumentDB︰新增列出連接字串的支援 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="b89b3-270">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="b89b3-271">VM</span><span class="sxs-lookup"><span data-stu-id="b89b3-271">VM</span></span>

* [<span data-ttu-id="b89b3-272">Compute] 將 AppGateway 支援新增至虛擬機器擴展集建立 ([#2570</span><span class="sxs-lookup"><span data-stu-id="b89b3-272">Compute] Add AppGateway support to virtual machine scale set create ([#2570</span></span>](https://github.com/Azure/azure-cli/pull/2570))
* [<span data-ttu-id="b89b3-273">VM/VMSS] 改良的磁碟快取支援 ([#2522</span><span class="sxs-lookup"><span data-stu-id="b89b3-273">VM/VMSS] Improved disk caching support ([#2522</span></span>](https://github.com/Azure/azure-cli/pull/2522))
* <span data-ttu-id="b89b3-274">VM/VMSS︰併入入口網站所使用的認證驗證邏輯 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="b89b3-274">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="b89b3-275">新增 wait 命令和 --no-wait 支援 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b89b3-275">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b89b3-276">虛擬機器擴展集︰支援 * 列出跨 VM 的執行個體檢視 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="b89b3-276">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="b89b3-277">新增 VM 和虛擬機器擴展集的 --祕密 ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="b89b3-277">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="b89b3-278">可使用特殊的 VHD 來建立 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="b89b3-278">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="b89b3-279">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b89b3-279">February 27, 2017</span></span>

<span data-ttu-id="b89b3-280">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b89b3-280">Version 2.0.0</span></span>

<span data-ttu-id="b89b3-281">此版本的 Azure CLI 2.0 是第一個「正式運作」版本。</span><span class="sxs-lookup"><span data-stu-id="b89b3-281">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="b89b3-282">正式運作適用於下列的命令模組︰</span><span class="sxs-lookup"><span data-stu-id="b89b3-282">General availability applies to these command modules:</span></span>
- <span data-ttu-id="b89b3-283">Container Service (ACS)</span><span class="sxs-lookup"><span data-stu-id="b89b3-283">Container Service (acs)</span></span>
- <span data-ttu-id="b89b3-284">計算 (包含 Resource Manager、VM、虛擬機器擴展集、受控磁碟)</span><span class="sxs-lookup"><span data-stu-id="b89b3-284">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="b89b3-285">網路功能</span><span class="sxs-lookup"><span data-stu-id="b89b3-285">Networking</span></span>
- <span data-ttu-id="b89b3-286">儲存體</span><span class="sxs-lookup"><span data-stu-id="b89b3-286">Storage</span></span>

<span data-ttu-id="b89b3-287">這些命令模組可用在生產環境中，且受標準 Microsoft SLA 支援。</span><span class="sxs-lookup"><span data-stu-id="b89b3-287">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="b89b3-288">您可以向 Microsoft 支援服務直接開啟問題，或在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)開啟問題。</span><span class="sxs-lookup"><span data-stu-id="b89b3-288">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="b89b3-289">您可以在 [StackOverflow 上使用 azure-cli 標記](http://stackoverflow.com/questions/tagged/azure-cli)提出問題，或請連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="b89b3-289">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
<span data-ttu-id="b89b3-290">您可以從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="b89b3-290">You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="b89b3-291">這些模組中的命令很穩定，且不應該變更此版 Azure CLI 之未來版本的語法。</span><span class="sxs-lookup"><span data-stu-id="b89b3-291">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="b89b3-292">若要確認的 CLI 的版本，請使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="b89b3-292">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="b89b3-293">輸出會列出 CLI 本身的版本 (此版本中為 2.0.0)、個別的命令模組，以及您所使用的 Python 和 GCC 版本。</span><span class="sxs-lookup"><span data-stu-id="b89b3-293">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="b89b3-294">些命令模組會有 "b*n*" 或 "rc*n*" 後置詞。</span><span class="sxs-lookup"><span data-stu-id="b89b3-294">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="b89b3-295">這些命令模組仍處於預覽狀態，且未來會正式運作。</span><span class="sxs-lookup"><span data-stu-id="b89b3-295">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="b89b3-296">我們也有 CLI 的夜間預覽組建。</span><span class="sxs-lookup"><span data-stu-id="b89b3-296">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="b89b3-297">如需詳細資訊，請參閱[取得夜間組建](https://github.com/Azure/azure-cli#nightly-builds)中的指示，以及[開發人員設定和參與程式碼](https://github.com/Azure/azure-cli#developer-setup)中的指示。</span><span class="sxs-lookup"><span data-stu-id="b89b3-297">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="b89b3-298">您可以透過下列方式來報告夜間預覽組建的問題︰</span><span class="sxs-lookup"><span data-stu-id="b89b3-298">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="b89b3-299">在我們的 [GitHub 問題清單](https://github.com/azure/azure-cli/issues/)中報告問題</span><span class="sxs-lookup"><span data-stu-id="b89b3-299">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="b89b3-300">連絡產品小組：[azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="b89b3-300">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="b89b3-301">從包含 `az feedback` 命令的命令列提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="b89b3-301">Provide feedback from the command line with the `az feedback` command.</span></span>

