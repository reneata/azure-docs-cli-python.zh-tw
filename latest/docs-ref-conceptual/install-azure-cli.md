---
title: "安裝 Azure CLI 2.0"
description: "安裝 Azure CLI 2.0 的參考文件"
keywords: "Azure CLI, 安裝 Azure CLI, Azure Python CLI, Azure CLI 參考"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 2b56382355cad5313a604ed1f493a2bcbebf3e27
ms.sourcegitcommit: e9b4c6dd9093980b69ca47f93f44ac54d0e5b68a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/03/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="ea184-104">安裝 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="ea184-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="ea184-105">立即安裝新版 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="ea184-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="ea184-106">我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="ea184-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="ea184-107">它可以用於 macOS、Linux 和 Windows。</span><span class="sxs-lookup"><span data-stu-id="ea184-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="ea184-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="ea184-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ea184-109">如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。</span><span class="sxs-lookup"><span data-stu-id="ea184-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="ea184-110"><a name="macOS"/>在 MacOS 上安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-110"><a name="macOS"/>Install on macOS</span></span>

<span data-ttu-id="ea184-111">您可以在 macOS 上使用 [Homebrew](https://brew.sh/) 或手動安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-111">On macOS, you are able to install either with [Homebrew](https://brew.sh/) or manually.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="ea184-112">使用 Homebrew 安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-112">Install with Homebrew</span></span>

1. <span data-ttu-id="ea184-113">如果您沒有 Homebrew，請依 [Homebrew 安裝指示](https://docs.brew.sh/Installation.html)安裝 Homebrew。</span><span class="sxs-lookup"><span data-stu-id="ea184-113">If you don't have it already, install Homebrew by following the [Homebrew installation instructions](https://docs.brew.sh/Installation.html).</span></span>

2. <span data-ttu-id="ea184-114">如果您先前曾手動安裝 CLI，請遵循[手動解除安裝](#UninstallManually)指示。</span><span class="sxs-lookup"><span data-stu-id="ea184-114">If you have previously installed the CLI manually, follow the [manual uninstall](#UninstallManually) instructions.</span></span>

3. <span data-ttu-id="ea184-115">更新您的本機 Homebrew 存放庫。</span><span class="sxs-lookup"><span data-stu-id="ea184-115">Update your local Homebrew repositories.</span></span>

   ```bash
   brew update
   ```

4. <span data-ttu-id="ea184-116">安裝 `azure-cli` 套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-116">Install the `azure-cli` package.</span></span>

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> <span data-ttu-id="ea184-117">若您之前使用 Homebrew 安裝 Azure CLI 1.0，而不是安裝套件，您可以透過一般的 Homebrew 升級程序取得 CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="ea184-117">If you previously installed the Azure CLI 1.0 with Homebrew, instead of installing the package you can get CLI 2.0 through the regular Homebrew upgrade process.</span></span>
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a><span data-ttu-id="ea184-118">手動安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-118">Install manually</span></span>

1. <span data-ttu-id="ea184-119">使用 `curl` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="ea184-119">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="ea184-120">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="ea184-120">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="ea184-121">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-121">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="ea184-122">在 Windows 上安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-122">Install on Windows</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="ea184-123">使用適用於 Windows 命令列的 MSI 安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-123">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="ea184-124">若要在 Windows 上安裝 CLI，並在 Windows 命令列中加以使用，請下載並執行 [Azure CLI 安裝程式 (MSI)](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="ea184-124">To install the CLI on Windows and use it in the Windows command-line, download and run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="ea184-125">使用 Windows 上 Ubuntu 之 Bash 的 apt-get 安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-125">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="ea184-126">如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="ea184-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="ea184-127">開啟 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="ea184-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="ea184-128">修改來源清單。</span><span class="sxs-lookup"><span data-stu-id="ea184-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="ea184-129">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="ea184-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="ea184-130">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-apt-package-manager"></a><span data-ttu-id="ea184-131">透過 APT 套件管理員安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-131">Install with apt package manager</span></span> 

<span data-ttu-id="ea184-132">針對使用 `apt` 套件管理員的散發套件 (例如 Ubuntu 或 Debian)，您可以透過 `apt-get` 來安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="ea184-132">For distributions using the `apt` package manager such as Ubuntu or Debian, you can install Azure CLI 2.0 via `apt-get`.</span></span>

> [!NOTE]
> <span data-ttu-id="ea184-133">您必須具備 Python 2.7.x 或 Python 3.x，才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-133">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="ea184-134">如果您的散發套件並沒有套件，且您也沒有 Python 2.7.x 或 Python 3.x，請[安裝 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="ea184-134">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="ea184-135">修改來源清單：</span><span class="sxs-lookup"><span data-stu-id="ea184-135">Modify your sources list:</span></span>
 
   - <span data-ttu-id="ea184-136">32 位元系統</span><span class="sxs-lookup"><span data-stu-id="ea184-136">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="ea184-137">64 位元系統</span><span class="sxs-lookup"><span data-stu-id="ea184-137">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="ea184-138">執行下列 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="ea184-138">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="ea184-139">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-139">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-yum-package-manager"></a><span data-ttu-id="ea184-140">透過 Yum 套件管理員安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-140">Install with yum package manager</span></span>

<span data-ttu-id="ea184-141">針對使用 `yum` 套件管理員的散發套件，例如 Red Hat Enterprise Linux (RHEL)、Fedora 或 CentOS，您可以透過 `yum` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="ea184-141">For distributions which use the `yum` package manager such as Red Hat Enterprise Linux (RHEL), Fedora, or CentOS, you can install Azure CLI 2.0 via `yum`.</span></span>

> [!NOTE]
> <span data-ttu-id="ea184-142">您必須具備 Python 2.7.x 或 Python 3.x，才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-142">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="ea184-143">如果您的散發套件並沒有套件，且您也沒有 Python 2.7.x 或 Python 3.x，請[安裝 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="ea184-143">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="ea184-144">匯入 Microsoft 存放庫金鑰：</span><span class="sxs-lookup"><span data-stu-id="ea184-144">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="ea184-145">建立本機 `azure-cli` 存放庫資訊：</span><span class="sxs-lookup"><span data-stu-id="ea184-145">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="ea184-146">更新 `yum` 套件索引並安裝：</span><span class="sxs-lookup"><span data-stu-id="ea184-146">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="ea184-147">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-147">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-zypper-package-manager"></a><span data-ttu-id="ea184-148">透過 Zypper 套件管理員安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-148">Install with zypper package manager</span></span>

<span data-ttu-id="ea184-149">針對使用 `zypper` 套件管理員的散發套件，例如 OpenSUSE 或 SLE，您可以透過 `zypper` 安裝 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="ea184-149">For distributions which use the `zypper` package manager such as OpenSUSE or SLE, you can install Azure CLI 2.0 via `zypper`.</span></span>

> [!NOTE]
> <span data-ttu-id="ea184-150">您必須具備 Python 2.7.x 或 Python 3.x，才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-150">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="ea184-151">如果您的散發套件並沒有套件，且您也沒有 Python 2.7.x 或 Python 3.x，請[安裝 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="ea184-151">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="ea184-152">匯入 Microsoft 存放庫金鑰：</span><span class="sxs-lookup"><span data-stu-id="ea184-152">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="ea184-153">建立本機 `azure-cli` 存放庫資訊：</span><span class="sxs-lookup"><span data-stu-id="ea184-153">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="ea184-154">更新 `zypper` 套件索引並安裝：</span><span class="sxs-lookup"><span data-stu-id="ea184-154">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="ea184-155">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-155">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="ea184-156">使用 Docker 安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-156">Install with Docker</span></span>

<span data-ttu-id="ea184-157">我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="ea184-157">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="ea184-158">使用 `docker run` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-158">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="ea184-159">請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。</span><span class="sxs-lookup"><span data-stu-id="ea184-159">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="ea184-160">CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="ea184-160">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="ea184-161">如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。</span><span class="sxs-lookup"><span data-stu-id="ea184-161">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><span data-ttu-id="ea184-162"><a name="Linux"/>不使用套件管理員在 Linux 上安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-162"><a name="Linux"/>Install on Linux without a package manager</span></span>

<span data-ttu-id="ea184-163">如果可行，建議您使用套件管理員安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-163">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="ea184-164">如果您不希望新增 Microsoft 的存放庫，或搭配使用的散發套件並未提供套件，則可以手動安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-164">If you do not want to add Microsoft's repositories, or are working with a distribution which does not have a provided package, you can manually install the CLI.</span></span>

1. <span data-ttu-id="ea184-165">以您的 Linux 散發套件作為基礎安裝必要條件。</span><span class="sxs-lookup"><span data-stu-id="ea184-165">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="ea184-166">如果以上未列出您的散發套件，就必須安裝 [Python 2.7 或更新版本](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。</span><span class="sxs-lookup"><span data-stu-id="ea184-166">If your distribution is not listed above, you will need to install [Python 2.7 or later](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="ea184-167">使用 `curl` 安裝 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-167">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="ea184-168">您可能必須重新啟動 Shell，某些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="ea184-168">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="ea184-169">從具有 `az` 命令的命令提示字元中執行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-169">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ea184-170">疑難排解</span><span class="sxs-lookup"><span data-stu-id="ea184-170">Troubleshooting</span></span>

<span data-ttu-id="ea184-171">如果您在 CLI 安裝期間遇到問題，請查看此章節了解是否涵蓋您的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="ea184-171">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="ea184-172">如果您的問題不在這裡，請[提出 Github 問題](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="ea184-172">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="ea184-173">CURL「物件已移動」錯誤</span><span class="sxs-lookup"><span data-stu-id="ea184-173">curl "Object Moved" error</span></span>

<span data-ttu-id="ea184-174">如果您收到與 `-L` 參數有關，來自 `curl` 的錯誤，或者是包含「物件已移動」文字的錯誤訊息，請嘗試使用完整的 URL 而非 `aka.ms` 來重新導向：</span><span class="sxs-lookup"><span data-stu-id="ea184-174">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="ea184-175">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="ea184-175">`az` command not found</span></span>

<span data-ttu-id="ea184-176">建議您清除 shell 命令雜湊快取。</span><span class="sxs-lookup"><span data-stu-id="ea184-176">You may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="ea184-177">執行</span><span class="sxs-lookup"><span data-stu-id="ea184-177">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="ea184-178">並查看問題是否已解決。</span><span class="sxs-lookup"><span data-stu-id="ea184-178">and see if the problem is resolved.</span></span> <span data-ttu-id="ea184-179">此命令也可能不在您的 `$PATH`中。</span><span class="sxs-lookup"><span data-stu-id="ea184-179">The command may also not be in your `$PATH`.</span></span> <span data-ttu-id="ea184-180">請確定 `<install path>/bin` 有出現在您的 `$PATH` 中，並視需要重新啟動您的 shell。</span><span class="sxs-lookup"><span data-stu-id="ea184-180">Make sure that `<install path>/bin` appears in your `$PATH`, and restart your shell if necessary.</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="ea184-181">解除安裝 CLI 1.x 版本</span><span class="sxs-lookup"><span data-stu-id="ea184-181">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="ea184-182">如果您的系統上可使用較舊的 CLI 1.x 版本，就能以所使用的安裝類型作為基礎加以解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-182">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="ea184-183">使用 npm 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-183">Uninstall with npm</span></span>

<span data-ttu-id="ea184-184">使用 `npm uninstall` 將舊版的 CLI 移除。</span><span class="sxs-lookup"><span data-stu-id="ea184-184">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="ea184-185">使用可散佈解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-185">Uninstall with distributable</span></span>

<span data-ttu-id="ea184-186">如果您是透過 [Azure CLI 安裝程式 (MSI)](http://aka.ms/webpi-azure-cli) 或 [macOS 套件](http://aka.ms/mac-azure-cli)安裝，請使用相同的工具移除您的安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-186">If you installed via the [Azure CLI Installer (MSI)](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="ea184-187">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-187">Uninstall with Docker</span></span>

<span data-ttu-id="ea184-188">如果您安裝了 Docker 映像以使用較舊的 CLI 版本，請將該映像及任何相關聯的容器移除。</span><span class="sxs-lookup"><span data-stu-id="ea184-188">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="ea184-189">接著，您可以在安裝新的 Docker 映像之後重新建立容器，如安裝指示中所述。</span><span class="sxs-lookup"><span data-stu-id="ea184-189">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="ea184-190">更新 CLI</span><span class="sxs-lookup"><span data-stu-id="ea184-190">Update the CLI</span></span>

<span data-ttu-id="ea184-191">若要更新 Azure CLI，請使用您用來安裝它的相同方法。</span><span class="sxs-lookup"><span data-stu-id="ea184-191">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="ea184-192">使用 Homebrew 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-192">Update with Homebrew</span></span>

1. <span data-ttu-id="ea184-193">如果您先前以手動方式安裝，請遵循[使用 Homebrew 安裝](#macOS)的指示。</span><span class="sxs-lookup"><span data-stu-id="ea184-193">If you previously installed manually, follow the [install with Homebrew](#macOS) instructions.</span></span>

2. <span data-ttu-id="ea184-194">更新您的本機 Homebrew 存放庫資訊。</span><span class="sxs-lookup"><span data-stu-id="ea184-194">Update your local Homebrew repository information.</span></span>

   ```bash
   brew update
   ```

3. <span data-ttu-id="ea184-195">升級已安裝的套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-195">Upgrade your installed packages.</span></span>

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a><span data-ttu-id="ea184-196">使用 MSI 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-196">Update with MSI</span></span>

<span data-ttu-id="ea184-197">再次執行 [Azure CLI 安裝程式 (MSI)](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="ea184-197">Run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt"></a><span data-ttu-id="ea184-198">使用 Apt 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-198">Update with apt</span></span>

<span data-ttu-id="ea184-199">若要更新 CLI 套件，請使用 `apt-get upgrade`。</span><span class="sxs-lookup"><span data-stu-id="ea184-199">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="ea184-200">這會將您系統上所有已安裝但尚未進行相依性變更的套件進行升級。</span><span class="sxs-lookup"><span data-stu-id="ea184-200">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="ea184-201">若只要升級 CLI，請使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="ea184-201">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-yum"></a><span data-ttu-id="ea184-202">使用 Yum 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-202">Update with yum</span></span>

<span data-ttu-id="ea184-203">使用 `yum update` 命令更新 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="ea184-203">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a><span data-ttu-id="ea184-204">使用 Zypper 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-204">Update with zypper</span></span>

<span data-ttu-id="ea184-205">您可以使用 `zypper update` 命令更新套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-205">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

### <a name="update-with-docker"></a><span data-ttu-id="ea184-206">使用 Docker 更新</span><span class="sxs-lookup"><span data-stu-id="ea184-206">Update with Docker</span></span>

1. <span data-ttu-id="ea184-207">使用 `docker pull` 更新本機映像。</span><span class="sxs-lookup"><span data-stu-id="ea184-207">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="ea184-208">取得目前使用 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="ea184-208">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="ea184-209">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="ea184-209">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="ea184-210">停止並重新建立容器。</span><span class="sxs-lookup"><span data-stu-id="ea184-210">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="ea184-211">手動更新</span><span class="sxs-lookup"><span data-stu-id="ea184-211">Update manually</span></span>

<span data-ttu-id="ea184-212">請遵循 [macOS](#macOS) 或 [Linux](#Linux) 的手動安裝指示進行更新。</span><span class="sxs-lookup"><span data-stu-id="ea184-212">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="ea184-213">解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-213">Uninstall</span></span>

<span data-ttu-id="ea184-214">如果您決定要將 CLI 解除安裝，我們很遺憾您不再繼續使用。</span><span class="sxs-lookup"><span data-stu-id="ea184-214">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="ea184-215">您應該使用您用來安裝 CLI 的相同方法來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-215">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="ea184-216">使用 Homebrew 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-216">Uninstall with Homebrew</span></span>

<span data-ttu-id="ea184-217">解除安裝 `azure-cli` 套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-217">Uninstall the `azure-cli` package.</span></span>

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a><span data-ttu-id="ea184-218">使用 MSI 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-218">Uninstall with MSI</span></span>

<span data-ttu-id="ea184-219">請重新執行 [MSI](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-219">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt"></a><span data-ttu-id="ea184-220">使用 Apt 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-220">Uninstall with apt</span></span>

<span data-ttu-id="ea184-221">透過 `apt-get remove` 解除安裝：</span><span class="sxs-lookup"><span data-stu-id="ea184-221">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a><span data-ttu-id="ea184-222">使用 Yum 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-222">Uninstall with yum</span></span>

1. <span data-ttu-id="ea184-223">從系統移除套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-223">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="ea184-224">如果您不打算重新安裝 CLI，移除存放庫資訊。</span><span class="sxs-lookup"><span data-stu-id="ea184-224">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="ea184-225">如果您移除存放庫資訊，也會移除 Microsoft GPG 簽章金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea184-225">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a><span data-ttu-id="ea184-226">使用 Zypper 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-226">Uninstall with zypper</span></span>

1. <span data-ttu-id="ea184-227">從系統移除套件。</span><span class="sxs-lookup"><span data-stu-id="ea184-227">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="ea184-228">如果您不打算重新安裝 CLI，移除存放庫資訊。</span><span class="sxs-lookup"><span data-stu-id="ea184-228">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="ea184-229">如果您移除存放庫資訊，也會移除 Microsoft GPG 簽章金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea184-229">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="ea184-230">使用 Docker 解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-230">Uninstall with Docker</span></span>

<span data-ttu-id="ea184-231">如果您已安裝 Docker 映像，就必須移除任何執行它的容器，然後再將本機映像刪除。</span><span class="sxs-lookup"><span data-stu-id="ea184-231">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="ea184-232">取得執行 azure-cli 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="ea184-232">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="ea184-233">將任何使用 CLI 映像的容器刪除。</span><span class="sxs-lookup"><span data-stu-id="ea184-233">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="ea184-234">將本機安裝的 CLI 映像移除。</span><span class="sxs-lookup"><span data-stu-id="ea184-234">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="ea184-235">如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="ea184-235">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><span data-ttu-id="ea184-236"><a name="UninstallManually"/>手動解除安裝</span><span class="sxs-lookup"><span data-stu-id="ea184-236"><a name="UninstallManually"/>Uninstall manually</span></span>

<span data-ttu-id="ea184-237">如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ea184-237">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="ea184-238">移除已安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="ea184-238">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="ea184-239">將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。</span><span class="sxs-lookup"><span data-stu-id="ea184-239">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

3. <span data-ttu-id="ea184-240">如果您的殼層使用命令快取，請將它重新載入。</span><span class="sxs-lookup"><span data-stu-id="ea184-240">If your shell uses a command cache, reload it.</span></span>

   ```bash
   hash -r
   ```

> [!Note]
> <span data-ttu-id="ea184-241">預設安裝位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="ea184-241">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="ea184-242">報告 CLI 問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="ea184-242">Report CLI issues and feedback</span></span>

<span data-ttu-id="ea184-243">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="ea184-243">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="ea184-244">若要從命令列提供意見反應，請使用 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="ea184-244">To provide feedback from the command line, use the `az feedback` command.</span></span>
