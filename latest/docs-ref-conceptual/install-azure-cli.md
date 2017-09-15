---
title: "安裝 Azure CLI 2.0"
description: "安裝 Azure CLI 2.0 的參考文件"
keywords: "Azure CLI, 安裝 Azure CLI, Azure Python CLI, Azure CLI 參考"
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
ms.openlocfilehash: a61f47076854d0ff0a7056f82240794b7533fe3e
ms.sourcegitcommit: 3db5fb207db551a0d3fe0a88fe09e8f5e2ec184d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/14/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="f0fc0-104">安裝 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f0fc0-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="f0fc0-105">立即安裝新版 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="f0fc0-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="f0fc0-106">我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="f0fc0-107">它可以用於 macOS、Linux 和 Windows。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="f0fc0-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f0fc0-109">如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="f0fc0-110"><a name="macOS"/>在 MacOS 上安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="f0fc0-111">使用 `curl` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="f0fc0-112">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="f0fc0-113">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="f0fc0-114">在 Windows 上安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-114">Install on Windows</span></span>

<span data-ttu-id="f0fc0-115">您可以使用 MSI 來安裝 Azure CLI 2.0，然後在 Windows 命令列中使用它，或是使用 Windows 上 Ubuntu 之 Bash 上的 `apt-get` 來安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="f0fc0-116">使用適用於 Windows 命令列的 MSI 安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="f0fc0-117">若要在 Windows 上安裝 CLI，然後在 Windows 命令列中使用它，請下載並執行 [MSI](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="f0fc0-118">使用 Windows 上 Ubuntu 之 Bash 的 apt-get 安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="f0fc0-119">如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="f0fc0-120">開啟 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="f0fc0-121">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="f0fc0-122">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="f0fc0-123">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="f0fc0-124">使用 apt get 在 Debian/Ubuntu 上安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="f0fc0-125">以 Debian/Ubuntu 為基礎的系統，您可以透過 `apt-get` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="f0fc0-126">修改來源清單：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-126">Modify your sources list:</span></span>
 
   - <span data-ttu-id="f0fc0-127">32 位元系統</span><span class="sxs-lookup"><span data-stu-id="f0fc0-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="f0fc0-128">64 位元系統</span><span class="sxs-lookup"><span data-stu-id="f0fc0-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="f0fc0-129">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="f0fc0-130">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a><span data-ttu-id="f0fc0-131">安裝於 RHEL、Fedora 及 CentOS 搭配 Yum</span><span class="sxs-lookup"><span data-stu-id="f0fc0-131">Install on RHEL, Fedora, and CentOS with yum</span></span>

<span data-ttu-id="f0fc0-132">對於任何以 RedHat 為基礎且包含 `yum` 套件管理員的散發套件，您可以透過 `yum` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-132">For any distribution which is based off of RedHat and contains the `yum` package manager, you can install Azure CLI 2.0 via `yum`.</span></span>

1. <span data-ttu-id="f0fc0-133">匯入 Microsoft 存放庫金鑰：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-133">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="f0fc0-134">建立本機 `azure-cli` 存放庫資訊：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-134">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="f0fc0-135">更新 `yum` 套件索引並安裝：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-135">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="f0fc0-136">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-136">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-opensuse-and-sle-with-zypper"></a><span data-ttu-id="f0fc0-137">安裝於 openSUSE 和 SLE 搭配 Zypper</span><span class="sxs-lookup"><span data-stu-id="f0fc0-137">Install on openSUSE and SLE with zypper</span></span>

1. <span data-ttu-id="f0fc0-138">匯入 Microsoft 存放庫金鑰：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-138">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="f0fc0-139">建立本機 `azure-cli` 存放庫資訊：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-139">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="f0fc0-140">更新 `zypper` 套件索引並安裝：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-140">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="f0fc0-141">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-141">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="f0fc0-142">使用 Docker 安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-142">Install with Docker</span></span>

<span data-ttu-id="f0fc0-143">我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-143">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="f0fc0-144">使用 `docker run` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-144">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="f0fc0-145">請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-145">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="f0fc0-146">CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-146">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="f0fc0-147">如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-147">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="f0fc0-148"><a name="Linux"/>不使用 apt-get 在 Linux 安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-148"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="f0fc0-149">如果可行，建議您使用套件管理員安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-149">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="f0fc0-150">針對不需要使用套件的散發套件，您可以手動方式來安裝。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-150">For distributions which do not have a package provided for them, you can manually install.</span></span>

1. <span data-ttu-id="f0fc0-151">以您的 Linux 散發套件作為基礎安裝必要條件。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-151">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="f0fc0-152">如果以上未列出您的散發套件，就必須安裝 [Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-152">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="f0fc0-153">使用 `curl` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-153">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="f0fc0-154">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-154">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="f0fc0-155">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-155">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f0fc0-156">疑難排解</span><span class="sxs-lookup"><span data-stu-id="f0fc0-156">Troubleshooting</span></span>

<span data-ttu-id="f0fc0-157">如果您在 CLI 安裝期間遇到問題，請查看此章節了解是否涵蓋您的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-157">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="f0fc0-158">如果您的問題不在這裡，請[提出 Github 問題](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-158">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="f0fc0-159">CURL「物件已移動」錯誤</span><span class="sxs-lookup"><span data-stu-id="f0fc0-159">curl "Object Moved" error</span></span>

<span data-ttu-id="f0fc0-160">如果您收到與 `-L` 參數有關，來自 `curl` 的錯誤，或者是包含「物件已移動」文字的錯誤訊息，請嘗試使用完整的 URL 而非 `aka.ms` 來重新導向：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-160">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="f0fc0-161">macOS 上安裝較舊版本的 Homebrew</span><span class="sxs-lookup"><span data-stu-id="f0fc0-161">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="f0fc0-162">macOS 可用的 Homebrew `azure-cli` 公式目前已過期，且會安裝 CLI 的 1.x 版本。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-162">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="f0fc0-163">您可以在更新時加以查看，方法是檢查 `brew info azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-163">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="f0fc0-164">在此之前，[解除安裝舊版](#uninstall_brew)並遵循 [macOS 安裝指示](#macOS)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-164">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="f0fc0-165">解除安裝 CLI 1.x 版本</span><span class="sxs-lookup"><span data-stu-id="f0fc0-165">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="f0fc0-166">如果您的系統上可使用較舊的 CLI 1.x 版本，就能以所使用的安裝類型作為基礎加以解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-166">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="f0fc0-167">使用 npm 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-167">Uninstall with npm</span></span>

<span data-ttu-id="f0fc0-168">使用 `npm uninstall` 將舊版的 CLI 移除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-168">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="f0fc0-169"><a name="uninstall_brew"/>使用 macOS 上的 Homebrew 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-169"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="f0fc0-170">使用 `brew uninstall` 將舊版的 CLI 移除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-170">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="f0fc0-171">使用可散佈解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-171">Uninstall with distributable</span></span>

<span data-ttu-id="f0fc0-172">如果您是透過 [MSI](http://aka.ms/webpi-azure-cli) 或 [macOS 套件](http://aka.ms/mac-azure-cli)安裝，請使用相同的工具將您的安裝移除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-172">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="f0fc0-173">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-173">Uninstall with Docker</span></span>

<span data-ttu-id="f0fc0-174">如果您安裝了 Docker 映像以使用較舊的 CLI 版本，請將該映像及任何相關聯的容器移除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-174">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="f0fc0-175">接著，您可以在安裝新的 Docker 映像之後重新建立容器，如安裝指示中所述。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-175">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="f0fc0-176">更新 CLI</span><span class="sxs-lookup"><span data-stu-id="f0fc0-176">Update the CLI</span></span>

<span data-ttu-id="f0fc0-177">若要更新 Azure CLI，請使用您用來安裝它的相同方法。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-177">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="f0fc0-178">使用 MSI 更新</span><span class="sxs-lookup"><span data-stu-id="f0fc0-178">Update with MSI</span></span>

<span data-ttu-id="f0fc0-179">再次執行 [MSI](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-179">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="f0fc0-180">使用 apt-get 更新</span><span class="sxs-lookup"><span data-stu-id="f0fc0-180">Update with apt-get</span></span>

<span data-ttu-id="f0fc0-181">若要更新 CLI 套件，請使用 `apt-get upgrade`。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-181">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="f0fc0-182">這會將您系統上所有已安裝但尚未進行相依性變更的套件進行升級。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-182">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="f0fc0-183">若只要升級 CLI，請使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-183">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="f0fc0-184">使用 Docker 更新</span><span class="sxs-lookup"><span data-stu-id="f0fc0-184">Update with Docker</span></span>

1. <span data-ttu-id="f0fc0-185">使用 `docker pull` 更新本機映像。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-185">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="f0fc0-186">取得目前使用 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-186">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="f0fc0-187">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-187">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="f0fc0-188">停止並重新建立容器。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-188">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="f0fc0-189">手動更新</span><span class="sxs-lookup"><span data-stu-id="f0fc0-189">Update manually</span></span>

<span data-ttu-id="f0fc0-190">請遵循 [macOS](#macOS) 或 [Linux](#Linux) 的手動安裝指示進行更新。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-190">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="f0fc0-191">解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-191">Uninstall</span></span>

<span data-ttu-id="f0fc0-192">如果您決定要將 CLI 解除安裝，我們很遺憾您不再繼續使用。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-192">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f0fc0-193">您應該使用您用來安裝 CLI 的相同方法來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-193">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="f0fc0-194">使用 MSI 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-194">Uninstall with MSI</span></span>

<span data-ttu-id="f0fc0-195">請重新執行 [MSI](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-195">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="f0fc0-196">使用 apt get 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-196">Uninstall with apt-get</span></span>

<span data-ttu-id="f0fc0-197">透過 `apt-get remove` 解除安裝：</span><span class="sxs-lookup"><span data-stu-id="f0fc0-197">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="f0fc0-198">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-198">Uninstall with Docker</span></span>

<span data-ttu-id="f0fc0-199">如果您已安裝 Docker 映像，就必須移除任何執行它的容器，然後再將本機映像刪除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-199">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="f0fc0-200">取得執行 azure-cli 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-200">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="f0fc0-201">將任何使用 CLI 映像的容器刪除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-201">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="f0fc0-202">將本機安裝的 CLI 映像移除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-202">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="f0fc0-203">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-203">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="f0fc0-204">手動解除安裝</span><span class="sxs-lookup"><span data-stu-id="f0fc0-204">Uninstall manually</span></span>

<span data-ttu-id="f0fc0-205">如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-205">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="f0fc0-206">移除已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-206">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="f0fc0-207">將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-207">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="f0fc0-208">預設安裝位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-208">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="f0fc0-209">報告 CLI 問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="f0fc0-209">Report CLI issues and feedback</span></span>

<span data-ttu-id="f0fc0-210">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-210">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="f0fc0-211">若要從命令列提供意見反應，請使用 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="f0fc0-211">To provide feedback from the command line, use the `az feedback` command.</span></span>
