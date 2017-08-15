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
ms.openlocfilehash: 36a08835b9c4f6e71c5ddadbce8ba946c52a1e9b
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2017
---
# <a name="azure-cli-20"></a><span data-ttu-id="15623-104">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="15623-104">Azure CLI 2.0</span></span>

<span data-ttu-id="15623-105">Azure CLI 2.0 是管理 Azure 資源的 Azure 新命令列體驗。</span><span class="sxs-lookup"><span data-stu-id="15623-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="15623-106">您可以透過 [Azure Cloud Shell](/azure/cloud-shell/overview) 在瀏覽器中使用，或者在 macOS、Linux 和 Windows 中[安裝](install-azure-cli.md)並從命令列中執行。</span><span class="sxs-lookup"><span data-stu-id="15623-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="15623-107">Azure CLI 2.0 已針對從命令列管理 Azure 資源進行最佳化，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。</span><span class="sxs-lookup"><span data-stu-id="15623-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="15623-108">使用 Azure CLI 2.0，您只要輕鬆輸入下列命令，就可以在 Azure 中建立 VM：</span><span class="sxs-lookup"><span data-stu-id="15623-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="15623-109">使用 [Cloud Shell](/azure/cloud-shell/overview) 在您的瀏覽器中執行 CLI，或在 macOS、Linux 或 Windows 中[安裝](install-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="15623-109">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="15623-110">閱讀[開始使用](get-started-with-azure-cli.md)文章來開始使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="15623-110">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="15623-111">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="15623-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="15623-112">下列範例可協助您了解如何使用 Azure CLI 2.0 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="15623-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="15623-113">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="15623-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="15623-114">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="15623-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="15623-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="15623-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="15623-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="15623-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="15623-117">另提供詳細的[參考](/cli/azure/)，說明如何使用每個個別的 Azure CLI 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="15623-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="15623-118">立即[開始使用](get-started-with-azure-cli.md) Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="15623-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="15623-119">如果您使用舊版的 CLI (Azure CLI)，可以繼續使用。</span><span class="sxs-lookup"><span data-stu-id="15623-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="15623-120">如果您同時使用這兩個 CLI，請記住，`azure` 是舊的 CLI - Azure CLI，而 `az` 是新的 CLI - Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="15623-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 