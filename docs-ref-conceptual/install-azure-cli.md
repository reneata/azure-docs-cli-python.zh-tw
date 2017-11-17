---
title: "安裝 Azure CLI 2.0"
description: "安裝 Azure CLI 2.0 的參考文件"
keywords: "Azure CLI 2.0、Azure CLI 2.0 參考、安裝 Azure CLI 2.0、Azure Python CLI、解除安裝 Azure CLI 2.0"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 08/17/2017
ms.topic: "articleå"
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 432edac070e238a6f1be0ccd76b9b3582b082219
ms.sourcegitcommit: 2ec80224c6b831e31038b710d912c0dbb1ddfef6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="4fcb9-104">安裝 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="4fcb9-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="4fcb9-105">立即安裝新版 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="4fcb9-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="4fcb9-106">我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="4fcb9-107">它可以用於 macOS、Linux 和 Windows。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="4fcb9-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-109">如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="4fcb9-110">macOS</span><span class="sxs-lookup"><span data-stu-id="4fcb9-110">macOS</span></span>

> [!WARNING]
> <span data-ttu-id="4fcb9-111">Azure CLI 的 Homebrew 公式 `azure-cli` 目前過期，且會安裝舊版。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-111">The Homebrew formula for the Azure CLI, `azure-cli`, is currently out of date and will install a previous version.</span></span>

1. <span data-ttu-id="4fcb9-112">使用 `curl` 命令來安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-112">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="4fcb9-113">您可能必須重新啟動命令殼層，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-113">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="4fcb9-114">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-114">Run the CLI from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="4fcb9-115">當您使用 InstallAzureCli 安裝時，不支援 [`az component update`](/cli/azure/component#update)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-115">When you install with InstallAzureCli, [`az component update`](/cli/azure/component#update) isn't supported.</span></span>
> <span data-ttu-id="4fcb9-116">若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-116">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="4fcb9-117">若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-117">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="4fcb9-118">Windows</span><span class="sxs-lookup"><span data-stu-id="4fcb9-118">Windows</span></span>

<span data-ttu-id="4fcb9-119">您可以使用 MSI 來安裝 Azure CLI 2.0，然後在 Windows 命令列中使用它，或是使用 Windows 上 Ubuntu 之 Bash 上的 apt-get 來安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-119">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="4fcb9-120">適用於 Windows 命令列的 MSI</span><span class="sxs-lookup"><span data-stu-id="4fcb9-120">MSI for the Windows command-line</span></span> 

<span data-ttu-id="4fcb9-121">若要在 Windows 上安裝 CLI，然後在 Windows 命令列中使用它，請下載並執行 [msi](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-121">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-122">使用 msi 來進行安裝時，不支援 [`az component`](/cli/azure/component)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-122">When you install with the msi, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="4fcb9-123">若要更新成最新的 CLI，請重新執行 [msi](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-123">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="4fcb9-124">若要將 CLI 解除安裝，請重新執行 [msi](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-124">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="4fcb9-125">Windows 上 Ubuntu 之 Bash 的 apt-get</span><span class="sxs-lookup"><span data-stu-id="4fcb9-125">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="4fcb9-126">如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="4fcb9-127">開啟 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="4fcb9-128">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="4fcb9-129">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="4fcb9-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="4fcb9-130">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-130">Run the CLI from the command prompt with the `az` command.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-131">當您使用 apt-get 進行安裝時，不支援 [`az component`](/cli/azure/component)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-131">When you install with apt-get, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="4fcb9-132">若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-132">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="4fcb9-133">若要解除安裝，請執行 `sudo apt-get remove azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-133">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="apt-get-for-debianubuntu"></a><span data-ttu-id="4fcb9-134">apt-get for Debian/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="4fcb9-134">apt-get for Debian/Ubuntu</span></span>

<span data-ttu-id="4fcb9-135">以 Debian/Ubuntu 為基礎的系統，您可以透過 `apt-get` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-135">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="4fcb9-136">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-136">Modify your sources list.</span></span>
 
   - <span data-ttu-id="4fcb9-137">32 位元系統</span><span class="sxs-lookup"><span data-stu-id="4fcb9-137">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="4fcb9-138">64 位元系統</span><span class="sxs-lookup"><span data-stu-id="4fcb9-138">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="4fcb9-139">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="4fcb9-139">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="4fcb9-140">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-140">Run the CLI from the command prompt with the `az` command.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-141">當您使用 apt-get 進行安裝時，不支援 [`az component`](/cli/azure/component)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-141">When you install with apt-get, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="4fcb9-142">若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-142">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="4fcb9-143">若要解除安裝，請執行 `sudo apt-get remove azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-143">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="docker"></a><span data-ttu-id="4fcb9-144">Docker</span><span class="sxs-lookup"><span data-stu-id="4fcb9-144">Docker</span></span>

<span data-ttu-id="4fcb9-145">我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-145">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="4fcb9-146">使用 `docker run` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-146">Install the CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="4fcb9-147">請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-147">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-148">如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-148">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

>> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

<span data-ttu-id="4fcb9-149">CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-149">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcb9-150">Docker 映像不支援 [`az component`](/cli/azure/component) 功能。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-150">The Docker image does not support the [`az component`](/cli/azure/component) feature.</span></span>
> <span data-ttu-id="4fcb9-151">若要更新 Azure CLI 2.0，請使用 `docker run` 來安裝最新的映像或您想要的特定映像。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-151">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="linux"></a><span data-ttu-id="4fcb9-152">Linux</span><span class="sxs-lookup"><span data-stu-id="4fcb9-152">Linux</span></span>

1. <span data-ttu-id="4fcb9-153">如果沒有 Python，請[安裝](https://www.python.org/downloads)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-153">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="4fcb9-154">根據您的 Linux 散發套件，安裝必要條件。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-154">Depending on your Linux distribution, install the prerequisites.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

3. <span data-ttu-id="4fcb9-155">使用一個 `curl` 命令安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-155">Install the CLI with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

4. <span data-ttu-id="4fcb9-156">您可能必須重新啟動命令殼層，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-156">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

5. <span data-ttu-id="4fcb9-157">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-157">Run the CLI from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="4fcb9-158">當您使用 InstallAzureCli 安裝時，不支援 [`az component update`](/cli/azure/component#update)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-158">When you install with InstallAzureCli, [`az component update`](/cli/azure/component#update) isn't supported.</span></span>
> <span data-ttu-id="4fcb9-159">若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-159">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="4fcb9-160">若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-160">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="4fcb9-161">疑難排解</span><span class="sxs-lookup"><span data-stu-id="4fcb9-161">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="4fcb9-162">使用 curl 重新導向時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="4fcb9-162">Errors with curl redirection</span></span>

<span data-ttu-id="4fcb9-163">如果您收到與 `-L` 參數有關，來自 `curl` 命令的錯誤，或者是某錯誤指出「物件已移動」，請嘗試使用完整的 url，而非 aka.ms url：</span><span class="sxs-lookup"><span data-stu-id="4fcb9-163">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a><span data-ttu-id="4fcb9-164">解除安裝</span><span class="sxs-lookup"><span data-stu-id="4fcb9-164">Uninstall</span></span>

<span data-ttu-id="4fcb9-165">如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-165">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="4fcb9-166">移除已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-166">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="4fcb9-167">將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-167">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="4fcb9-168">預設安裝位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-168">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="4fcb9-169">如果您使用 apt-get、Docker 或 msi 來安裝 CLI，請使用相同的工具來將它解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-169">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="4fcb9-170">報告問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="4fcb9-170">Reporting issues and feedback</span></span>

<span data-ttu-id="4fcb9-171">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-171">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="4fcb9-172">若要透過命令行提供意見反應，請嘗試 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="4fcb9-172">To provide feedback from the command line, try the `az feedback` command.</span></span>
