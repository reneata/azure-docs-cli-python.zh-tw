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
# <a name="install-azure-cli-20"></a>安裝 Azure CLI 2.0

立即安裝新版 Azure CLI！
我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。
它可以用於 macOS、Linux 和 Windows。
如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。

> [!NOTE]
> 如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>在 MacOS 上安裝

1. 使用 `curl` 安裝 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 您可能必須重新啟動 Shell，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 從具有 `az` 命令的命令提示字元中執行 CLI。

## <a name="install-on-windows"></a>在 Windows 上安裝

您可以使用 MSI 來安裝 Azure CLI 2.0，然後在 Windows 命令列中使用它，或是使用 Windows 上 Ubuntu 之 Bash 上的 `apt-get` 來安裝 CLI。

### <a name="install-with-msi-for-the-windows-command-line"></a>使用適用於 Windows 命令列的 MSI 安裝 

若要在 Windows 上安裝 CLI，然後在 Windows 命令列中使用它，請下載並執行 [MSI](https://aka.ms/InstallAzureCliWindows)。

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a>使用 Windows 上 Ubuntu 之 Bash 的 apt-get 安裝

1. 如果在 Windows 上沒有 Bash，請[安裝它](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. 開啟 Bash 殼層。

3. 修改來源清單。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. 執行下列 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  從具有 `az` 命令的命令提示字元中執行 CLI。

## <a name="install-on-debianubuntu-with-apt-get"></a>使用 apt get 在 Debian/Ubuntu 上安裝

以 Debian/Ubuntu 為基礎的系統，您可以透過 `apt-get` 安裝 Azure CLI 2.0。

1. 修改來源清單。
 
   - 32 位元系統

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64 位元系統

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. 執行下列 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  從具有 `az` 命令的命令提示字元中執行 CLI。

## <a name="install-with-docker"></a>使用 Docker 安裝

我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。

使用 `docker run` 安裝 CLI。

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。

CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。

> [!NOTE]
> 如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><a name="Linux"/>不使用 apt-get 在 Linux 安裝

如果可行，建議您使用 `apt-get` 安裝 CLI。 針對不需要使用 `apt` 套件管理員的散發套件，您可以手動方式來安裝。

1. 以您的 Linux 散發套件作為基礎安裝必要條件。

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

如果以上未列出您的散發套件，就必須安裝 [Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。

2. 使用 `curl` 安裝 CLI。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 您可能必須重新啟動 Shell，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```

4. 從具有 `az` 命令的命令提示字元中執行 CLI。

## <a name="troubleshooting"></a>疑難排解

如果您在 CLI 安裝期間遇到問題，請查看此章節了解是否涵蓋您的特殊案例。 如果您的問題不在這裡，請[提出 Github 問題](https://github.com/Azure/azure-cli/issues)。

### <a name="curl-object-moved-error"></a>CURL「物件已移動」錯誤

如果您收到與 `-L` 參數有關，來自 `curl` 的錯誤，或者是包含「物件已移動」文字的錯誤訊息，請嘗試使用完整的 URL 而非 `aka.ms` 來重新導向：

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a>macOS 上安裝較舊版本的 Homebrew

macOS 可用的 Homebrew `azure-cli` 公式目前已過期，且會安裝 CLI 的 1.x 版本。 您可以在更新時加以查看，方法是檢查 `brew info azure-cli`。

在此之前，[解除安裝舊版](#uninstall_brew)並遵循 [macOS 安裝指示](#macOS)。

## <a name="uninstall-cli-1x-versions"></a>解除安裝 CLI 1.x 版本

如果您的系統上可使用較舊的 CLI 1.x 版本，就能以所使用的安裝類型作為基礎加以解除安裝。

### <a name="uninstall-with-npm"></a>使用 npm 解除安裝

使用 `npm uninstall` 將舊版的 CLI 移除。

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><a name="uninstall_brew"/>使用 macOS 上的 Homebrew 解除安裝

使用 `brew uninstall` 將舊版的 CLI 移除。

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a>使用可散佈解除安裝

如果您是透過 [MSI](http://aka.ms/webpi-azure-cli) 或 [macOS 套件](http://aka.ms/mac-azure-cli)安裝，請使用相同的工具將您的安裝移除。

### <a name="uninstall-with-docker"></a>使用 Docker 解除安裝

如果您安裝了 Docker 映像以使用較舊的 CLI 版本，請將該映像及任何相關聯的容器移除。 接著，您可以在安裝新的 Docker 映像之後重新建立容器，如安裝指示中所述。

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>更新 CLI

若要更新 Azure CLI，請使用您用來安裝它的相同方法。

### <a name="update-with-msi"></a>使用 MSI 更新

再次執行 [MSI](https://aka.ms/InstallAzureCliWindows)。

### <a name="update-with-apt-get"></a>使用 apt-get 更新

若要更新 CLI 套件，請使用 `apt-get upgrade`。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> 這會將您系統上所有已安裝但尚未進行相依性變更的套件進行升級。
> 若只要升級 CLI，請使用 `apt-get install`。
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a>使用 Docker 更新

1. 使用 `docker pull` 更新本機映像。

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. 取得目前使用 CLI 映像的容器。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> 如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。

3. 停止並重新建立容器。

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a>手動更新

請遵循 [macOS](#macOS) 或 [Linux](#Linux) 的手動安裝指示進行更新。

## <a name="uninstall"></a>解除安裝

如果您決定要將 CLI 解除安裝，我們很遺憾您不再繼續使用。 您應該使用您用來安裝 CLI 的相同方法來解除安裝。

### <a name="uninstall-with-msi"></a>使用 MSI 解除安裝

請重新執行 [MSI](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。

### <a name="uninstall-with-apt-get"></a>使用 apt get 解除安裝

透過 `apt-get remove` 解除安裝：

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a>使用 Docker 解除安裝

如果您已安裝 Docker 映像，就必須移除任何執行它的容器，然後再將本機映像刪除。

1. 取得執行 azure-cli 映像的容器。

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. 將任何使用 CLI 映像的容器刪除。

  ```bash
  docker rm 34a868beb2ab
  ```

3. 將本機安裝的 CLI 映像移除。

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> 如果您已安裝特定版本的映像，就必須將 `:<version>` 新增至映像名稱的結尾。

### <a name="uninstall-manually"></a>手動解除安裝

如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。

1. 移除已安裝的檔案。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。

> [!Note]
> 預設安裝位置是 `/Users/<username>`。

## <a name="report-cli-issues-and-feedback"></a>報告 CLI 問題和意見反應

如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。
若要從命令列提供意見反應，請使用 `az feedback` 命令。
