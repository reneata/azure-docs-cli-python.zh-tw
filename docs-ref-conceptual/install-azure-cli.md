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
# <a name="install-azure-cli-20"></a>安裝 Azure CLI 2.0

立即安裝新版 Azure CLI！
我們已改進並更新此版本，以提供絕佳的原生命令列，讓您管理 Azure 資源。
它可以用於 macOS、Linux 和 Windows。
如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azure-cli.md)。

> [!NOTE]
> 如果您需要舊版 Azure CLI，此處提供 [安裝 Azure CLI 1.0](/azure/cli-install-nodejs) 的方法。

## <a name="macos"></a>macOS

> [!WARNING]
> Azure CLI 的 Homebrew 公式 `azure-cli` 目前過期，且會安裝舊版。

1. 使用 `curl` 命令來安裝 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 您可能必須重新啟動命令殼層，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 從具有 `az` 命令的命令提示字元中執行 CLI。

> [!Note]
> 當您使用 InstallAzureCli 安裝時，不支援 [`az component update`](/cli/azure/component#update)。
> 若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。

## <a name="windows"></a>Windows

您可以使用 MSI 來安裝 Azure CLI 2.0，然後在 Windows 命令列中使用它，或是使用 Windows 上 Ubuntu 之 Bash 上的 apt-get 來安裝 CLI。

### <a name="msi-for-the-windows-command-line"></a>適用於 Windows 命令列的 MSI 

若要在 Windows 上安裝 CLI，然後在 Windows 命令列中使用它，請下載並執行 [msi](https://aka.ms/InstallAzureCliWindows)。

> [!NOTE]
> 使用 msi 來進行安裝時，不支援 [`az component`](/cli/azure/component)。
> 若要更新成最新的 CLI，請重新執行 [msi](https://aka.ms/InstallAzureCliWindows)。
> 
> 若要將 CLI 解除安裝，請重新執行 [msi](https://aka.ms/InstallAzureCliWindows) 並選擇解除安裝。

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a>Windows 上 Ubuntu 之 Bash 的 apt-get

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

> [!NOTE]
> 當您使用 apt-get 進行安裝時，不支援 [`az component`](/cli/azure/component)。
> 若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要解除安裝，請執行 `sudo apt-get remove azure-cli`。

## <a name="apt-get-for-debianubuntu"></a>apt-get for Debian/Ubuntu

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

> [!NOTE]
> 當您使用 apt-get 進行安裝時，不支援 [`az component`](/cli/azure/component)。
> 若要更新 CLI，請再次執行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要解除安裝，請執行 `sudo apt-get remove azure-cli`。

## <a name="docker"></a>Docker

我們會維護使用 Azure CLI 2.0 預先設定的 Docker 映像。

使用 `docker run` 安裝 CLI。

```bash
docker run azuresdk/azure-cli-python:<version>
```

請參閱我們的 [Docker 標籤](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)，以取得可用的版本。

> [!NOTE]
> 如果您想要從使用者環境挑選 SSH 金鑰，可以使用 `-v ${HOME}:/root` 來裝載 $HOME 作為 `/root`。

>> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

CLI 會安裝在映像上，作為 `/usr/local/bin` 中的 `az` 命令。

> [!NOTE]
> Docker 映像不支援 [`az component`](/cli/azure/component) 功能。
> 若要更新 Azure CLI 2.0，請使用 `docker run` 來安裝最新的映像或您想要的特定映像。

## <a name="linux"></a>Linux

1. 如果沒有 Python，請[安裝](https://www.python.org/downloads)。

2. 根據您的 Linux 散發套件，安裝必要條件。

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

3. 使用一個 `curl` 命令安裝 CLI。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

4. 您可能必須重新啟動命令殼層，某些變更才會生效。

   ```bash
   exec -l $SHELL
   ```

5. 從具有 `az` 命令的命令提示字元中執行 CLI。

> [!Note]
> 當您使用 InstallAzureCli 安裝時，不支援 [`az component update`](/cli/azure/component#update)。
> 若要更新為最新的 CLI，請再次執行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要解除安裝，請參閱 [手動解除安裝說明](#uninstall)。

## <a name="troubleshooting"></a>疑難排解

### <a name="errors-with-curl-redirection"></a>使用 curl 重新導向時發生的錯誤

如果您收到與 `-L` 參數有關，來自 `curl` 命令的錯誤，或者是某錯誤指出「物件已移動」，請嘗試使用完整的 url，而非 aka.ms url：

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

## <a name="uninstall"></a>解除安裝

如果您使用在 https://aka.ms/InstallAzureCli 的指令碼安裝 CLI，您可以利用下列步驟進行解除安裝。

1. 移除已安裝的檔案。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 將 `<install location>/lib/azure-cli/az.completion` 行從 `<install location>/.bash_profile` 刪除。

> [!Note]
> 預設安裝位置是 `/Users/<username>`。

如果您使用 apt-get、Docker 或 msi 來安裝 CLI，請使用相同的工具來將它解除安裝。

## <a name="reporting-issues-and-feedback"></a>報告問題和意見反應

如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-cli/issues)一節中提出問題。
若要透過命令行提供意見反應，請嘗試 `az feedback` 命令。
