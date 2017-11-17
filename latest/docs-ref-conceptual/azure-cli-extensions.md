---
title: "Azure CLI 2.0 延伸模組"
description: "使用 Azure CLI 2.0 延伸模組"
keywords: "Azure CLI, 延伸模組"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 930073324d68f9719ce5035388120e7b6ac41a98
ms.sourcegitcommit: 93f6bd2c199774fcb3b43c6b14d714196873ed04
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2017
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="f578d-104">使用 Azure CLI 2.0 延伸模組</span><span class="sxs-lookup"><span data-stu-id="f578d-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="f578d-105">延伸模組是個別的模組，並未隨附在 Azure CLI 中；可讓您以新增命令的方式來新增功能。</span><span class="sxs-lookup"><span data-stu-id="f578d-105">Extensions are individual modules not shipped with the Azure CLI itself that allow you to add functionality through new commands.</span></span> <span data-ttu-id="f578d-106">這些模組可能是實驗性或發行前提供的版本、Microsoft 專為您的需求設計的特定工具，或甚至是您自己撰寫的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-106">These might be experimental or pre-release offerings, specialized tools that Microsoft has for your needs, or even extensions that you yourself have written.</span></span> <span data-ttu-id="f578d-107">延伸模組可提供搭配 CLI 使用的靈活性，可讓您依需求進行修改，無需使用與核心功能組不相關的其他套件。</span><span class="sxs-lookup"><span data-stu-id="f578d-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="f578d-108">本文會協助您了解如何安裝、更新及移除 CLI 延伸模組，</span><span class="sxs-lookup"><span data-stu-id="f578d-108">This article will help you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="f578d-109">也會包含延伸模組行為的常見問題回答。</span><span class="sxs-lookup"><span data-stu-id="f578d-109">It should also answer common questions about extension behavior.</span></span>

## <a name="finding-extensions"></a><span data-ttu-id="f578d-110">尋找延伸模組</span><span class="sxs-lookup"><span data-stu-id="f578d-110">Finding extensions</span></span>

<span data-ttu-id="f578d-111">若要知道會提供哪些延伸模組，您可以使用 `az extension list-available`。</span><span class="sxs-lookup"><span data-stu-id="f578d-111">In order to know what extensions are available, you can use `az extension list-available`.</span></span> <span data-ttu-id="f578d-112">此命令會列出由 Microsoft 提供，可用且正式的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-112">This command lists the available, official extensions which are provided and supported by Microsoft.</span></span>

## <a name="installing-extensions"></a><span data-ttu-id="f578d-113">安裝延伸模組</span><span class="sxs-lookup"><span data-stu-id="f578d-113">Installing extensions</span></span>

<span data-ttu-id="f578d-114">一旦找到要安裝延伸模組，請使用 `az extension add` 加以取得。</span><span class="sxs-lookup"><span data-stu-id="f578d-114">Once you have found an extension to install, use `az extension add` to get it.</span></span> <span data-ttu-id="f578d-115">如果延伸模組是在 `az extension list-available` 中所列出的正式 Microsoft 延伸模組，您可以依名稱來安裝延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-115">If the extension is an official Microsoft extension listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli
az extension add --name <extension-name>
```

<span data-ttu-id="f578d-116">如果延伸模組是來自於外部資源，或者您擁有該延伸模組的直接連結，可以提供來源網址或本機路徑。</span><span class="sxs-lookup"><span data-stu-id="f578d-116">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="f578d-117">延伸模組_必須_是編譯過的 Python Whell 檔案。</span><span class="sxs-lookup"><span data-stu-id="f578d-117">This _must_ be a compiled Python wheel file.</span></span>

```azurecli
az extension add --source <URL-or-path>
```

<span data-ttu-id="f578d-118">安裝延伸模組之後，便可以在 `$AZURE_EXTENSION_DIR` shell 變數的值下找到該延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-118">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="f578d-119">如果未設定這個變數，則 Linux 及 macOS 上的預設值為 `$HOME/.azure/cliextensions`，Windows 上的預設值為 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="f578d-119">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="updating-extensions"></a><span data-ttu-id="f578d-120">更新延伸模組</span><span class="sxs-lookup"><span data-stu-id="f578d-120">Updating extensions</span></span>

<span data-ttu-id="f578d-121">延伸模組只能依名稱更新：</span><span class="sxs-lookup"><span data-stu-id="f578d-121">Extensions can only be updated by name:</span></span>

```azurecli
az extension update --name <extension-name>
```

<span data-ttu-id="f578d-122">如果 CLI 因為任何原因無法解析延伸模組名稱，請重新安裝延伸模組名稱並更新。</span><span class="sxs-lookup"><span data-stu-id="f578d-122">If an extension name cannot be resolved by the CLI for whatever reason, reinstall the extension to update it.</span></span> <span data-ttu-id="f578d-123">此外，也有可能是延伸模組被移出預覽，成為 CLI 內建命令。</span><span class="sxs-lookup"><span data-stu-id="f578d-123">There is also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="f578d-124">在此情況下，更新 CLI，並解除安裝延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-124">In that case, update the CLI and uninstall the extension.</span></span>

## <a name="uninstalling-extensions"></a><span data-ttu-id="f578d-125">解除安裝延伸模組</span><span class="sxs-lookup"><span data-stu-id="f578d-125">Uninstalling extensions</span></span>

<span data-ttu-id="f578d-126">如果您不再需要延伸模組，可以使用 `az extension remove` 移除，</span><span class="sxs-lookup"><span data-stu-id="f578d-126">If you no longer need an extension, it can be removed with `az extension remove`,</span></span>

```azurecli
az extension remove --name <extension-name>
```

<span data-ttu-id="f578d-127">您也可以從安裝位置手動移除延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-127">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="f578d-128">這將會是 `$AZURE_EXTENSION_DIR` Shell 變數的值。</span><span class="sxs-lookup"><span data-stu-id="f578d-128">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="f578d-129">如果未設定這個變數，則 Linux 及 macOS 上的預設值為 `$HOME/.azure/cliextensions`，Windows 上的預設值為 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="f578d-129">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="f578d-130">建議您使用 `az extension remove` 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f578d-130">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="f578d-131">常見問題集</span><span class="sxs-lookup"><span data-stu-id="f578d-131">FAQ</span></span>

<span data-ttu-id="f578d-132">以下是一些 CLI 延伸模組的相關常見問題解答。</span><span class="sxs-lookup"><span data-stu-id="f578d-132">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="f578d-133">允許使用何種檔案格式安裝？</span><span class="sxs-lookup"><span data-stu-id="f578d-133">What file formats are allowed for installation?</span></span>

<span data-ttu-id="f578d-134">目前，只有編譯的 Python Whell 可以安裝為延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f578d-134">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="f578d-135">延伸模組可以取代現有的命令嗎？</span><span class="sxs-lookup"><span data-stu-id="f578d-135">Can extensions replace existing commands?</span></span>

<span data-ttu-id="f578d-136">是。</span><span class="sxs-lookup"><span data-stu-id="f578d-136">Yes.</span></span> <span data-ttu-id="f578d-137">延伸模組可能會取代現有的命令，但在執行已取代 CLI 的命令之前，會發出警告。</span><span class="sxs-lookup"><span data-stu-id="f578d-137">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="f578d-138">如何知道發行前版本中是否包括延伸模組？</span><span class="sxs-lookup"><span data-stu-id="f578d-138">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="f578d-139">如果發行前版本中包括延伸模組，則應該會在延伸模組的文件和版本控制中找到延伸模的記錄。</span><span class="sxs-lookup"><span data-stu-id="f578d-139">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="f578d-140">Microsoft 也可能會將 CLI 預覽命令發行為延伸模組，並規劃在產品通過預覽階段時，將這些延伸模組移至主要 CLI 介面。</span><span class="sxs-lookup"><span data-stu-id="f578d-140">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="f578d-141">延伸模組會彼此相依嗎？</span><span class="sxs-lookup"><span data-stu-id="f578d-141">Can extensions depend upon each other?</span></span>

<span data-ttu-id="f578d-142">否。</span><span class="sxs-lookup"><span data-stu-id="f578d-142">No.</span></span> <span data-ttu-id="f578d-143">延伸模組必須是個別的套件，並不會彼此相依。</span><span class="sxs-lookup"><span data-stu-id="f578d-143">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="f578d-144">這是因為 CLI 不保證何時會載入延伸模組，因此無法保證會滿足相依性。</span><span class="sxs-lookup"><span data-stu-id="f578d-144">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="f578d-145">安裝延伸模組只會安裝該延伸模組，即使您移除其他延伸模組，該延伸模組應該仍然會繼續工作。</span><span class="sxs-lookup"><span data-stu-id="f578d-145">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="f578d-146">延伸模組會與 CLI 一併更新嗎？</span><span class="sxs-lookup"><span data-stu-id="f578d-146">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="f578d-147">否。</span><span class="sxs-lookup"><span data-stu-id="f578d-147">No.</span></span> <span data-ttu-id="f578d-148">延伸模組必須個別進行更新，如[更新延伸模組](#updating-extensions)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="f578d-148">Extensions must be updated separately, as described in the [Updating extensions](#updating-extensions) section.</span></span>
