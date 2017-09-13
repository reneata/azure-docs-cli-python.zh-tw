---
title: "開始使用 Azure CLI 2.0"
description: "開始使用 Linux、Mac 或 Windows 上的 Azure CLI 2.0。"
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
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 5d6d7abb34fa2be571a9a49f0f84380538592807
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="48fa7-104">開始使用 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa7-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="48fa7-105">Azure CLI 2.0 是管理 Azure 資源的 Azure 新命令列體驗。</span><span class="sxs-lookup"><span data-stu-id="48fa7-105">The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.</span></span>
<span data-ttu-id="48fa7-106">您可以透過 [Azure Cloud Shell](/azure/cloud-shell/overview) 在瀏覽器中使用，或者在 macOS、Linux 和 Windows 中[安裝](install-azure-cli.md)並從命令列中執行。</span><span class="sxs-lookup"><span data-stu-id="48fa7-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="48fa7-107">Azure CLI 2.0 已針對從命令列管理 Azure 資源進行最佳化，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。</span><span class="sxs-lookup"><span data-stu-id="48fa7-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span>
<span data-ttu-id="48fa7-108">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="48fa7-108">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

<span data-ttu-id="48fa7-109">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-109">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

## <a name="connect"></a><span data-ttu-id="48fa7-110">連線</span><span class="sxs-lookup"><span data-stu-id="48fa7-110">Connect</span></span>

<span data-ttu-id="48fa7-111">若要開始使用，最簡單的方式就是[啟動 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-111">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="48fa7-112">從 Azure 入口網站的頂端導覽啟動 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="48fa7-112">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 圖示](media/get-started-with-azure-cli/shell-icon.png)

2. <span data-ttu-id="48fa7-114">選擇您想使用的訂用帳戶，並建立儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="48fa7-114">Choose the subscription you want to use and create a storage account.</span></span>

   ![建立儲存體帳戶](media/get-started-with-azure-cli/storage-prompt.png)

<span data-ttu-id="48fa7-116">您也可以[安裝](install-azure-cli.md) CLI，並從本機命令列執行。</span><span class="sxs-lookup"><span data-stu-id="48fa7-116">You can also [install](install-azure-cli.md) the CLI and run it locally from the command line.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="48fa7-117">建立資源群組</span><span class="sxs-lookup"><span data-stu-id="48fa7-117">Create a Resource Group</span></span>

<span data-ttu-id="48fa7-118">一切都已準備就緒，接下來我們要使用 Azure CLI 在 Azure 中建立資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-118">Now that we've got everything set up, let's use the Azure CLI to create resources within Azure.</span></span>

<span data-ttu-id="48fa7-119">首先，建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="48fa7-119">First, create a Resource Group.</span></span>  <span data-ttu-id="48fa7-120">針對您想要以邏輯方式進行分組的多個資源，Azure 中的「資源群組」提供一個讓您管理這些資源的方式。</span><span class="sxs-lookup"><span data-stu-id="48fa7-120">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group.</span></span>  <span data-ttu-id="48fa7-121">例如，您可以為應用程式或專案建立資源群組，並在該群組中新增虛擬機器、資料庫和 CDN 服務。</span><span class="sxs-lookup"><span data-stu-id="48fa7-121">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="48fa7-122">讓我們建立一個名為「MyResourceGroup」的資源群組，位置則定在 Azure 的 westus2 區域。</span><span class="sxs-lookup"><span data-stu-id="48fa7-122">Let's create a resource group named "MyResourceGroup" in the *westus2* region of Azure.</span></span>  <span data-ttu-id="48fa7-123">若要這麼做，請輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="48fa7-123">To do so type the following command:</span></span>

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

<span data-ttu-id="48fa7-124">建立資源群組之後，`az group create` 命令會輸出數個新建立資源的屬性︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-124">Once the resource group has been created, the `az group create` command outputs several properties of the newly created resource:</span></span>

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="48fa7-125">建立 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="48fa7-125">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="48fa7-126">我們已擁有資源群組，接著我們要在其中建立 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="48fa7-126">Now that we have our resource group, let's create a Linux VM within it.</span></span>

<span data-ttu-id="48fa7-127">您可以使用下列命令搭配常用的 UbuntuLTS 映像，建立一個具有 10 GB 和 20 GB 兩個連結儲存體磁碟的 Linux VM︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-127">You can create a Linux VM using the popular UbuntuLTS image, with two attached storage disks of 10 GB and 20 GB, with the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

<span data-ttu-id="48fa7-128">當您執行上述命令時，Azure CLI 2.0 會尋找儲存在 ~/.ssh 目錄下的 SSH 金鑰組。</span><span class="sxs-lookup"><span data-stu-id="48fa7-128">When you run the preceding command, the Azure CLI 2.0 looks for an SSH key pair stored under your ~/.ssh directory.</span></span>  <span data-ttu-id="48fa7-129">如果您還沒有儲存在該處的 SSH 金鑰組，可以要求 Azure CLI 為您自動建立一個，方法為傳遞 --generate-ssh-keys 參數︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-129">If you don't already have an SSH key pair stored there, you can ask the Azure CLI to automatically create one for you by passing the --generate-ssh-keys parameter:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

<span data-ttu-id="48fa7-130">在 VM 完全建立好並可供存取及使用之後，`az vm create` 命令會傳回輸出。</span><span class="sxs-lookup"><span data-stu-id="48fa7-130">The `az vm create` command returns output once the VM has been fully created and is ready to be accessed and used.</span></span> <span data-ttu-id="48fa7-131">輸出會包含新建立 VM 的數個屬性，包括其公用 IP 位址︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-131">The output includes several properties of the newly created VM including its public IP address:</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="48fa7-132">VM 已經建立好，因此您可以搭配使用 **SSH** 與您所建立之 VM 的公用 IP 位址，來登入新的 Linux VM︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-132">Now that the VM has been created, you can log on to your new Linux VM using **SSH** with the public IP address of the VM you created:</span></span>

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a><span data-ttu-id="48fa7-133">建立 Windows Server 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="48fa7-133">Create a Windows Server Virtual Machine</span></span>

<span data-ttu-id="48fa7-134">現在讓我們使用 `az vm create` 命令來建立以 Windows Server 2016 Datacenter 為基礎 VM，並將它新增至用於我們 Linux VM 的相同 "MyResourceGroup" 資源群組。</span><span class="sxs-lookup"><span data-stu-id="48fa7-134">Let's now create a Windows Server 2016 Datacenter-based VM using the `az vm create` command and add it to the same "MyResourceGroup" resource group that we used for our Linux VM.</span></span>  <span data-ttu-id="48fa7-135">如同 Linux VM 範例，我們也會使用 `--data-disk-sizes-gb` 參數來連結兩個儲存體磁碟。</span><span class="sxs-lookup"><span data-stu-id="48fa7-135">Like the Linux VM example, we'll also attach two storage disks using the `--data-disk-sizes-gb` parameter.</span></span>

<span data-ttu-id="48fa7-136">Azure 要求您避免使用輕易猜到的使用者名稱/密碼。</span><span class="sxs-lookup"><span data-stu-id="48fa7-136">Azure requires that you avoid using easily guessed usernames/passwords.</span></span> <span data-ttu-id="48fa7-137">關於可使用哪些字元以及使用者名稱和密碼的最小長度，皆有特定的規則。</span><span class="sxs-lookup"><span data-stu-id="48fa7-137">There are specific rules for what characters can be used as well as the minimum length of both username and password.</span></span>  

> [!NOTE]
> <span data-ttu-id="48fa7-138">執行此命令時，系統會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="48fa7-138">You will be prompted to enter your username and password when running this command.</span></span>

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

<span data-ttu-id="48fa7-139">在 VM 完全建立好並可供存取及使用之後，`az vm create` 命令會輸出結果。</span><span class="sxs-lookup"><span data-stu-id="48fa7-139">The `az vm create` command output results once the VM has been fully created and is ready to be accessed and used.</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="48fa7-140">現在，使用遠端桌面和 VM 的公用 IP 位址來登入新建立的 Windows Server VM (會從 `az vm create` 的輸出中傳回)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-140">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM (which is returned in the output from `az vm create`).</span></span>  
<span data-ttu-id="48fa7-141">如果您是使用以 Windows 為基礎的系統，可以從命令列利用 `mstsc` 命令來執行此作業︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-141">If you are on a Windows-based system, you can do this from the command line using the `mstsc` command:</span></span>

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="48fa7-142">提供您在建立 VM 時所使用的相同使用者名稱/密碼組合來進行登入。</span><span class="sxs-lookup"><span data-stu-id="48fa7-142">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="48fa7-143">在 Azure 中建立其他資源</span><span class="sxs-lookup"><span data-stu-id="48fa7-143">Creating other resources in Azure</span></span>

<span data-ttu-id="48fa7-144">我們已逐步瀏覽過如何建立資源群組、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="48fa7-144">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="48fa7-145">您也可以建立其他許多類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-145">You can create many other types of Azure resources as well.</span></span>  

<span data-ttu-id="48fa7-146">所有新的資源都會使用一致的 `az <resource type name> create` 命名模式來建立。</span><span class="sxs-lookup"><span data-stu-id="48fa7-146">All new resources are created using a consistent `az <resource type name> create` naming pattern.</span></span>  <span data-ttu-id="48fa7-147">例如，若要建立 Azure 網路負載平衡器，然後與我們新建立的 VM 相關聯，我們可以使用下列 create 命令︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-147">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

<span data-ttu-id="48fa7-148">我們也可以使用下列 create 命令，為我們的基礎結構建立新的私人虛擬網路 (此網路在 Azure 中通常稱為 "VNet")︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-148">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following create command:</span></span>

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

<span data-ttu-id="48fa7-149">Azure 和 Azure CLI 的功能之所以強大，是因為它們不只能用來取得以雲端為基礎的基礎結構，還能用來建立受管理的平台服務。</span><span class="sxs-lookup"><span data-stu-id="48fa7-149">What makes Azure and the Azure CLI powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span>  <span data-ttu-id="48fa7-150">受管理的平台服務也可以結合基礎結構來建置更強大的解決方案。</span><span class="sxs-lookup"><span data-stu-id="48fa7-150">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="48fa7-151">例如，您可以使用 Azure CLI 來建立 Azure AppService。</span><span class="sxs-lookup"><span data-stu-id="48fa7-151">For example, you can use the Azure CLI to create an Azure AppService.</span></span>  <span data-ttu-id="48fa7-152">Azure AppService 是一種受管理的平台服務，它可讓您裝載 Web Apps，而不必擔心基礎結構的問題。</span><span class="sxs-lookup"><span data-stu-id="48fa7-152">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span>  <span data-ttu-id="48fa7-153">在建立 Azure AppService 之後，您可以使用下列 create 命令在 AppService 內建立兩個新的 Azure Web Apps︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-153">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following create commands:</span></span>

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

<span data-ttu-id="48fa7-154">一旦您了解 `az <resource type name> create` 模式的基本概念後，建立任何項目都會變得很輕鬆。</span><span class="sxs-lookup"><span data-stu-id="48fa7-154">Once you understand the basics of the `az <resource type name> create` pattern, it becomes easy to create anything.</span></span> <span data-ttu-id="48fa7-155">以下是一些熱門的 Azure 資源類型，以及用來建立它們的對應 Azure CLI create 命令︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-155">Following are some popular Azure resource types and the corresponding Azure CLI create commands to create them:</span></span>

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

<span data-ttu-id="48fa7-156">若要深入了解您可以傳遞給每個先前命令的其他資源特定參數，以及您可以建立的資源類型，請瀏覽[參考文件](/cli/azure)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-156">Visit the [Reference documentation](/cli/azure) to learn more about the additional resource-specific parameters that you can pass to each of the preceding commands and the resource types you can create.</span></span> 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a><span data-ttu-id="48fa7-157">實用秘訣︰使用 --no-wait 將建立作業最佳化</span><span class="sxs-lookup"><span data-stu-id="48fa7-157">Useful tip: Optimizing create operations using --no-wait</span></span>

<span data-ttu-id="48fa7-158">依預設，當您使用 Azure CLI 2.0 建立資源時，`az <resource type name> create` 命令會等候到資源已建立且可供使用為止。</span><span class="sxs-lookup"><span data-stu-id="48fa7-158">By default when you create resources using the Azure CLI 2.0, the `az <resource type name> create` command waits until the resource has been created and is ready for you to use.</span></span>  <span data-ttu-id="48fa7-159">例如，如果您是建立 VM，依預設不會傳回 `az vm create` 命令，直到 VM 建立且已就緒可供您進行 SSH 或 RDP 為止。</span><span class="sxs-lookup"><span data-stu-id="48fa7-159">For example, if you create a VM, the `az vm create` command will, by default, not return until the VM is created and is ready for you to SSH or RDP into it.</span></span>

<span data-ttu-id="48fa7-160">我們使用這種方法的原因是，它可讓您更輕鬆地撰寫自動化指令碼，當中包含具有相依性的多個步驟 (且在繼續執行之前需已順利完成先前的工作)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-160">We use this approach because it makes it easier to write automation scripts that contain multiple steps with dependencies (and need a prior task to have completed successfully before continuing).</span></span>

<span data-ttu-id="48fa7-161">如果您在繼續之前不需要等候資源建立，可以使用 `no-wait` 選項，在背景中啟動建立動作。</span><span class="sxs-lookup"><span data-stu-id="48fa7-161">If you do not need to wait on creation of a resource before continuing, you can use the `no-wait` option to start a create action in the background.</span></span> <span data-ttu-id="48fa7-162">您可以針對其他命令繼續使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="48fa7-162">You can continue using the CLI for other commands.</span></span>

<span data-ttu-id="48fa7-163">例如，下列的 `az vm create` 使用方式會啟動 VM 部署，然後更快速地傳回 (且在 VM 完全啟動之前)︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-163">For example, the following usage of the `az vm create` starts a VM deployment and then return much more quickly (and before the VM has fully booted):</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

<span data-ttu-id="48fa7-164">使用 `--no-wait` 方法可以幫助您將自動化指令碼的效能大幅最佳化。</span><span class="sxs-lookup"><span data-stu-id="48fa7-164">Using the `--no-wait` approach can help you optimize the performance of your automation scripts considerably.</span></span>

## <a name="listing-resources-and-formatting-output"></a><span data-ttu-id="48fa7-165">列出資源並設定輸出格式</span><span class="sxs-lookup"><span data-stu-id="48fa7-165">Listing resources and formatting output</span></span>

<span data-ttu-id="48fa7-166">您可以使用 Azure CLI 內的 `list` 命令，來尋找並列出 Azure 中執行的資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-166">You can use the `list` command within the Azure CLI to find and list the resources running in Azure.</span></span> 

<span data-ttu-id="48fa7-167">例如，您可以利用 create 命令，使用一個在所有資源類型中皆一致的通用 `az <resource type name> list` 命名模式，將使用 Azure CLI 2.0 的資源列出。</span><span class="sxs-lookup"><span data-stu-id="48fa7-167">Like with the create command, you can list resources using the Azure CLI 2.0 using a common `az <resource type name> list` naming pattern that is consistent across all resource types.</span></span>  <span data-ttu-id="48fa7-168">有各種不同的輸出格式和查詢選項，可讓您以想要查看這些資源的方式，來篩選和排序資源的清單。</span><span class="sxs-lookup"><span data-stu-id="48fa7-168">There are various output formats and query options available to filter and sort the list of resources in the way you prefer to see them.</span></span>

<span data-ttu-id="48fa7-169">例如，`az vm list` 會顯示您擁有的所有 VM 清單。</span><span class="sxs-lookup"><span data-stu-id="48fa7-169">For example, `az vm list` shows the list of all VMs you have.</span></span>   

```azurecli-interactive
az vm list 
```
<span data-ttu-id="48fa7-170">依預設，傳回的值為 JSON 格式 (為了保持簡潔，只顯示部分輸出)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-170">The values returned are by default in JSON (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...   
]
```

<span data-ttu-id="48fa7-171">您可以使用 `--output` 選項，選擇性地修改輸出格式。</span><span class="sxs-lookup"><span data-stu-id="48fa7-171">You can optionally modify the output format using the `--output` option.</span></span>  <span data-ttu-id="48fa7-172">使用易於閱讀的資料表格式選項，執行 `az vm list` 命令，以檢視稍早建立的 Linux 和 Windows Server VM 以及最常見的 VM 屬性︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-172">Run the `az vm list` command to see both the Linux and Windows Server VMs created earlier, along with the most common properties of a VM, using the easy to read *table* format option:</span></span>

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="48fa7-173">TSV 輸出選項可用來取得沒有標頭、以文字為基礎的定位字元分隔格式。</span><span class="sxs-lookup"><span data-stu-id="48fa7-173">The *tsv* output option can be used to get a text-based, tab-separated format without any headers.</span></span>  <span data-ttu-id="48fa7-174">當您要將輸出輸送到另一個以文字為基礎的工具 (例如 grep) 時，此格式會很有用。</span><span class="sxs-lookup"><span data-stu-id="48fa7-174">This format is useful when you want to pipe the output into another text-based tool like grep.</span></span> 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
<span data-ttu-id="48fa7-175">請瀏覽[輸出格式](format-output-azure-cli.md)文件，進一步了解列出資源及設定輸出格式的其他方式。</span><span class="sxs-lookup"><span data-stu-id="48fa7-175">Visit the [output formats](format-output-azure-cli.md) article to learn more about the additional ways to list resources and format the output.</span></span>

## <a name="querying-resources-and-shaping-outputs"></a><span data-ttu-id="48fa7-176">查詢資源與成形輸出</span><span class="sxs-lookup"><span data-stu-id="48fa7-176">Querying resources and shaping outputs</span></span>

<span data-ttu-id="48fa7-177">通常您會想要能夠只查詢符合特定條件的資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-177">Often you want to be able to query for only those resources that meet a specific condition.</span></span>  

<span data-ttu-id="48fa7-178">`list` 命令有內建支援，可輕鬆地依資源群組名稱篩選資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-178">The `list` command has built-in support that makes it easy to filter resources by Resource Group name.</span></span>  <span data-ttu-id="48fa7-179">例如，您可以將 `--ResourceGroup` 或 `-g` 參數傳遞至 `list` 命令，只擷取特定資源群組內的這些資源︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-179">For example, you can pass either a `--ResourceGroup` or `-g` parameter to a `list` command to only retrieve those resources within a specific resource group:</span></span>


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="48fa7-180">如需更強大的查詢支援，您可以使用 `--query` 參數，在任何 `az` 命令的結果執行 JMESPath 查詢。</span><span class="sxs-lookup"><span data-stu-id="48fa7-180">For even more powerful querying support, you can use the `--query` parameter to execute a JMESPath query on the results of *any* `az` command.</span></span>  <span data-ttu-id="48fa7-181">JMESPath 查詢可用於篩選以及成形任何傳回結果的輸出。</span><span class="sxs-lookup"><span data-stu-id="48fa7-181">JMESPath queries can be used both to filter as well as shape the output of any returned result.</span></span>

<span data-ttu-id="48fa7-182">例如，執行下列命令，在包含 "My" 字母的任何資源群組內查詢任何 VM 資源：</span><span class="sxs-lookup"><span data-stu-id="48fa7-182">For example, execute the following command to query for any VM resource within any resource group that contains the letters "My":</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="48fa7-183">然後我們還可以選擇進一步精簡輸出，方法為使用 JMESPath 查詢的成形能力來輸出不同的值。</span><span class="sxs-lookup"><span data-stu-id="48fa7-183">We could then choose to further refine the output by using the shaping capability of JMESPath queries to output different values as well.</span></span>  <span data-ttu-id="48fa7-184">例如，下列命令所擷取的 OS 磁碟類型，VM 會用來決定作業系統是以 Linux 還是 Windows 為基礎︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-184">For example, the following command retrieves the type of OS disk the VM is using to determine whether the OS is Linux or Windows based:</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

<span data-ttu-id="48fa7-185">Azure CLI 中的 JMESPath 支援很強大。</span><span class="sxs-lookup"><span data-stu-id="48fa7-185">The JMESPath support in Azure CLI is powerful.</span></span>  <span data-ttu-id="48fa7-186">在我們的[查詢](query-azure-cli.md)文件中深入了解如何它的使用方式。</span><span class="sxs-lookup"><span data-stu-id="48fa7-186">Learn more about how to use it in our [query](query-azure-cli.md) article.</span></span>

## <a name="deleting-resources"></a><span data-ttu-id="48fa7-187">刪除資源</span><span class="sxs-lookup"><span data-stu-id="48fa7-187">Deleting resources</span></span>

<span data-ttu-id="48fa7-188">您可以使用 Azure CLI 內的 `delete` 命令來刪除您不再需要的資源。</span><span class="sxs-lookup"><span data-stu-id="48fa7-188">You can use the `delete` command within Azure CLI to delete the resources you no longer need.</span></span> <span data-ttu-id="48fa7-189">您可以搭配使用 `delete` 命令與任何資源，就像您使用 `create` 命令一樣。</span><span class="sxs-lookup"><span data-stu-id="48fa7-189">You can use the `delete` command with any resource just like you can with the `create` command.</span></span>

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

<span data-ttu-id="48fa7-190">依預設，CLI 會提示您確認刪除。</span><span class="sxs-lookup"><span data-stu-id="48fa7-190">By default the CLI prompts to confirm deletion.</span></span>  <span data-ttu-id="48fa7-191">您可以隱藏這個自動化指令碼的提示。</span><span class="sxs-lookup"><span data-stu-id="48fa7-191">You can suppress this prompt for automated scripts.</span></span>

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

<span data-ttu-id="48fa7-192">您也可以使用 `delete` 命令，一次將許多資源刪除。</span><span class="sxs-lookup"><span data-stu-id="48fa7-192">You can also use the `delete` command to delete many resources at a time.</span></span> <span data-ttu-id="48fa7-193">例如，下列命令會將資源群組 "MyResourceGroup" 中的所有資源刪除，之前我們將這個群組用於此快速入門教學課程中的所有範例。</span><span class="sxs-lookup"><span data-stu-id="48fa7-193">For example, the following command deletes all the resources in the "MyResourceGroup" resource group that we've used for all the samples in this Get Started tutorial.</span></span>

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a><span data-ttu-id="48fa7-194">取得範例</span><span class="sxs-lookup"><span data-stu-id="48fa7-194">Get samples</span></span>

<span data-ttu-id="48fa7-195">若要深入了解如何使用 Azure CLI，請參閱我們針對 [Linux VM](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) 和 [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) 所提供的最常見指令碼。</span><span class="sxs-lookup"><span data-stu-id="48fa7-195">To learn more about ways to use the Azure CLI, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Web apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), and [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).</span></span>

## <a name="read-the-api-reference-docs"></a><span data-ttu-id="48fa7-196">閱讀 API 參考文件</span><span class="sxs-lookup"><span data-stu-id="48fa7-196">Read the API reference docs</span></span>

[<span data-ttu-id="48fa7-197">API 參考</span><span class="sxs-lookup"><span data-stu-id="48fa7-197">API reference</span></span>](/cli/azure)

## <a name="get-help"></a><span data-ttu-id="48fa7-198">取得說明</span><span class="sxs-lookup"><span data-stu-id="48fa7-198">Get help</span></span>

<span data-ttu-id="48fa7-199">Azure CLI 有內建說明文件，用來比對您可以從命令列執行的 web 文件︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-199">The Azure CLI has built-in help documentation, which matches our web documentation that you can run from the command line:</span></span>

```azurecli-interactive
az [command-group [command]] -h
```

<span data-ttu-id="48fa7-200">例如，若要查看 VM 可使用哪些命令和子群組，請使用︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-200">For example, to see what commands and subgroups are available for VMs, use:</span></span>

```azurecli-interactive
az vm -h
```

<span data-ttu-id="48fa7-201">若要取得建立 VM 的命令說明，請使用︰</span><span class="sxs-lookup"><span data-stu-id="48fa7-201">To get help with the command to create a VM, use:</span></span>

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a><span data-ttu-id="48fa7-202">從 Azure CLI 1.0 進行切換</span><span class="sxs-lookup"><span data-stu-id="48fa7-202">Switch from Azure CLI 1.0</span></span>

<span data-ttu-id="48fa7-203">如果您已經知道如何使用 Azure CLI 1.0 (azure.js)，會發現命令並不完全相同之處。</span><span class="sxs-lookup"><span data-stu-id="48fa7-203">If you already know how to use Azure CLI 1.0 (azure.js), you'll notice places where the commands aren't quite the same.</span></span>
<span data-ttu-id="48fa7-204">有時要執行工作的命令會有顯著的差異。</span><span class="sxs-lookup"><span data-stu-id="48fa7-204">Sometimes the commands to perform a task are significantly different.</span></span>
<span data-ttu-id="48fa7-205">為了協助您從 Azure CLI 1.0 切換至 Azure CLI 2.0，我們已經開始進行這個[命令對應](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst)。</span><span class="sxs-lookup"><span data-stu-id="48fa7-205">To help you make the switch from Azure CLI 1.0 to Azure CLI 2.0, we've started this [command mapping](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).</span></span>

## <a name="send-us-your-feedback"></a><span data-ttu-id="48fa7-206">將您的意見反應傳給我們</span><span class="sxs-lookup"><span data-stu-id="48fa7-206">Send us your feedback</span></span>

```azurecli-interactive
az feedback
```
