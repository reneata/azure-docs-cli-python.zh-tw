---
title: "安裝 Azure CLI 2.0"
description: "安裝 Azure CLI 2.0 的參考文件"
keywords: "Azure CLI 2.0, Azure CLI 2.0 參考, 安裝 Azure CLI 2.0, Azure Python CLI, 解除安裝 Azure CLI 2.0, Azure CLI, 安裝 Azure CLI, Azure CLI 參考"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 08/17/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 00d5b555975007d7e57f04ce5d69f4f29e6d0219
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="5dd33-104">安裝 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="5dd33-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="5dd33-105">立即安裝新版 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="5dd33-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="5dd33-106">我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="5dd33-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="5dd33-107">它可以用於 macOS、Linux 和 Windows。</span><span class="sxs-lookup"><span data-stu-id="5dd33-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="5dd33-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5dd33-109">如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。</span><span class="sxs-lookup"><span data-stu-id="5dd33-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="5dd33-110"><a name="macOS"/>在 MacOS 上安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="5dd33-111">使用 `curl` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="5dd33-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="5dd33-112">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="5dd33-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="5dd33-113">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="5dd33-114">在 Windows 上安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-114">Install on Windows</span></span>

<span data-ttu-id="5dd33-115">您可以使用 MSI 來安裝 Azure CLI 2.0，然後在 Windows 命令列中使用它，或是使用 Windows 上 Ubuntu 之 Bash 上的 `apt-get` 來安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="5dd33-116">使用適用於 Windows 命令列的 MSI 安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="5dd33-117">若要在 Windows 上安裝 CLI，然後在 Windows 命令列中使用它，請下載並執行 [MSI](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="5dd33-118">使用 Windows 上 Ubuntu 之 Bash 的 apt-get 安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="5dd33-119">如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="5dd33-120">開啟 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="5dd33-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="5dd33-121">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="5dd33-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="5dd33-122">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="5dd33-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="5dd33-123">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="5dd33-124">使用 apt get 在 Debian/Ubuntu 上安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="5dd33-125">以 Debian/Ubuntu 為基礎的系統，您可以透過 `apt-get` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="5dd33-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="5dd33-126">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="5dd33-126">Modify your sources list.</span></span>
 
   - <span data-ttu-id="5dd33-127">32 位元系統</span><span class="sxs-lookup"><span data-stu-id="5dd33-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="5dd33-128">64 位元系統</span><span class="sxs-lookup"><span data-stu-id="5dd33-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="5dd33-129">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="5dd33-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="5dd33-130">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="5dd33-131">使用 Docker 安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-131">Install with Docker</span></span>

<span data-ttu-id="5dd33-132">我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="5dd33-132">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="5dd33-133">使用 `docker run` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-133">Install the CLI using `docker run`.</span></span>

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

<span data-ttu-id="5dd33-134">請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。</span><span class="sxs-lookup"><span data-stu-id="5dd33-134">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="5dd33-135">CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="5dd33-135">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="5dd33-136">如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。</span><span class="sxs-lookup"><span data-stu-id="5dd33-136">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="5dd33-137"><a name="Linux"/>不使用 apt-get 在 Linux 安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-137"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="5dd33-138">如果可行，建議您使用 `apt-get` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-138">It is recommended that you install the CLI with `apt-get` if you are able to.</span></span> <span data-ttu-id="5dd33-139">針對不需要使用 `apt` 套件管理員的散發套件，您可以手動方式來安裝。</span><span class="sxs-lookup"><span data-stu-id="5dd33-139">For distributions which do not use the `apt` package manager, you can manually install.</span></span>

1. <span data-ttu-id="5dd33-140">以您的 Linux 散發套件作為基礎安裝必要條件。</span><span class="sxs-lookup"><span data-stu-id="5dd33-140">Install the prerequisites based on your Linux distribution.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

<span data-ttu-id="5dd33-141">如果以上未列出您的散發套件，就必須安裝 [Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-141">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="5dd33-142">使用 `curl` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-142">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="5dd33-143">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="5dd33-143">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="5dd33-144">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="5dd33-144">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5dd33-145">疑難排解</span><span class="sxs-lookup"><span data-stu-id="5dd33-145">Troubleshooting</span></span>

<span data-ttu-id="5dd33-146">如果您在 CLI 安裝期間遇到問題，請查看此章節了解是否涵蓋您的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="5dd33-146">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="5dd33-147">如果您的問題不在這裡，請[提出 Github 問題](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-147">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="5dd33-148">CURL「物件已移動」錯誤</span><span class="sxs-lookup"><span data-stu-id="5dd33-148">curl "Object Moved" error</span></span>

<span data-ttu-id="5dd33-149">如果您收到與 `-L` 參數有關，來自 `curl` 的錯誤，或者是包含「物件已移動」文字的錯誤訊息，請嘗試使用完整的 URL 而非 `aka.ms` 來重新導向：</span><span class="sxs-lookup"><span data-stu-id="5dd33-149">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="5dd33-150">macOS 上安裝較舊版本的 Homebrew</span><span class="sxs-lookup"><span data-stu-id="5dd33-150">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="5dd33-151">macOS 可用的 Homebrew `azure-cli` 公式目前已過期，且會安裝 CLI 的 1.x 版本。</span><span class="sxs-lookup"><span data-stu-id="5dd33-151">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="5dd33-152">您可以在更新時加以查看，方法是檢查 `brew info azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="5dd33-152">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="5dd33-153">在此之前，[解除安裝舊版](#uninstall_brew)並遵循 [macOS 安裝指示](#macOS)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-153">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="5dd33-154">解除安裝 CLI 1.x 版本</span><span class="sxs-lookup"><span data-stu-id="5dd33-154">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="5dd33-155">如果您的系統上可使用較舊的 CLI 1.x 版本，就能以所使用的安裝類型作為基礎加以解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5dd33-155">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="5dd33-156">使用 npm 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-156">Uninstall with npm</span></span>

<span data-ttu-id="5dd33-157">使用 `npm uninstall` 將舊版的 CLI 移除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-157">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="5dd33-158"><a name="uninstall_brew"/>使用 macOS 上的 Homebrew 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-158"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="5dd33-159">使用 `brew uninstall` 將舊版的 CLI 移除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-159">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="5dd33-160">使用可散佈解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-160">Uninstall with distributable</span></span>

<span data-ttu-id="5dd33-161">如果您是透過 [MSI](http://aka.ms/webpi-azure-cli) 或 [macOS 套件](http://aka.ms/mac-azure-cli)安裝，請使用相同的工具將您的安裝移除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-161">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="5dd33-162">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-162">Uninstall with Docker</span></span>

<span data-ttu-id="5dd33-163">如果您安裝了 Docker 映像以使用較舊的 CLI 版本，請將該映像及任何相關聯的容器移除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-163">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="5dd33-164">接著，您可以在安裝新的 Docker 映像之後重新建立容器，如安裝指示中所述。</span><span class="sxs-lookup"><span data-stu-id="5dd33-164">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="5dd33-165">更新 CLI</span><span class="sxs-lookup"><span data-stu-id="5dd33-165">Update the CLI</span></span>

<span data-ttu-id="5dd33-166">若要更新 Azure CLI，請使用您用來安裝它的相同方法。</span><span class="sxs-lookup"><span data-stu-id="5dd33-166">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="5dd33-167">使用 MSI 更新</span><span class="sxs-lookup"><span data-stu-id="5dd33-167">Update with MSI</span></span>

<span data-ttu-id="5dd33-168">再次執行 [MSI](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="5dd33-168">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="5dd33-169">使用 apt-get 更新</span><span class="sxs-lookup"><span data-stu-id="5dd33-169">Update with apt-get</span></span>

<span data-ttu-id="5dd33-170">若要更新 CLI 套件，請使用 `apt-get upgrade`。</span><span class="sxs-lookup"><span data-stu-id="5dd33-170">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="5dd33-171">這會將您系統上所有已安裝但尚未進行相依性變更的套件進行升級。</span><span class="sxs-lookup"><span data-stu-id="5dd33-171">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="5dd33-172">若只要升級 CLI，請使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="5dd33-172">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="5dd33-173">使用 Docker 更新</span><span class="sxs-lookup"><span data-stu-id="5dd33-173">Update with Docker</span></span>

1. <span data-ttu-id="5dd33-174">使用 `docker pull` 更新本機映像。</span><span class="sxs-lookup"><span data-stu-id="5dd33-174">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="5dd33-175">取得目前使用 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="5dd33-175">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="5dd33-176">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="5dd33-176">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="5dd33-177">停止並重新建立容器。</span><span class="sxs-lookup"><span data-stu-id="5dd33-177">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="5dd33-178">手動更新</span><span class="sxs-lookup"><span data-stu-id="5dd33-178">Update manually</span></span>

<span data-ttu-id="5dd33-179">請遵循 [macOS](#macOS) 或 [Linux](#Linux) 的手動安裝指示進行更新。</span><span class="sxs-lookup"><span data-stu-id="5dd33-179">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="5dd33-180">解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-180">Uninstall</span></span>

<span data-ttu-id="5dd33-181">如果您決定要將 CLI 解除安裝，我們很遺憾您不再繼續使用。</span><span class="sxs-lookup"><span data-stu-id="5dd33-181">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="5dd33-182">您應該使用您用來安裝 CLI 的相同方法來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5dd33-182">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="5dd33-183">使用 MSI 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-183">Uninstall with MSI</span></span>

<span data-ttu-id="5dd33-184">請重新執行 [MSI](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5dd33-184">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="5dd33-185">使用 apt get 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-185">Uninstall with apt-get</span></span>

<span data-ttu-id="5dd33-186">透過 `apt-get remove` 解除安裝：</span><span class="sxs-lookup"><span data-stu-id="5dd33-186">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="5dd33-187">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-187">Uninstall with Docker</span></span>

<span data-ttu-id="5dd33-188">如果您已安裝 Docker 映像，就必須移除任何執行它的容器，然後再將本機映像刪除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-188">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="5dd33-189">取得執行 azure-cli 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="5dd33-189">Get the containers which are running the azure-cli image.</span></span>

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. <span data-ttu-id="5dd33-190">將任何使用 CLI 映像的容器刪除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-190">Delete any containers with the CLI image.</span></span>

  ```bash
  docker rm 34a868beb2ab
  ```

3. <span data-ttu-id="5dd33-191">將本機安裝的 CLI 映像移除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-191">Remove the locally installed CLI image.</span></span>

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> <span data-ttu-id="5dd33-192">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="5dd33-192">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="5dd33-193">手動解除安裝</span><span class="sxs-lookup"><span data-stu-id="5dd33-193">Uninstall manually</span></span>

<span data-ttu-id="5dd33-194">如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5dd33-194">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="5dd33-195">移除已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="5dd33-195">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="5dd33-196">將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。</span><span class="sxs-lookup"><span data-stu-id="5dd33-196">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="5dd33-197">預設安裝位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="5dd33-197">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="5dd33-198">報告 CLI 問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="5dd33-198">Report CLI issues and feedback</span></span>

<span data-ttu-id="5dd33-199">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="5dd33-199">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="5dd33-200">若要從命令列提供意見反應，請使用 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="5dd33-200">To provide feedback from the command line, use the `az feedback` command.</span></span>
